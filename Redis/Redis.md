# Redis

Redis:Remote Dictionary Server(远程字典服务器)

==Redis is an in-memory database that persists on disk==. The data model is key-value, but many different kind of values are supported: Strings, Lists, Sets, Sorted Sets, Hashes, Streams, HyperLogLogs, Bitmaps.

引入Redis的原因：

​	事实上，大部分情况下，对数据的操作还是以查询为主。显而易见的是每次查询都需要经过硬盘IO操作会比直接内存操作要慢。

![image-20240114183003101](D:/CS/Note/Redis/Redis.assets/image-20240114183003101.png)

主要是为传统的RDBMS减负。Redis是kv数据库（noSQL的一种）。Reddis数据操作主要在内存，而MySQL主要存储在磁盘。Redis通常永固一些特定场景，与MySQL配合使用。。

Redis的优势：

* 性能极高——Redis读的速度为110000次/秒，写的速度是81000/秒
* Reis数据类型丰富，不仅仅支持简单的key-value类型的数据，同时还提供list，set，zst，hash等数据结构的存储
* Reis支持数据的持久化，可以将内存中的数据保持再磁盘中，重启的时候可以再次加载进行使用
* Redis支持数据的备份，即master-slave模式的数据备份

参考资料：

* Redis源码地址：https://github.com/redis/redis
* Redis在线测试：https://try.redis.io/
* Redis命令参考：https://redis.io/commands/

新特性：https://github.com/redis/redis/releases

## 1. Redis安装、配置与卸载

Redis的压缩包放在/opt目录下，在/opt目录解压然后通过make && make install 下载

Redis的默认安装路径在/usr/local/bin

Redis密码111111

启动redis需要 redis-server /myredis/redis7.conf（因为redis安装在bin目录下，所以在任何位置都可以直接使用）

> 此处是启动的服务端，使用的是我们自己彼岸写的myredis目录下的conf文件（拷贝的源文件）

然后输入redis-cli -a 111111 进行登录 (-p 6379，默认就是6379端口)

> 此处启动客户端如果不加-a及以后内容就会提示
>
> ((error) NOAUTH Authentication required)，这时候输入auth 111111即可

查看启动成功：ps -ef | grep redis

![image-20240114201712704](D:/CS/Note/Redis/Redis.assets/image-20240114201712704.png)

退出客户端

![image-20240114202254654](D:/CS/Note/Redis/Redis.assets/image-20240114202254654.png)

如果要关闭Redis，则只需在Redis内部输入SHUTDOWN即可。

外部关闭方式：

* 单实例关闭：redis-cli -a 111111 shutdown
* 多实例关闭，指定端口关闭：redis-cli -p 6379 shutdown

Redis卸载：

![image-20240114203118534](D:/CS/Note/Redis/Redis.assets/image-20240114203118534.png)

## 2. Redis的十大数据类型

![image-20240114203336343](D:/CS/Note/Redis/Redis.assets/image-20240114203336343.png)

> 此处说的数据类型是Value的数据类型，key一般为String

### 2.1 字符串

~~~
// 字符串
set k1 hello!word
~~~

string类型是==二进制安全的==，相当于支持序列化，意思是redis的string可以包含任何数据，比如jpg图片或者序列化的对象。string类型是Redis最基本的数据类型，一个Redis中字符串value最多可以是==512M==

### 2.2 List（列表）

Redis列表是简单的字符串列表，按照插入顺序排序。可以添加一个元素到列表的头部（左边）或者尾部（右边），它的底层实际是个==双端链表==，最多可包含2^32^-1个元素。最经典的就是Java的linklist

### 2.3 哈希表（Hash）

Redis Hash十一个String类型的field（字段）和value（值）的映射表，hash特别适合用于存储对象。

### 2.4 集合（Set）

Redis的Set是String类型的无序集合。集合成员是唯一的，这就意味着集合中不能出现重复的数据，集合对象的编码可以是Intset或者hashtable。Redis中Set集合是通过哈希表实现的，所以添加，删除，查找的复杂度都是O（1）

### 2.5 ZSet(Sorted set)

不同的是每个元素都会关联一个double类型的愤俗，redis正是通过分数来为集合中的成员进行从小到大的排序。

zset的成员是唯一的，但分数（score）可以重复

### 2.6 

### 2.11 命令查询

https://redis.io/commands/

![image-20240114210850409](D:/CS/Note/Redis/Redis.assets/image-20240114210850409.png)

![image-20240114210915816](D:/CS/Note/Redis/Redis.assets/image-20240114210915816.png)

默认数据库是0号库，下标最高为15号

> 命令不区分大小写，但`key`区分

帮助命令 help @type(具体要查询的类型,例如help @string)

## 3.SpringBoot整合Redis

![image-20240119185446100](D:/CS/Note/Redis/Redis.assets/image-20240119185446100.png)

![image-20240119185753793](D:/CS/Note/Redis/Redis.assets/image-20240119185753793.png)

### 3.1 Redis配置文件以及依赖引入

#### 3.1.1 依赖引入

