**SOURCE CODE PRAKTIKUM STRUKTUR DATA**

```python
def quicksort(arr,low,high):
    if(low < high):
        pivot = arr[high]

        i = low
        j = high
        while(i <= j):
            while (arr[i] < pivot):
                i += 1
            while (arr[j] > pivot):
                j -= 1
            if (i <= j):
                arr[i], arr[j] = arr[j], arr[i]
                i += 1
                j -= 1
        quicksort(arr, low, j)
        quicksort(arr, i, high)

terbesar = 0
data = [int(x) for x in input().split()]
quicksort(data,0,len(data)-1)

if (len(data) < 2):
    print(0)
else:
    for i in range(1,len(data)):
        if data[i]-data[i-1] > terbesar:
            terbesar = data[i]-data[i-1]
    print(terbesar)
```
