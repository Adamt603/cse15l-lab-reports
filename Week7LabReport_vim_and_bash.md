# Week 7 Part 1: Using vim

---

## In DocSearchServer.java, change the name of the start parameter of getFiles, and all of its uses, to instead be called base.

```vim DocSearchServer.java```
- opens DocSearchServer.java in vim
```:%s/start/base<Enter>:w```
- Find each occurrence of 'base' (in all lines), and replace it with 'start'.