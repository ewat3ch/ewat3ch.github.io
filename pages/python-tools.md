# Iterators
### iter(<lists|strings|dictionaries|file connections ..>)
```sh
 x=iter(sound)
 print(next(x))
 print(*x)
 ```
```sh
dict1={'one':'1','two': '2', 'three': 3}
for key, value in dict1.items():
    print(key, value)
```
```sh
file=open(file1.txt)
f=iter(file)
```
```sh
a=['one','two']
for index, value in enumerate(a):
    print(index, value)
#optional enumerate(a,start=1)
```
```sh
# define lists
z=['a','b','c']
z1=['a1','b1','c1']
z2=zip(z1,z2)
print(list(z2))
print(*z2)
# or
for i, j in zip(z,z1):
    print(i, j)
```
```sh
for chunk in pd.read_csv('text.csv',chunksize=1000):
    ...
```
## All 
```sh
def cnt(file_csv,size,col_name):
    # Initialize an empty dictionary:
    cntdict = {}
    for chunk in pd.read_csv(file_csv,chunksize=size):
        for entry in chunk[col_name]:
            if entry in cntdict.keys():
                cntdict[entry] += 1
                   cntdict[entry] = 1
         else:
                    cntdict[entry] += 1
    return cntdict
result = cnt(<file name csv,1<int size>,<'column name'>)
print(result)
```

   [PlGa]: <https://github.com/RahulHP/dillinger/blob/master/plugins/googleanalytics/README.md>
