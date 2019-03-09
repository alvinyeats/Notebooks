# !/bin/bash                                 # 指定shell类型

echo -n "Enter your name:"                   # 参数-n的作用是不换行，echo默认换行
read  name                                   # 把键盘输入放入变量name
echo "hello $name,welcome to my program"     # 显示输入信息
exit 0                                       # 返回一个零退出状态，退出shell程序