![image-20240119204904237](D:/CS/Note/Redis/Redis.assets/image-20240119204904237.png)

#### 3.1.2 配置文件

![image-20240119191109347](D:/CS/Note/Redis/Redis.assets/image-20240119191109347.png)

![image-20240119194058064](D:/CS/Note/Redis/Redis.assets/image-20240119194058064.png)

SpringBoot会为我们自动配置好RedisTemplate然后将其纳入bean管理

### 3.2 基本存入方式

> 序列化之前必须注意：请确保如果您要存入的数据类具有无参数构造函数，并且可以被Jackson库正确地序列化和反序列化。如果您使用的是其他序列化库，相应地调整配置。

![image-20240119191310819](D:/CS/Note/Redis/Redis.assets/image-20240119191310819.png)

![image-20240119191323097](D:/CS/Note/Redis/Redis.assets/image-20240119191323097.png)

> 这是因为SpringData可以接受任何类型的对象，然后将其转成Redis可以处理的字节。Redis对象底层对这些对象的默认处理方式就是JDK的序列化工具ObjectOutputStream

![image-20240119191645235](D:/CS/Note/Redis/Redis.assets/image-20240119191645235.png)

![image-20240119191731868](D:/CS/Note/Redis/Redis.assets/image-20240119191731868.png)

没有自定义序列化工具就会默认走JDK

缺点

* 可读性差
* 内存占用大

### 3.3 String+JSON

`我们希望的是写的是什么就是什么`

1. key一般用：StringRedisSerializer 转成String
2. value一般用：==GenericJackson2JsonRedisSerializer==（RedisTemplate的序列化器） 转成json

~~~java
    @Bean
    public RedisTemplate<String ,Object>redisTemplate(RedisConnectionFactory connectionFactory){
        // 创建RedisTemplate对象
        RedisTemplate<String,Object> template = new RedisTemplate<>();
        // 设置连接工厂
        template.setConnectionFactory(connectionFactory);
        // 创建JSON序列化工具
        GenericJackson2JsonRedisSerializer jsonRedisSerializer =
                new GenericJackson2JsonRedisSerializer();
        // 设置key的序列化
        template.setKeySerializer(RedisSerializer.string());
        template.setHashKeySerializer(RedisSerializer.string());
        // 设置Value的序列化
        template.setValueSerializer(jsonRedisSerializer);
        template.setHashValueSerializer(jsonRedisSerializer);
        // 返回
        return template;
    }
~~~



SpringBoot-web中已经引入了jackson-databind依赖因此我们无需再次引入

~~~java
    @Autowired
    private RedisTemplate<String,Object> redisTemplate;

	@Test
    void testSaveUser(){
        redisTemplate.opsForValue().set("userdemo",new User());
        User o = (User)redisTemplate.opsForValue().get("userdemo");
        System.out.println(o);
    }
~~~

![image-20240119193649345](D:/CS/Note/Redis/Redis.assets/image-20240119193649345.png)

![image-20240119193711573](D:/CS/Note/Redis/Redis.assets/image-20240119193711573.png)

> 存的时候会把我们的对象序列化称为JSON，取得时候在反序列化回来，注意是通过@class标签来反序列化的。（这是自动序列化和自动反序列化的关键核心）

为了在反序列化时知道对象的类型，JSON序列化器会将类的class类型写入JSON结果中，存入Redis，会带来额外的内存开销。

### 3.4 节省内存的存入方法

为了节省内存空间，我们并不会使用JSON序列化器来处理value，而是统一使用String序列化，要求智能存储String类型的key和value。当要存储Java对象时，手动完成对象的序列化和反序列化。

**![image-20240119194546268](D:/CS/Note/Redis/Redis.assets/image-20240119194546268.png)**

> Spring默认提供了一个StringRedisTemplate类，它的Key和Value的序列化方式默认就是String方式。省去了我们自定义RedisTemplate的过程。

因此可以直接注入

~~~java
@SpringBootTest(classes = Application.class)
public class StringRedisTemplateTest {
    @Autowired
    private StringRedisTemplate stringRedisTemplate;
    // JSON工具,可以使用自己熟悉的JSON序列化工具
    // 例如FastJSON
    // 本例我们使用的是jackson的序列化工具即（ObejectMapper）
    private static final ObjectMapper mapper = new ObjectMapper();
    @Test
    void testAStringTemplate(){
        User user = new User();

    }
    @Test
    void testSaveString(){
        stringRedisTemplate.opsForValue().set("SRTDemoForSaveString","StringDemo");
        String srtDemoForSaveString = stringRedisTemplate.opsForValue().get("SRTDemoForSaveString");
        System.out.println(srtDemoForSaveString);
    }
       @Test
    void testSaveObject() throws JsonProcessingException {
        User user = new User();
        String json = mapper.writeValueAsString(user);
        // 写入数据
        stringRedisTemplate.opsForValue().set("SRTDemoForSaveObject",json);
        // 获取数据
        String s = stringRedisTemplate.opsForValue().get("SRTDemoForSaveObject");
        // 手动反序列化
        User user1 = mapper.readValue(s, User.class);
        System.out.println(user1);
    }
}
~~~

