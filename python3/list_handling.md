# Remove empty items in list
```python3
str_list = list(filter(None, str_list))
```
# Create list from file
```python3
with open('myfile','r') as file:
    content = file.read()
    #if on newline:
    content = content.split("\n")
    #if on commas, etc:
    content = content.split(",")
```
