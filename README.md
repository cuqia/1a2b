# 1a2b
    from string import digits
 
    from random import randint, choice

    print ("""A一個代表數字正確位置正確，B代表數字正確位置錯誤。直到猜中（即4A0B）為止""")
 
#随机选出4位数

    seeds = "1234567890"

    num1= []

    for i in range(4):

    num1.append(choice(seeds))
  
    num2 = "".join(num1)’

#输入4位数
    num = [] 

    results = []

    Winner = 0

    while Winner == 0:

    num = input('輸入四個數字:')
  
    nA = 0 
  
    nB = 0

#判断数字是否存在以及位置是否正确并计数
  for i in range(4) :
  
    if num[i] in num1 :
    
      if i == num2.find(num[i]) :
      
        nA += 1
        
      else :
      
        nB += 1
        
    if nA == 4:
    
      print ("you win!!")

#当4个数全部正确时跳出迴圈
      Winner = 1
      
    else:
    
      exit
      
    result = '%dA%dB' % (nA, nB)
    
    print (result)
  
