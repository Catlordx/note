# Rust

### 引用：

- A reference is said to “borrow” the value it refers to, and this is a good model for students not familiar with pointers: code can use the reference to access the value, but is still “owned” by the original variable. The course will get into more detail on ownership in day 3.
- References are implemented as pointers, and a key advantage is that they can be much smaller than the thing they point to. Students familiar with C or C++ will recognize references as pointers. Later parts of the course will cover how Rust prevents the memory-safety bugs that come from using raw pointers.
- Rust does not automatically create references for you - the `&` is always required.
- ***Rust will auto-dereference in some cases***, in particular when invoking methods (try `r.is_ascii()`). There is no need for an `->` operator like in C++.And you will see that when you use slice ,rust will help you to deref too.
- In this example, `r` is mutable so that it can be reassigned (`r = &b`). Note that this re-binds `r`, so that it refers to something else. This is different from C++, where assignment to a reference changes the referenced value.
- A shared reference does not allow modifying the value it refers to, even if that value was mutable. Try `*r = 'X'`.
- Rust is tracking the lifetimes of all references to ensure they live long enough. Dangling references cannot occur in safe Rust. `x_axis` would return a reference to `point`, but `point` will be deallocated when the function returns, so this will not compile.

## 1.所有权

Rust的引用仅仅允许我们读取值或者调用方法，捕获的值的所有权。要想直接通过引用修改值必须调用方法！Rust的引用实际上类似于C++中的指针！只不过Rust会自动为我们进行一些个操作，例如调用方法不用我们->

​	***所有权***是Rust的核心功能之一。对于内存的管理有很多种方式，

* 一种类似于C/C++手动管理内存，让人头秃而且经常出现一些莫名其妙的问题。
* 另一种则是像Java中的gc（garbage collection），程序员无需手动管理内存，但使用gc对程序的运行速度影响很大。

那么Rust是如何保证内存安全的前提下，保持程序的运行速度呢？答案是，***所有权系统***。

> 所有权规则
>
> 1.Rust中的每一个值都有一个所有者。
>
> 2.值在任何时刻有且仅有一个所有者
>
> 3.当值的所有者离开作用域的时候，这个值将会被丢弃

值存放在内存的栈或堆中，而我们声明的变量更多的像是一个**指针**，指向了这样一块内存。只不过我们无需像C/C++一样手动的解引用来读取值或者调用其上相应的方法，这些事情Rust都已经帮我们很好的完成了。

### 1.1 规则解读

#### 1.1.1 Rust中的每一个值都有一个所有者

这句话其实主要是针对于***堆***上的值。

对于***栈***上的值，下列代码是毫无问题的：

~~~rust
fn main(){
    let x = 1006;
    let y = x;
    println!("x is {} , y is {}",x,y);   // x is 1006 , y is 1006
}
~~~

这段代码首先将 5 绑定到x上，然后生成一个x对应的值的拷贝，将其绑定到y上。x，y实际上并没有指向同一个值，或者说同一段内存空间。

然而对于***堆***上的值，这样的代码就有大问题了：

~~~rust
fn main(){
    let str1 = String::from("A simple demo!");
    let str2 = str1;
    println!("{} , dudududuudu",str1);
}
~~~

首先编译一下。

![image-20240315121649685](./Rust.assets/image-20240315121649685.png)

很遗憾，编译没有通过。编译器告诉我们str1的值被移动了，在我们的println！中自然无法借用。

注：编译器很人性化的告诉了我们如何修改：那就是生成一份完全一样的拷贝，然后把它绑定到str2上。

![image-20240315155446914](./Rust.assets/image-20240315155446914.png)

[^1]: 引自The Rust Programming Language



~~~rust
let demo = String::from("Hello！World!")
~~~

一个String类型的变量，变量本身是存储在栈中的，对应的值存放在堆中

* 一个指向存放字符串内容的内存的指针（指向其绑定的值）
* 字符串的长度（len）：表示字符串中实际存储的Unicode字符的数量，可以通过***len()***方法来获得这个值。
* 字符串的容量（capacity）：这是为该字符串分配的内存空间的大小。可以使用***capacity()***方法来获取。

那么其实我们可以简单的把前文中的str1当作一个指针，指向了一块内存区域。

当我们试图把str1复制给str2，就会出现下面这种情况。

![image-20240315161051064](./Rust.assets/image-20240315161051064.png)

