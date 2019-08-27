# Sort the connections from an IP
## Python - This code is written in python to count the number of connections from each IP from the accesss log using dictionary.

```python
count = {}

with open('access.log','r') as fh:

    for item in fh:
    
        ip = item.split()[0]
        if ip not in count:
            
            count[ip] = 1
        else:
            count[ip] = count[ip] + 1
            
for asd in count:
    if count[asd] >= 20:
        print('{:20} {}'.format(asd,count[asd]))
```
