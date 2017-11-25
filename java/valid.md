

@Null	限制只能为null
@NotNull	限制必须不为null
@AssertFalse	限制必须为false
@AssertTrue	限制必须为true
@DecimalMax(value)	限制必须为一个不大于指定值的数字
@DecimalMin(value)	限制必须为一个不小于指定值的数字
@Digits(integer,fraction)	限制必须为一个小数，且整数部分的位数不能超过integer，小数部分的位数不能超过fraction
@Future	限制必须是一个将来的日期
@Max(value)	限制必须为一个不大于指定值的数字
@Min(value)	限制必须为一个不小于指定值的数字
@Past	限制必须是一个过去的日期
@Pattern(value)	限制必须符合指定的正则表达式
@Size(max,min)	限制字符长度必须在min到max之间
@Past	验证注解的元素值（日期类型）比当前时间早
@NotEmpty	验证注解的元素值不为null且不为空（字符串长度不为0、集合大小不为0）
@NotBlank	验证注解的元素值不为空（不为null、去除首位空格后长度为0），不同于@NotEmpty，@NotBlank只应用于字符串且在比较时会去除字符串的空格
@Email	验证注解的元素值是Email，也可以通过正则表达式和flag指定自定义的email格式

@ScriptAssert  如果需要校验的业务逻辑比较复杂，简单的@NotBlank，@Min注解已经无法满足需求了，这时可以使用@ScriptAssert来指定进行校验的方法，通过方法来进行复杂业务逻辑的校验，然后返回true或false来表明是否校验成功。例如下面的例子：
~~~java
    //通过script 属性指定进行校验的方法，传递校验的参数，  
    @ScriptAssert(lang="javascript",script="com.learn.validate.domain.Student.checkParams(_this.name,_this.age,_this.classes)" messgae="")  
    public class Student {  
     private String name;  
     private int age;  
     private String classess;  
     //注意进行校验的方法要写成静态方法，否则会出现   
     //TypeError: xxx is not a function 的错误  
     public static boolean checkParams(String name,int age,String classes) {  
      if(name!=null&&age>8&classes!=null){  
       return true;  
      }else{  
       return false;  
      }  
    }  
    }
~~~



@Pattern(regexp="^[a-zA-Z0-9]+$",message="{account.username.space}")
@Pattern(regexp="^(AF|AX|SY|TW|TC|UZ|VU|VE|VN|VG|VI|WF|EH|YE|ZM|ZW)$",message="invalid code")
private String countryCode;
@Size(min=3,max=20,message="{account.username.size}")