哈希操作略有不同

```java
@Test
void testHash() throws JsonProcessingException {
    String s = mapper.writeValueAsString(new User("1", "shelly", "123", "administrator"));
    stringRedisTemplate.opsForHash().put("SRTDemoForSaveHash",
            "username", s);
    Map<Object, Object> srtDemoForSaveHash = stringRedisTemplate.opsForHash().entries("SRTDemoForSaveHash");
    System.out.println(srtDemoForSaveHash.get("username"));
}
```

`推荐使用`，但必须注意，只要涉及到自定义类，必须手动序列化和反序列化

总结：

![image-20240119200558749](D:/CS/Note/Redis/Redis.assets/image-20240119200558749.png)

方案一占内存，方便，但更推荐StringRedisTemplate

## 4.Redis实战1——黑马点评

### 4.1 短信登陆

基于session实现登录

![image-20240119210307421](D:/CS/Note/Redis/Redis.assets/image-20240119210307421.png)

> 每一个请求到达我们的业务中，他都会是一个独立的线程。如果我们没有用ThreadLocal而是直接把这个用户保存到一个本地变量那就可能出现多线程并发修改安全问题。而ThreadLocal会将数据保存到线程内部，在线程内部创建一个map来去保存。每一个线程都有自己独立的存储空间，那么每一个请求来了之后都会有自己的空间，相互之间没有干扰。

~~~java
// 可以帮助我们实现单表增删改查
import com.baomidou.mybatisplus.extension.service.impl.ServiceImpl;

// 第一个参数为Mapper类，第二个参数为实体类
public class ServiceImpl<M extends BaseMapper<T>, T> implements IService<T>
~~~

![image-20240120102816019](D:/CS/Note/Redis/Redis.assets/image-20240120102816019.png)

首先需要实现登录拦截器的业务逻辑

~~~java
package com.hmdp.utils;

import com.hmdp.dto.UserDTO;
import com.hmdp.entity.User;
import jakarta.servlet.http.HttpServletRequest;
import jakarta.servlet.http.HttpServletResponse;
import jakarta.servlet.http.HttpSession;
import org.springframework.web.servlet.HandlerInterceptor;


public class LoginInterceptor implements HandlerInterceptor {

    // 前置拦截器
    @Override
    public boolean preHandle(HttpServletRequest request, HttpServletResponse response, Object handler) throws Exception {
        HttpSession session = request.getSession();
        Object user = session.getAttribute("user");
        if (user == null) {
            response.setStatus(401);
            return false;
        }


        UserHolder.saveUser((UserDTO) user);
        return true;
    }

    // 后置拦截器，用户业务执行完毕销毁相关信息，避免业务泄露
    @Override
    public void afterCompletion(HttpServletRequest request, HttpServletResponse response, Object handler, Exception ex) throws Exception {
        HandlerInterceptor.super.afterCompletion(request, response, handler, ex);
    }
}
~~~

其次需要配置拦截器

~~~java
package com.hmdp.config;

import com.hmdp.utils.LoginInterceptor;
import com.hmdp.utils.RefreshTokenInterceptor;
import jakarta.annotation.Resource;
import org.springframework.context.annotation.Configuration;
import org.springframework.data.redis.core.StringRedisTemplate;
import org.springframework.web.servlet.config.annotation.InterceptorRegistry;
import org.springframework.web.servlet.config.annotation.WebMvcConfigurer;


@Configuration
public class MvcConfig implements WebMvcConfigurer {

    @Resource
    private StringRedisTemplate stringRedisTemplate;

    @Override
    public void addInterceptors(InterceptorRegistry registry) {
        // 登录拦截器，配置直接放行项
        registry.addInterceptor(new LoginInterceptor())
                .excludePathPatterns(
                        "/shop/**",
                        "/voucher/**",
                        "/shop-type/**",
                        "/upload/**",
                        "/blog/hot",
                        "/user/code",
                        "/user/login"
                ).order(1);
        // token刷新的拦截器
        registry.addInterceptor(new RefreshTokenInterceptor(stringRedisTemplate)).addPathPatterns("/**").order(0);
    }
}
~~~

#### 4.1.1 登录信息的保存

最先想到的就是用户成功登录后可以将用户信息存入session中。当需要拦截器需要当前访问接口的User的信息时只需要从session中取出user即可。

~~~java
    @Override
    public Result login(LoginFormDTO loginForm, HttpSession session) {
        String phone = loginForm.getPhone();
        // 1.校验手机号
        if (RegexUtils.isPhoneInvalid(phone)) {
            return Result.fail("手机号格式错误！");
        }
        // 2.校验验证码
        Object cacheCode = session.getAttribute("code");
        String code = loginForm.getCode();
        if (cacheCode == null || !cacheCode.toString().equals(code)) {
            // 3.不一致，报错
            return Result.fail(("验证码错误！"));
        }

        // 4.一致，根据手机号查询用户
        User user = query().eq("phone", phone).one();

        // 5.判断用户是否存在
        if (user == null) {
            // 6.不存在，创建新用户并保存到(不管user必须得存在，不管有没有最后都要有)
            user = createUserWithPhone(phone);
        }
        // 7.保存用户信息到session中
        session.setAttribute("user", BeanUtil.copyProperties(user, UserDTO.class));
        return Result.ok();
    }
