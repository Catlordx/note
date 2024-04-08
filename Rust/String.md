## String

在很长时间内我们都会同字符串打交道，因此我们必须掌握Rust标准库提供给我们的相关API.



### 1.创建一个新String

> 如果没有特殊标注，所有则不会有所有权转移的问题

#### 1.1 通过字符串字面量

~~~rust
let s = "Hello".to_string();

let s = String::from("World");
// 通过into方法创建一个新的String必须显式标明类型
let s:String = "Hello World!".into();
~~~

#### 1.2 通过+运算符

~~~rust
/// 通过+运算符的方式
let s = String::from("Hello");

// 在执行下面操作的过程中
//首先会创建一个新的`String`变量用于存储拼接的结果
//然后将`s`的内容复制到新的String中
//最后在新的`String`末尾增加`, world`内容
let demo = s + ", World";
~~~

#### 1.3 使用format！宏

##### 1.3.1 基本语法

`format!` 宏的格式化字符串可以包含占位符 `{}`，用于表示需要插入的值的位置。在插入时，这些占位符会被对应参数的值替换。

例如：

~~~rust
let s_end = String::from("World!");
let format_string_demo = format!("Hello, {}",s_end);
println!("{}",format_string_demo)      // Hello, World!
~~~

其中{}是一个占位符，会被后面的`value`替换掉。value可以是任何类型的数据，只要实现了`Display`trait即可。(`Display`trait提供了将类型转换为字符串表示的能力)。

##### 1.3.2 命名参数

可以给参数命名，以便在格式化字符串中引用

~~~rust
format!("{h} , {w}!",h="hello",w="world")
~~~

##### 1.3.3 格式化参数

###### 整数格式化参数：

- `{}`: 默认格式
- `{:b}`:以二进制形式输出，可以在`#b`中指定位数。
- `{:o}`: 以八进制形式输出。
- `{:x}`: 以十六进制形式输出。
- `{:X}`: 以十六进制形式输出，大写字母。
- `{:>5}`：右对齐，占5位
- `{:<5}`：左对齐，占五位
- `{:>width$}`：右对齐，占width位

~~~rust
    let num = 10;
    println!("{:>5}",num);
    println!("{:<5}1",num);
    println!("{:>width$}",num,width=10);
    println!("Decimal: {}",num);
    println!("Binary: {:b}",num);
    println!("Octal: {:o}",num);
    println!("Hexadecimal: {:x}",num);
    println!("Hexadecimal(uppercase): {:X}",num);

// 输出结果
   10
10   1
        10
Decimal: 10
Binary: 1010
Octal: 12
Hexadecimal: a
Hexadecimal(uppercase): A
~~~

###### 浮点数格式化参数

~~~rust
let pi = 3.1415926;
println!("Rounded to 2 decimal places: {:.2}", pi); // 3.14
~~~

###### 字符串格式化参数

```rust
let name = "Alice";
println!("Name: {}", name);
println!("Padded name: {:<10},1", name);
println!("Truncated name: {:.3}", name);

// 输出
Name: Alice
Padded name: Alice     ,1
Truncated name: Ali
```

#### 1.4 创建空String

~~~rust
let s = String::new();

// 创建一个具有指定大小的字符串
let s_1 = String::with_capacity(your_given_capacity);
~~~



### 2.String类型的常用API

#### 2.1 拼接和追加

~~~rust
fn main() {
    let test_string = String::from(" Wow!");
    let mut s = String::with_capacity(10);
    println!("{}",s);
    // 将一个字符追加到字符串后面
    s.push('1');
    println!("{}",s); // 1

    // 将一个字符串切片追加到字符串后面
    s.push_str("I am a slice");
    println!("{}",s); // 1I am a slice
    s.push_str(&test_string);
    println!("{}",s); // 1I am a slice Wow!
    s.push_str(&test_string[2..]);
    println!("{}",s); // 1I am a slice Wow!ow!
}
~~~

#### 2.2 切片

~~~rust
~~~

#### 2.3 获得相关属性

