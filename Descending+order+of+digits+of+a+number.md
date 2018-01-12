

```python
'''
Your task is to make a function that can take any non-negative integer as a argument and return it with its digits in descending order. Essentially, rearrange the digits to create the highest possible number.

Examples:
Input: 21445 Output: 54421

Input: 145263 Output: 654321

Input: 1254859723 Output: 9875543221
'''

def Descending_Order(x):
    #Bust a move right here
    if x >=0:
        l1 = []
        while x != 0:
            l1.append(x%10)
            x = int(x/10)
        list1 = sorted(l1, key=lambda e: int(e), reverse=True)
        print("list1",list1)
        number = 0
        for i in range(0,len(list1)):
            number =number*10 + list1[i]
            #del list1[0]
        return number

print("Desc",Descending_Order(1012))



```

    list1 [2, 1, 1, 0]
    Desc 2110
    


```python
# one line solution
def Descending_Order(num):
    return int("".join(sorted(str(num), reverse=True)))
Descending_Order(1543)
```




    5431


