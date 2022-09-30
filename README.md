# Binary_Search
def BinarySearch(l,low,high,key):
    while low<=high:
        mid=(low+high)//2
        if l[mid]==key:
            return mid
        elif l[mid]>key:
            high=mid-1
        else:
            low=mid+1
    return -1
l=[]
n=int(input("Enter no of ele:"))
for i in range(n):
    e=int(input())
    l.append(e)
key=int(input("Enter ele to be found:"))
low=0
result=BinarySearch(l,low,n-1,key)
if result==-1:
    print("Element not found")
else:
    print("Element found at:",result)
