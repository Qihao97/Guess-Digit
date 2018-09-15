# Guess Digit
First program in github.
#!/usr/bin/python3
#-*-conding:UTF-8-*-

import random

number = random.randint(1,100)
guess = 0 
while True:
  num_input = input("请输入一个1到100的整数：")
  guess += 1
  if not num_input.isdigit():
    print("请输入数字！")
  elif int(num_input) < 0 or int(num_input) > 100:
    print("您输入的数字必须介于1到100之间！")
  else:
    if number == int(num_input):
      print("恭喜您，您猜对了，您总共猜了 %d 次。"%guess)
      break
    elif number > int(num_input):
      print("您输入的数字小了！")
    elif number < int(num_input):
      print("您输入的数字大了！")
    else:
      print("系统发生了不可预测的问题，请联系管理人员进行处理！")