~~~



~~~java
public class LoginInterceptor implements HandlerInterceptor {

    // 前置拦截器
    @Override
    public boolean preHandle(HttpServletRequest request, HttpServletResponse response, Object handler) throws Exception {
        HttpSession session = request.getSession();
        Object user = session.getAttribute("user");
        if (user == null) {
            response.setStatus(401);
            return false;
        }


        UserHolder.saveUser((UserDTO) user);
        return true;
    }

    // 后置拦截器，用户业务执行完毕销毁相关信息，避免业务泄露
    @Override
    public void afterCompletion(HttpServletRequest request, HttpServletResponse response, Object handler, Exception ex) throws Exception {
        HandlerInterceptor.super.afterCompletion(request, response, handler, ex);
    }
}
~~~

> 但这么做的问题时显而易见的，当我们需要应对高并发的情形的时候。可能会水平扩展Tomcat，并且做到负载均衡。但显而易见的是如果用户登录的时候请求的是tomcat1，那么用户需要访问自身信息时访问的时tomcat2，那么就会显示用户未登录，这显而易见是不合理的。因此会有集群session共享问题。

![image-20240120115108287](D:/CS/Note/Redis/Redis.assets/image-20240120115108287.png)

那么session的替代方案应该满足：

* 数据共享
* 内存存储（因为session就是内存存储，效率高。不需要和磁盘IO）
* key，value结构（索引快，简单高效方便）

--> ==Redis== 是最优解

1. Redis首先是在Tomcat之外存储，任何一台Tomcat都能访问到Redis。
2. Redis是内存存储，而且性能非常强
3. Key-Value型

![image-20240120115644339](D:/CS/Note/Redis/Redis.assets/image-20240120115644339.png)

#### 4.1.2 基于Redis实现共享sessio登录

> Tomcat内部维护了很多session，当用户浏览器发送请求时，tomcat就会自动为他生成session，并且把sessionid存在cookie中发送给浏览器。浏览器之后每次请求都带着这个cookie里面携带着sessionID，然后取数据就很方便了。

每一个浏览器在向我们的服务器发送请求时都会有一个专属于它的session，因此必须确定每一个不同的手机号来验证时都必须保证Redis中存的key是不同的（有唯一的key），那么就可以直接把手机号作为key。

![image-20240120122820747](D:/CS/Note/Redis/Redis.assets/image-20240120122820747.png)

Key一方面要考虑==唯一性==，一方面要考虑将来取==key==。

![image-20240120123011329](D:/CS/Note/Redis/Redis.assets/image-20240120123011329.png)

![image-20240120123126961](D:/CS/Note/Redis/Redis.assets/image-20240120123126961.png)

随机token就是一个随机字符串，可以通过UUID来生成，保证唯一性。

![image-20240120123220416](D:/CS/Note/Redis/Redis.assets/image-20240120123220416.png)

在原来，我们的登陆凭证是通过session来取出数据的，非常方便，每次通过浏览器传送过来的cookie就可以找到对应的session然后取出相应的对象。

但是现在我们要采用Redis的形式。token是每次浏览器需要携带的，但tomcat并不会帮我们维护token，所以我们必须手动把token返回给前端，客户端再把token保存下来，之后每次请求都要携带token。

![image-20240120123505866](D:/CS/Note/Redis/Redis.assets/image-20240120123505866.png)

总结：

key的要求：

* 唯一性
* 易于携带，方便提取数据

前端代码：

![image-20240120123803324](D:/CS/Note/Redis/Redis.assets/image-20240120123803324.png)

axios请求拦截器，确保每次发送请求都会携带'authorization'这个请求头

![image-20240120123819956](D:/CS/Note/Redis/Redis.assets/image-20240120123819956.png)

~~~java
package com.hmdp.controller;


import com.hmdp.dto.LoginFormDTO;
import com.hmdp.dto.Result;
import com.hmdp.dto.UserDTO;
import com.hmdp.entity.UserInfo;
import com.hmdp.service.IUserInfoService;
import com.hmdp.service.IUserService;
import com.hmdp.utils.UserHolder;
import jakarta.annotation.Resource;
import jakarta.servlet.http.HttpSession;
import lombok.extern.slf4j.Slf4j;
import org.springframework.web.bind.annotation.*;


/**
 * <p>
 * 前端控制器
 * </p>
 *
 * @author 虎哥
 * @since 2021-12-22
 */
@Slf4j
@RestController
@RequestMapping("/user")
public class UserController {

    @Resource
    private IUserService userService;

    @Resourceh
    private IUserInfoService userInfoService;

    /**
     * 发送手机验证码
     */
    @PostMapping("code")
    public Result sendCode(@RequestParam("phone") String phone, HttpSession session) {
        // TODO 发送短信验证码并保存验证码
        return userService.sendCode(phone,session);
    }