显而易见的，栈上现在有两份数据都同时指向堆中的一份数据。变量str2的内容实际上就是str1内容的拷贝。而不是还同时拷贝了堆内存上的数据，像这样

![image-20240315161457818](./Rust.assets/image-20240315161457818.png)

> 曾经学习过C++的人可能会看他们俩很眼熟，神似深拷贝和浅拷贝的区别。

当变量离开作用域后，Rust会自动调用`drop`函数并清理变量的堆内存。那么当上面代码中的str1,str2离开作用域后，他们都会尝试释放相同的堆内存，这是一个十分典型的***二次释放***的错误。那么在Rust中，如何确保这样的问题不会发生呢？在我们`let str2 = str1;`之后，Rust认为str1不再有效（或许可以理解为：Rust已经不把str1当人看了？），因此Rust不需要在`str1`离开作用域后清理别的什么东西，只需要把栈上相关内存释放就好了。



## 2.生命周期



## 3.函数式编程

### 3.1 迭代器

在Rust中，`iter()`、`iter_mut()` 和 `into_iter()` 是针对不同类型的集合（比如数组、向量、哈希表等）提供的方法，用于在集合上进行迭代。它们的区别在于迭代器的所有权和可变性。

`iter()`: `iter()` 方法用于在不消耗集合的情况下产生一个不可变引用的迭代器。这意味着你可以通过迭代器遍历集合中的每个元素，但无法对集合本身进行修改。因此，这个方法适用于需要只读访问集合元素的场景。

```
rustCopy codelet vec = vec![1, 2, 3];
for i in vec.iter() {
    println!("{}", i);
}
```

`iter_mut()`: `iter_mut()` 方法产生一个可变引用的迭代器，允许你对集合中的元素进行修改。但是，这并不意味着你可以同时对集合进行修改。在迭代器存在的情况下，你无法再对集合进行可变访问，这是Rust借用检查规则的一部分。

```rust
codelet mut vec = vec![1, 2, 3];
for i in vec.iter_mut() {
    *i += 1;
}
```

`into_iter()`: `into_iter()` 方法消耗集合并返回一个拥有所有权的迭代器。这意味着在使用 `into_iter()` 后，你无法再次使用原始的集合，因为它的所有权已经被转移。这种方法在你希望在迭代过程中拥有对集合的完全所有权时非常有用，因为它允许你在迭代完成后销毁集合。

```rust
codelet vec = vec![1, 2, 3];
for i in vec.into_iter() {
    println!("{}", i);
}
// 这里不能再使用 vec，因为它的所有权已经被转移
```

总之，`iter()` 产生一个不可变引用的迭代器，允许只读访问集合；`iter_mut()` 产生一个可变引用的迭代器，允许修改集合中的元素；`into_iter()` 消耗集合并产生一个拥有所有权的迭代器，用于迭代过程中拥有对集合的完全所有权。

闭包接收参数一般情况下是引用，而迭代器是在引用的基础上进行迭代的因此就有一个很有意思的现象就是，我们在闭包中获得的x实际上是一个双重引用。我们可以通过结构获得值

### 3.2 filter方法

filter方法返回的是一个迭代器

## 4.文件读写

首先

~~~rust
    let input = input.trim();
    let mut file = match File::open(&input) {
        Ok(file) => file,
        Err(err) => {
            eprintln!("something wrong happened when open the file: {}", err);
            return;
        }
    };
    let mut content = String::new();
    let byte_count = match file.read_to_string(&mut content) {
        Ok(byte_count) => byte_count,
        Err(err) => {
            eprintln!("something wrong happened when read the file: {}", err);
            return;
        }
    };
    println!("{} bytes read", byte_count);
~~~

这段代码是只能够读取以UTF-8编码的文件（`file.read_to_string`）

~~~Rust
    let mut content: Vec<u8> = Vec::new(); // 用于存储二进制数据
    let byte_count = match file.read_to_end(&mut content) { // 以二进制形式读取文件内容
        Ok(byte_count) => byte_count,
        Err(err) => {
            eprintln!("something wrong happened when read the file: {}", err);
            return;
        }
    };
~~~

以二进制形式读取即可

## 5.模式

在利用模式进行结构的时候如果涉及到分配在堆上的变量，那么所有权会发生转移，栈上数据会直接进行复制操作。

## 6.标准库

#### str::replace

可以将一个string类型中的某些指定的字符串替换为我们需要的字符串，返回一个新的字符串