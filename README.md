# As we are unknown about constarin and it is clearly written input output is in our hand
# So considering 0<N<100
list1 = []
for i in range(2,100000):
 for j in range(2, i):
 if i % j == 0:
 break
 else:
 list1.append(i)
list2=[]
for i in list1:
 rev = 0
 e = i
 while i > 0:
 c = i % 10
 rev = rev * 10 + c
 i = i // 10
 if e == rev:
 list2=list2+[e]
while True:
 z=input("Do you want to find prime palindrome number then press yes to find and no 
to exit: ")
 if z=="yes":
 nth= int(input("Enter number(0<n<100): "))
 print(list2[nth-1],"is nth prime palindrome number")
 elif z=="no":
 exit()
 else:
 print("restart")
