# synchronize dua (ato lebih) folder


Ini rsync dari folder web image ke folder lain  

```
rsync -av /Users/wiwied/Desktop/JPGweb/*px /jpg/ --include="xx" --include="*/" --exclude="*" &&
rsync -av /Users/wiwied/Desktop/PNGweb/*px /png/ --include="xx" --include="*/" --exclude="*"
```

```
rsync -av /Users/wiwied/Desktop/PNGweb/*px png/ && rsync -av /Users/wiwied/Desktop/JPGweb/*px jpg/
```

