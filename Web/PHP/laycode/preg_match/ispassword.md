# PHP 正则匹配 6 到 16 位字符组合(且只能为数字、字母、下划线)

- [PHP 正则匹配 6 到 16 位字符组合(且只能为数字、字母、下划线) - thekingofreturn - 博客园](https://www.cnblogs.com/thekingofreturn/archive/2014/03/29/3632678.html)

## 创建数组

```php
<?php
/**
* php正则验证密码规则
* 只允许 数字、字母、下划线
* 最短6位、最长16位
* 搜集整理：www.jbxue.com
*/
function ispassword($str) {
 if (preg_match('/^[_0-9a-z]{6,16}$/i',$str)){
  return true;
 }else {
  return false;
 }
}
$password = 'abcde@';
if(ispassword($password)) {
 echo '符合';
}else {
 echo '不符合';
}
//output  不符合

echo '<br>';
$password = 'abcdeasdas_1324';
if(ispassword($password)) {
 echo '符合';
}else {
 echo '不符合';
}
//output  符合
?>

```
