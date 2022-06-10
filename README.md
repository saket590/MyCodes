# python-nmap_with_https_detect
> python-nmap lib is an excellent lib for binding nmap. <br>
> but it can't detect protocol https by default, it's not so convenient sometime.<br>
> this code add https protocol detection in python-nmap.<br>
## How to use?
### The usage is similar to original python-nmap lib,just a little different in https detection.
```python3
p = scan_result['scan']['127.0.0.1']['tcp']['443']
if p['name'] == 'http' and p['tunnel'] == 'ssl':
    service = 'https'
elif p['name'] == 'ssl' and p['tunnel'] == 'ssl':
    service = 'https'
```
