# How to contribute
## On python:
Use tabs (set to 4 spaces)
Avoid importing whole module, just import the funcs within it
```python
from os import getcwd
def pathnow():
	return('Current path is '+
		getcwd())
print(pathnow())
```
End all files with:
```python
#main
if __name__ == '__main__':
	with open('..\\path\\to-a\\json\\fileA.json', 'rt', -1) as read:
		data = json.load(read)
	main()
else:
    with open('path\\to-a\\json\\fileA.json', 'rt', -1) as read:
        data = json.load(read)
```
Also, define the `main()`
