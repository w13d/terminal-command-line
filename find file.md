#mencari file dengan perintah baris (command line)
#terminal OSX

```
find . -name 'fileA*.jpg' -type f -delete
```

  >> . artinya mencari di lokasi kerja (working directory)  
  >> -name menentukan nama file yang dicari  
  >> -name bisa lebih dari satu ( -name 'x' -name 'y' )  
  >> -name bisa menggunakan * atau wild card yg mempunyai arti "segalanya" mirip seperti regex  
  >> bisa menggunakan fungsi operator -or / -o untuk "atau"   
  >> bisa menggunakan fungsi operator & untuk "dan"  
  
  >> -type adalah argumen untuk menentukan hal yg dicari  
  
  >> f adalah parameter yg menunjukkan kalo yg dicari adalah file (bukan folder/directory, links, blocks, etc)  
  
  >> -delete adalah perintah untuk menghapus  
  
```
find -L /Volumes/mac_shared_drive/ \(-path \*/1600*/50-3017*_F.* -o -path \*/1600*/88-0010*_F.* \) -exec cp {} . \;
```

  // find -L maksudnya mencarinya termasuk di lokasi asalnya Symbolik Link.  
  // -path maksudnya mencari dgn menentukan path/link lokasi folder/directory  
  // seperti contoh di atas, argumen -path ini bisa menggunakan * wild card juga  
  // mencari di beberapa lokasi sekaligus bisa dimasukkan dalam kurung.  
  // kurung ato bracket harus di-escape dnegan backslash  
  // -exec maksudnya adalah perintah selanjutnya setelah menemukan yg dimaksudkan  
  // cp adalah perintah copy  
  // {} mewakili semua yang telah ditemukan oleh perintah find  
  // . merujuk pada lokasi tujuan, kemana harus meng-copy semua yg telah ditemukan  
  // perintah ini harus ditutup dengan titik coma ( ; ) dan sebelumnya harus di-escape dengan backslash.  

```
find /Users/wiwied/Desktop/PNGweb/ -name '*.png' -type f -delete && find /Users/wiwied/Desktop/JPGweb/ -name '*.jpg' -type f -delete
```
  


