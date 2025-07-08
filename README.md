# matrix-pattern
n=int(input("enter the size"))
matrix=[[0]*n for _ in range(n)]
top, left=0,0
right,bottom= n-1,n-1
num=1
while top<=bottom and left<=right:
    for i in range(left, right+1):
        matrix[top][i]=num
        num+=1
    top+=1
    for i in range(top, bottom+1):
        matrix[i][right]=num
        num+=1
    right-=1
    for i in range(right, left-1, -1):
        matrix[bottom][i]=num
    bottom-=1
    for i in range(bottom, top-1,-1):
        matrix[i][left]=num
        num+=1
    left+=1
for row in matrix:
    for val in row:
        print(f"{val:3}",end=' ')
    print()
    
    OUTPUT:
    enter the size 7
  1   2   3   4   5   6   7 
 18  19  20  21  22  23   8 
 17  30  31  32  33  24   9 
 16  29  36  37  34  25  10 
 15  28  36  36  35  26  11 
 14  28  28  28  28  27  12 
 14  14  14  14  14  14  13 
    