    /**
     * 登录功能
     * @param loginForm 登录参数，包含手机号、验证码；或者手机号、密码（JSON风格注解）
     */
    @PostMapping("/login")
    public Result login(@RequestBody LoginFormDTO loginForm, HttpSession session){
        return userService.login(loginForm,session);
    }

    /**
     * 登出功能
     * @return 无
     */
    @PostMapping("/logout")
    public Result logout(){
        // TODO 实现登出功能
        return Result.fail("功能未完成");
    }

    @GetMapping("/me")
    public Result me(){
        UserDTO user = UserHolder.getUser();
        return Result.ok(user);
    }

    @GetMapping("/info/{id}")
    public Result info(@PathVariable("id") Long userId){
        // 查询详情
        UserInfo info = userInfoService.getById(userId);
        if (info == null) {
            // 没有详情，应该是第一次查看详情
            return Result.ok();
        }
        info.setCreateTime(null);
        info.setUpdateTime(null);
        // 返回
        return Result.ok(info);
    }
}
~~~

~~~java
package com.hmdp.config;

import com.hmdp.utils.LoginInterceptor;
import com.hmdp.utils.RefreshTokenInterceptor;
import jakarta.annotation.Resource;
import org.springframework.context.annotation.Configuration;
import org.springframework.data.redis.core.StringRedisTemplate;
import org.springframework.web.servlet.config.annotation.InterceptorRegistry;
import org.springframework.web.servlet.config.annotation.WebMvcConfigurer;


@Configuration
public class MvcConfig implements WebMvcConfigurer {
    @Resource
    private StringRedisTemplate stringRedisTemplate;

    @Override
    public void addInterceptors(InterceptorRegistry registry) {
        // 登录拦截器
        registry.addInterceptor(new LoginInterceptor(stringRedisTemplate))
                .excludePathPatterns(
                        "/shop/**",
                        "/voucher/**",
                        "/shop-type/**",
                        "/upload/**",
                        "/blog/hot",
                        "/user/code",
                        "/user/login"
                ).order(1);
        // token刷新的拦截器
        registry.addInterceptor(new RefreshTokenInterceptor(stringRedisTemplate)).addPathPatterns("/**").order(0);
    }
}
~~~

~~~java
package com.hmdp.utils;

import cn.hutool.core.bean.BeanUtil;
import cn.hutool.core.util.StrUtil;
import com.hmdp.dto.UserDTO;
import jakarta.servlet.http.HttpServletRequest;
import jakarta.servlet.http.HttpServletResponse;
import org.springframework.data.redis.core.StringRedisTemplate;
import org.springframework.stereotype.Component;
import org.springframework.web.servlet.HandlerInterceptor;

import java.util.Map;
import java.util.concurrent.TimeUnit;

import static com.hmdp.utils.RedisConstants.LOGIN_USER_KEY;
import static com.hmdp.utils.RedisConstants.LOGIN_USER_TTL;

@Component
public class LoginInterceptor implements HandlerInterceptor {

    private StringRedisTemplate stringRedisTemplate;

    public LoginInterceptor(StringRedisTemplate stringRedisTemplate) {
        this.stringRedisTemplate = stringRedisTemplate;
    }

    // 前置拦截器
    @Override
    public boolean preHandle(HttpServletRequest request, HttpServletResponse response, Object handler) throws Exception {
//        HttpSession session = request.getSession();
//        Object user = session.getAttribute("user");
        // 获取请求头中的token
        String token = request.getHeader("authorization");
        if (StrUtil.isBlank(token)) {
            // 不存在，拦截，返回401状态码
            response.setStatus(401);
            return false;
        }
//        if (user == null) {
//            response.setStatus(401);
//            return false;
//        }
        // 基于token获取redis中的用户
        Map<Object, Object> userMap = stringRedisTemplate.opsForHash().entries(LOGIN_USER_KEY + token);
        if (userMap.isEmpty()) {
            response.setStatus(401);
            return false;
        }
        UserDTO userDTO = BeanUtil.fillBeanWithMap(userMap, new UserDTO(), false);
        UserHolder.saveUser(userDTO);
        stringRedisTemplate.expire(LOGIN_USER_KEY+token,LOGIN_USER_TTL, TimeUnit.MINUTES);
//        UserHolder.saveUser((UserDTO) user);
        return true;
    }

    // 后置拦截器，用户业务执行完毕销毁相关信息，避免业务泄露
    @Override
    public void afterCompletion(HttpServletRequest request, HttpServletResponse response, Object handler, Exception ex) throws Exception {
        HandlerInterceptor.super.afterCompletion(request, response, handler, ex);
    }
}
~~~

~~~java
package com.hmdp.service.impl;

