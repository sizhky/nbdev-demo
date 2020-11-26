# Demo Project
> This is solely to explain the steps involved in building a library out of your notebooks and `nbdev`.



1. Make a template out of [this-repo](https://github.optum.com/yreddy31/nbdev-template)
2. Clone it
```bash
$ git clone https://github.optum.com/yreddy31/demo-nbdev
```
3. Modify settings.ini
4. Add your notebooks in nbs folder
5. Build the library
```bash
$ nbdev_build_lib
$ cd nbs && ln -s ../demo . && cd ..
```
6. Test the library
```bash
$ nbdev_test_nbs
```
6. Build the docs
```bash
$ nbdev_build_docs
```
7. Verify the docs are built properly
```bash
$ make docs_serve
```
{% include important.html content='Ensure jekyll is properly built on your machine. This is needed for serving docs.' %}

## How to use

`index.ipynb` should be the notebook that introduces users to your library. 
You just need to add the important code snippets and the docs will be automatically built.

```python
c = Circle(10)
print(f'Area:\t\t{c.area}\nPerimeter:\t{c.perimeter}')
```

    Area:		314.1592653589793
    Perimeter:	62.83185307179586

