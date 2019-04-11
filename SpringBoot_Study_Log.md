###springboot学习
###springboot中@Controller与@RestController的区别
> 官方文档：
@RestController is a stereotype annotation that combines @ResponseBody and @Controller.

意思是：@RestController 是一个直接模式：是  @ResponseBody 和 @Controller的结合

- 如果只是使用`@RestController`注解Controller层，则Controller中的方法无法返回`jsp页面`，配置的视图解析器InternalResourceViewResolver不起作用，返回的内容就是Return 里的内容;

*例如：*

``` java
@RequestMapping("/login")
 public String goodBye(String name) {
        return "login";
    }
```
将会输出的是：login（return里的内容）

- 如果需要返回到指定页面，则需要用 @Controller配合视图解析器InternalResourceViewResolver才行。
- 如果需要返回JSON，XML或自定义mediaType内容到页面，则需要在对应的方法上加上@ResponseBody注解。

**适用的解决办法：**

``` java
/**
* 使用ModleAndView 将其转换
* 似的试图解析器解析
*/
@RequestMapping("/login")
    public ModelAndView login(){
        ModelAndView mv = new ModelAndView("login");
        return mv;
    }
```