import cn.hutool.core.bean.BeanUtil;
import cn.hutool.core.bean.copier.CopyOptions;
import cn.hutool.core.lang.UUID;
import cn.hutool.core.util.RandomUtil;
import com.baomidou.mybatisplus.extension.service.impl.ServiceImpl;
import com.hmdp.dto.LoginFormDTO;
import com.hmdp.dto.Result;
import com.hmdp.dto.UserDTO;
import com.hmdp.entity.User;
import com.hmdp.mapper.UserMapper;
import com.hmdp.service.IUserService;
import com.hmdp.utils.RegexUtils;
import jakarta.annotation.Resource;
import jakarta.servlet.http.HttpSession;
import lombok.extern.slf4j.Slf4j;
import org.springframework.data.redis.core.StringRedisTemplate;
import org.springframework.stereotype.Service;
import com.hmdp.utils.SystemConstants;

import java.util.HashMap;
import java.util.Map;
import java.util.Set;
import java.util.concurrent.TimeUnit;

import static cn.hutool.core.lang.Console.log;
import static com.hmdp.utils.RedisConstants.*;

/**
 * <p>
 * 服务实现类
 * </p>
 *
 * @author 虎哥
 * @since 2021-12-22
 */
@Slf4j
@Service
public class UserServiceImpl extends ServiceImpl<UserMapper, User> implements IUserService {
    @Resource
    private StringRedisTemplate stringRedisTemplate;

    @Override
    public Result sendCode(String phone, HttpSession session) {
        if (RegexUtils.isPhoneInvalid(phone)) {
            return Result.fail("手机号格式错误！");
        }
        String code = RandomUtil.randomNumbers(6);
        // 将验证码保存到Redis当中，加个业务前缀显得有层次感。
        // 不然别的业务也存手机号为key的话怎么办？<==> set key value ex 120
        // 常量最好定义一下，免得忘记了之类的
        // stringRedisTemplate.opsForValue().set("login:code" + phone, code,2, TimeUnit.MINUTES);
        stringRedisTemplate.opsForValue().set(LOGIN_CODE_KEY + phone, code, LOGIN_CODE_TTL, TimeUnit.MINUTES);
        // TODO 发送验证码
        log("登录验证码为:{}", code);
        return Result.ok();
    }

    @Override
    public Result login(LoginFormDTO loginForm, HttpSession session) {
        String phone = loginForm.getPhone();
        // 1.校验手机号
        if (RegexUtils.isPhoneInvalid(phone)) {
            return Result.fail("手机号格式错误！");
        }
        // 2.校验验证码
        String cacheCode = stringRedisTemplate.opsForValue().get(LOGIN_CODE_KEY + phone);
        String code = loginForm.getCode();
        if (cacheCode == null || !cacheCode.equals(code)) {
            // 3.不一致，报错
            return Result.fail(("验证码错误！"));
        }

        // 4.一致，根据手机号查询用户
        User user = query().eq("phone", phone).one();

        // 5.判断用户是否存在
        if (user == null) {
            // 6.不存在，创建新用户并保存到(不管user必须得存在，不管有没有最后都要有)
            user = createUserWithPhone(phone);
        }
        // 7.保存用户信息到session中
        // session.setAttribute("user", BeanUtil.copyProperties(user, UserDTO.class));
        // 随机生成TOKEN，作为登录令牌.(true意思是简单的token不带下划线)
        String token = UUID.randomUUID().toString(true);
        log("生成的token为:{}", token);
        // 将User对象转为Hash存储
        UserDTO userDTO = BeanUtil.copyProperties(user, UserDTO.class);
        Map<String, Object> userMap = BeanUtil.beanToMap(userDTO)
//        Set<Map.Entry<String, Object>> entries = userMap.entrySet();
//        entries.forEach(System.out::println);
        // 存储,token也要加个前缀
        stringRedisTemplate.opsForHash().putAll(LOGIN_USER_KEY + token, userMap);
        // session有效期是30分钟
        // 设置有效期
        stringRedisTemplate.expire(LOGIN_USER_KEY + token, LOGIN_USER_TTL, TimeUnit.MINUTES);
        return Result.ok();
    }

    private User createUserWithPhone(String phone) {
        // 创建用户
        User user = new User();
        user.setPhone(phone);
        user.setNickName(SystemConstants.USER_NICK_NAME_PREFIX + RandomUtil.randomString(10));
        save(user);
        return user;
    }
}

~~~



注意此时一定会报错！在我们把获取到的userDTO生成的userMap写入Redis的时候出错了

![image-20240120134702969](D:/CS/Note/Redis/Redis.assets/image-20240120134702969.png)

~~~java
Map<String, Object> userMap = BeanUtil.beanToMap(userDTO)
~~~

这一句中的UserDTO的id字段的类型为Long

也就是说Long类型的数据无法通过StringRedisTemplate存储到Redis当中

原因是上面抛class.java.lang.Long cannot be cast to class.java.lang.String

Long类型无法被强制转换为String类型

要么用笨办法一个一个kv先转换成字符串在放进map

要么：

~~~java
Map<String, Object> userMap = BeanUtil.beanToMap(userDTO, new HashMap<>(),
                CopyOptions.create()
                        .setIgnoreNullValue(true)
                        .setFieldValueEditor((fieldName, fieldValue) -> fieldValue.toString()));
~~~



#### 4.1.3 优化登录拦截器