~~~rust
fn main() {
    let s = String::from("尬emo!");
    // 获得字符串大小
    println!("{}",s.len()); // 7
    // 查询字符串是否为空
    assert_eq!(s.is_empty(),false);
    // 查看所有字符是否都是ASCII字符
    assert_eq!(!s.is_ascii(),true);
    assert_eq!("Grüße, Jürgen ❤".to_string().is_ascii(),false);
    // 在Unicode字符串中，一个字符可能由一个或多个字节表示，这取决于字符的编码方式
    // 在UTF-8编码中，每个字节的最高位用于指示该字节是否为字符的起始字节，从而确定字符的边界
    // 如果一个字节以'0'开头，则表示该字节是字符的起始字节，如果一个字节以'10'开头，则表示该字节是字符的后续字节
    // 因此，一个有效的 Unicode 字符边界是指一个索引处于字符串中某个字符的起始字节的位置。
    // 如果一个索引处于有效的 Unicode 字符边界上，则意味着在该索引处访问的字节是 UTF-8 编码中的字符的起始字节，从而确保我们可以正确地访问字符串中的每个字符。
    // 通过 is_char_boundary 方法，我们可以检查给定索引的字节是否位于有效的 Unicode 字符边界上，以确保我们在处理字符串时不会破坏字符编码的完整性，从而避免产生无效的 Unicode 字符序列。
    assert!(!s.is_char_boundary(1));
    assert!(s.is_char_boundary(0));
}
~~~

#### 2.4 子串相关

~~~rust
fn main() {
    let s = String::from("I am the am one who will win!");
    // 检查字符串是否包含指定子串
    assert!(s.contains("am"));

    // 检查字符串是否以子串开头
    assert!(s.starts_with("I am"));
    // assert!(s.starts_with("i"));

    // 检查字符串是否以子串结尾
    assert!(s.ends_with("win!"));

    // 从前往后查找指定字串在字符串的位置,返回值为Option类型
    // 字串存在则返回Some，不存在则返回None
    // 只能查到第一个字串的位置
    match s.find("am") {
        Some(loc) => println!("{}",loc),
        None => println!("不存在指定字串捏！")
    }
    // 从后往前
    match s.rfind("am") {
        Some(loc) => println!("{}",loc),
        None => println!("不存在指定的字串捏")
    }
    // 统计字串出现的次数
    println!("Sub string appears {} times",s.matches("am").count());
}
~~~

#### 2.5 字符串转换

~~~rust
fn main() {
    // parse方法将字符串解析为其他类型
    let string_to_integer = String::from("123");
    match string_to_integer.parse::<i32>() {
        Ok(demo_integer) => println!("{}", demo_integer),
        Err(err) => eprintln!("{}", err),
    }
    let string_to_float = String::from("3.1415926");
    match string_to_float.parse::<f64>() {
        Ok(demo_float) => println!("{}", demo_float),
        Err(err) => eprintln!("{}", err),
    }
    let basic_demo: i32 = string_to_integer.parse().unwrap();
    println!("{}", basic_demo);

    // 将字符串转换为大或小写
    println!("{}", "ABDCD".to_lowercase());
    println!("{}", "string_to_integer".to_uppercase());
    let mut s = String::from("Grüße, Jürgen ❤");
    // to_ascii_lowercase方法将字符串中所有ASCII字符转换成小写
    assert_eq!("grüße, jürgen ❤", s.to_ascii_lowercase());
    println!("{}", s);

    // 清除字符串首尾空格,返回的是引用
    let demo = String::from("    dmeo    ");
    println!("{}", demo.trim());
    println!("{}", demo);

    // split_whitespace方法根据空白字符拆分字符串，返回一个迭代器（迭代源字符串的切片）
    let mut demo = String::from("I will do it as you want");
    let splited_demo: Vec<&str> = demo.split_whitespace().collect();
    println!("{}", demo);
    println!("{:?}", splited_demo);
    // TODO 从指定位置(byte)开始的部分都被切下来分给一个新的，也就是说，真的修改了字符串！
    let the_former = demo.split_off(6);
    assert_eq!("I will", demo);
    assert_eq!(" do it as you want", the_former);

    // 此方法就返回的是两个引用了
    let s = String::from("Per Martin-Löf");

    let (first, last) = s.split_at(3);

    assert_eq!("Per", first);
    assert_eq!(" Martin-Löf", last);
    println!("{}", s);

    // 返回的是两个可变引用
    let mut s = "Per Martin-Löf".to_string();
    {
        let (first, last) = s.split_at_mut(3);
        first.make_ascii_uppercase();
        assert_eq!("PER", first);
        assert_eq!(" Martin-Löf", last);
    }
    assert_eq!("PER Martin-Löf", s);

    // 根据模式进行切分字符串！
    let v: Vec<&str> = "Mary had a little lamb".split(' ').collect();
    assert_eq!(v, ["Mary", "had", "a", "little", "lamb"]);

    // 同上，但是不抛弃模式所匹配的内容
    let v: Vec<&str> = "Mary had a little lamb\nlittle lamb\nlittle lamb.\n"
        .split_inclusive('\n')
        .collect();
    assert_eq!(
        v,
        [
            "Mary had a little lamb\n",
            "little lamb\n",
            "little lamb.\n"
        ]
    );
}
~~~

