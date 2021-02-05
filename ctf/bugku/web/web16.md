# md5  str_replace  web16
[地址](https://ctf.bugku.com/challenges/detail/id/83.html)
注意题目提示：备份是个好习惯
php -a 以交互式环境启动php，做一些测试

用dirsearch获得index.php.bak

```php
<?php
/**
 * Created by PhpStorm.
 * User: Norse
 * Date: 2017/8/6
 * Time: 20:22
*/
//题目要求 含有key1 和 key2 请求参数， str_replace函数会替换掉key字符串，另外需要md5($key1)==md5($key2) && $key1!==$key2
include_once "flag.php";
ini_set("display_errors", 0);
$str = strstr($_SERVER['REQUEST_URI'], '?');
$str = substr($str,1);
$str = str_replace('key','',$str); //可以双写绕过过  kkeyey1   kkeyey2
parse_str($str);
echo md5($key1);

echo md5($key2);
/**
   1. md5值为0e开头绕过过
*     QNKCDZO
*     240610708
*     s878926199a
*     s155964671a
* 2.payload: /?a[]=1&b[]=2  既可以绕过 == 也可以绕过过===
 * 
 * 
 * 
*/

if(md5($key1) == md5($key2) && $key1 !== $key2){
    echo $flag."取得flag";
}
?>
```



![](vx_images/4754857258473.png =844x)

![](vx_images/2523083825996.png =775x)
![](vx_images/473199615088.png =894x)

![](vx_images/61630940839.png =655x)
可以通过双写绕过过
![](vx_images/5646196889243.png =1017x)