上述实现方案有一个很明显的问题，登录拦截器只能够拦截需要查询用户状态的请求。如果用户一直访问的是对用户状态没有要求的接口，那么用户可能30分钟后就会被强制踢下线，即使用户一直在进行操作。因此我们需要更好的刷新token的机制。

![image-20240120141629316](D:/CS/Note/Redis/Redis.assets/image-20240120141629316.png)

可以增加一个拦截一切请求的拦截器，如果有token就刷新，没有就不管，任何情况都直接放行。

```java
package com.hmdp.config;

import com.hmdp.utils.LoginInterceptor;
import com.hmdp.utils.RefreshTokenInterceptor;
import jakarta.annotation.Resource;
import org.springframework.context.annotation.Configuration;
import org.springframework.data.redis.core.StringRedisTemplate;
import org.springframework.web.servlet.config.annotation.InterceptorRegistry;
import org.springframework.web.servlet.config.annotation.WebMvcConfigurer;


@Configuration
public class MvcConfig implements WebMvcConfigurer {
    @Resource
    private StringRedisTemplate stringRedisTemplate;

    @Override
    public void addInterceptors(InterceptorRegistry registry) {
        // 登录拦截器
        registry.addInterceptor(new LoginInterceptor(stringRedisTemplate))
                .excludePathPatterns(
                        "/shop/**",
                        "/voucher/**",
                        "/shop-type/**",
                        "/upload/**",
                        "/blog/hot",
                        "/user/code",
                        "/user/login"
                ).order(1);
        // token刷新的拦截器
        registry.addInterceptor(new RefreshTokenInterceptor(stringRedisTemplate)).addPathPatterns("/**").order(0);
    }
}
```

> 注意：RefreshTokenInterceptor拦截器是最先进行的，因此是设置顺序为0，然后需要登录的拦截器顺序设置为1。（根据源码可以知道其实拦截器默认的顺序都是0，谁先被添加谁先被执行，但我们可以手动更改顺序，如上述）

```java
package com.hmdp.utils;

import cn.hutool.core.bean.BeanUtil;
import cn.hutool.core.util.StrUtil;
import com.hmdp.dto.UserDTO;
import jakarta.servlet.http.HttpServletRequest;
import jakarta.servlet.http.HttpServletResponse;
import org.springframework.data.redis.core.StringRedisTemplate;
import org.springframework.web.servlet.HandlerInterceptor;


import java.util.Map;
import java.util.concurrent.TimeUnit;

import static com.hmdp.utils.RedisConstants.LOGIN_USER_KEY;
import static com.hmdp.utils.RedisConstants.LOGIN_USER_TTL;

public class RefreshTokenInterceptor implements HandlerInterceptor {

    private StringRedisTemplate stringRedisTemplate;

    public RefreshTokenInterceptor(StringRedisTemplate stringRedisTemplate) {
        this.stringRedisTemplate = stringRedisTemplate;
    }

    /**
     * 优化拦截器，此拦截器拦截一切请求
     * @param request
     * @param response
     * @param handler
     * @return
     * @throws Exception
     */

    @Override
    public boolean preHandle(HttpServletRequest request, HttpServletResponse response, Object handler) throws Exception {
        // 1.获取请求头中的token
        String token = request.getHeader("authorization");
        // 无需登录也能访问的资源
        if (StrUtil.isBlank(token)) {
            return true;
        }
        // 2.基于TOKEN获取redis中的用户
        // 有token说明登陆过，或正处于登录当中
        String key  = LOGIN_USER_KEY + token;
        Map<Object, Object> userMap = stringRedisTemplate.opsForHash().entries(key);
        // 3.判断用户是否存在
        if (userMap.isEmpty()) {
            return true;
        }
        // 5.将查询到的hash数据转为UserDTO
        UserDTO userDTO = BeanUtil.fillBeanWithMap(userMap, new UserDTO(), false);
        // 6.存在，保存用户信息到 ThreadLocal
        UserHolder.saveUser(userDTO);
        // 7.刷新token有效期
        stringRedisTemplate.expire(key, LOGIN_USER_TTL, TimeUnit.MINUTES);
        // 8.放行
        return true;
    }

    @Override
    public void afterCompletion(HttpServletRequest request, HttpServletResponse response, Object handler, Exception ex) throws Exception {
        // 移除用户
        UserHolder.removeUser();
    }
}
```

```java
package com.hmdp.utils;


import jakarta.servlet.http.HttpServletRequest;
import jakarta.servlet.http.HttpServletResponse;
import org.springframework.data.redis.core.StringRedisTemplate;
import org.springframework.stereotype.Component;
import org.springframework.web.servlet.HandlerInterceptor;



@Component
public class LoginInterceptor implements HandlerInterceptor {

    // 前置拦截器
    @Override
    public boolean preHandle(HttpServletRequest request, HttpServletResponse response, Object handler) throws Exception {
        if (UserHolder.getUser() == null) {
            response.setStatus(401);
            return false;
        }
        return true;
    }
}
```

### 4.2 缓存使用

#### 4.2.1 什么是缓存

**缓存**就是数据交换的缓冲区(乘坐Cache)，就是存贮数据的临时区域，一般读写性能较高。

