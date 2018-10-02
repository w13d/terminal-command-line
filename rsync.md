# synchronize dua (ato lebih) folder


Ini rsync dari folder web image ke folder lain  

```
rsync -av /Users/wiwied/Desktop/JPGweb/ /jpg/ --include="xx" --include="*px/" --exclude="*" &&
rsync -av /Users/wiwied/Desktop/PNGweb/ /png/ --include="xx" --include="*px/" --exclude="*"
```

`&&` : jika dipakai, maka baris selanjutnya hanya akan dieksekusi setelah perintah sebelumnya telah selesai dijalankan  
  
```
rsync -av /Users/wiwied/Desktop/PNGweb/*px png/ && rsync -av /Users/wiwied/Desktop/JPGweb/*px jpg/
```
  
Parameter -av keterangannya:  
`-a` : archive mode  
`-v` : verbose   
`-u` : --update  : skip files that are newer on the receiver  
       --inplace : update destination files in-place  
       --append  : append data onto shorter files  
`-d` : cuma copy directory/foldernya aja, konten diabaikan  
  
  
```
rsync -av [folder asal] [folder tujuan] --include="[file]" --"include="[folder/]" --exclude="[semua/all/*]"
```
  
Rsync akan membuat folder secara otomatis di folder tujuan  
meskipun tidak ada eksisting folder  

