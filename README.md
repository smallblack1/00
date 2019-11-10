ID=input('请输入十八位身份证号码: ')
if len(ID)==18:
  print("你的身份证号码是 "+ID)
else:
  print("错误的身份证号码")
  
ID_add=ID[0:6]
ID_birth=ID[6:14]
ID_sex=ID[14:17]
ID_check=ID[17]
  
#ID_add是身份证中的区域代码，如果有一个行政区划代码字典，就可以用获取大致地址#
  
year=ID_birth[0:4]
moon=ID_birth[4:6]
day=ID_birth[6:8]
print("生日: "+year+'年'+moon+'月'+day+'日')
  
if int(ID_sex)%2==0:
  print('性别：女')
else:
  print('性别：男')
  
    
#此部分应为错误判断，如果错误就不应有上面的输出，如何实现？#
W=[7,9,10,5,8,4,2,1,6,3,7,9,10,5,8,4,2]
ID_num=[18,17,16,15,14,13,12,11,10,9,8,7,6,5,4,3,2]
ID_CHECK=['1','0','X','9','8','7','6','5','4','3','2']
ID_aXw=0
for i in range(len(W)):
   
  ID_aXw=ID_aXw+int(ID[i])*W[i]
   
ID_Check=ID_aXw%11
if ID_check==ID_CHECK[ID_Check]:
  print('正确的身份证号码')
else:
  print('错误的身份证号码')