> CPU就是一个典型的例子。现代CPU的运算速度是相当夸张的，已经达到了一个很高的高度。但是CPU的运算都需要从内存或者磁盘读到数据，写入计算器才能进行运算，但是这种数据读写的能力远远低于运算能力，所以计算机性能受到了限制，因此人们在CPU内部添加了缓存，把CPU会把经常需要读写的一些数据放到CPU的缓存里。

![image-20240120144023906](D:/CS/Note/Redis/Redis.assets/image-20240120144023906.png)

* 浏览器缓存：比如一些网页的静态资源(CSS，JS，图片等等，就可以避免加载某些资源造成网络延迟)
* 应用层缓存：比如利用Redis（减轻数据库压力，同时读写速度飙升）
* 数据库缓存：比如索引

![image-20240120144249858](D:/CS/Note/Redis/Redis.assets/image-20240120144249858.png)

#### 4.2.2 添加Redis缓存

![image-20240121142649039](D:/CS/Note/Redis/Redis.assets/image-20240121142649039.png)

![image-20240121143023100](D:/CS/Note/Redis/Redis.assets/image-20240121143023100.png)



#### 4.2.3 缓存更新策略

![image-20240121191906118](D:/CS/Note/Redis/Redis.assets/image-20240121191906118.png)

这三种策略都不能保证数据一致性的完美无误。

业务场景：

* 低一致性需求：使用内存淘汰机制。例如店铺类型的查询缓存，店铺类型一般都不会变的。
* 高一致性需求：主动更新，并以超时提出作为兜底方案。例如店铺详情查询的缓存。

![image-20240121192313107](D:/CS/Note/Redis/Redis.assets/image-20240121192313107.png)

![image-20240121192644643](D:/CS/Note/Redis/Redis.assets/image-20240121192644643.png)

先删除缓存的正常情况：

![image-20240121192720652](D:/CS/Note/Redis/Redis.assets/image-20240121192720652.png)

异常情况：事实上发生频率还挺高的，因为查和写的速度都非常快！远远的比更新数据库要快，可能数据库还没更新完，我这边就已经查完了。

![image-20240121192751441](D:/CS/Note/Redis/Redis.assets/image-20240121192751441.png)

先操作数据库再删除缓存：

![image-20240121192911680](D:/CS/Note/Redis/Redis.assets/image-20240121192911680.png)

![image-20240121192953714](D:/CS/Note/Redis/Redis.assets/image-20240121192953714.png)

线程1来查缓存的时候刚好缓存失效了，然后这个时候线程2又刚好来更新数据库。

这种情况概率比较低，首先查缓存和查数据库事实上是很快的而且写缓存也很快，这两个操作完成的十分迅速，在微秒的范围内不大可能会在这两个操作之间出现更新数据库的情况。

原则是：==尽量先搞慢的==

![image-20240121193238532](D:/CS/Note/Redis/Redis.assets/image-20240121193238532.png)

注意@Transactional不能回滚Redis但可以回滚数据库例如MySQL

> 这一部分事实上是存在一些问题的，，，要后面好好理解这一小节。

#### 4.2.4 缓存穿透

![image-20240121194432813](D:/CS/Note/Redis/Redis.assets/image-20240121194432813.png)

常见解决方案：

* 缓存空对象
  * 优点：实现简单，维护方便
  * 缺点：
    * 额外的内存消耗（可以在缓存null的时候加一个`TTL`来解决）
    * 可能造成短期的不一致（刚好在在数据库插入相应数据前来了个请求发现缓存里有个空的）。可以通过每次插入新数据到数据库时同步把它丢到Redis当中，来覆盖掉null
* 布隆过滤（但也不是百分之百准确，详情自己了解为什么）：
  * 优点：内存占用较少
  * 缺点：
    * 实现复杂
    * 存在误判可能

![image-20240121194851406](D:/CS/Note/Redis/Redis.assets/image-20240121194851406.png)

![image-20240121202659709](D:/CS/Note/Redis/Redis.assets/image-20240121202659709.png)

#### 4.2.5 缓存雪崩

**缓存雪崩**是指在同一时段`大量的缓存key同时失效`或者`Redis服务宕机`，导致大量请求到达数据库，带来巨大压力。

![image-20240121202812927](D:/CS/Note/Redis/Redis.assets/image-20240121202812927.png)

#### 4.2.6 缓存击穿

**缓存击穿问题**也叫热点Key问题，就是一个被高并发访问并且缓存重建业务比较复杂的key`突然失效`了，无数请求访问会在瞬间给数据库带来巨大的冲击。

![image-20240121203342822](D:/CS/Note/Redis/Redis.assets/image-20240121203342822.png)

常见解决方案：

* 互斥锁
* 逻辑过期

![image-20240121203710142](D:/CS/Note/Redis/Redis.assets/image-20240121203710142.png)

![image-20240121203726561](D:/CS/Note/Redis/Redis.assets/image-20240121203726561.png)

本质上都是在解决重建时期等待的问题。

#### 4.2.7 缓存工具封装
