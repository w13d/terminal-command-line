# Command Touch untuk Time Stamp

Dipakai untuk mengubah time-stamp file dan folder sesuai dengan waktu yang diinginkan.

Digabungkan dengan fungsi/command `date` `copy ke clipboard` dan `paste from clipboard`

Step yang dipakai adalah sbb : 
• Ambil waktu dan tanggal (diambil _current time_)
• dimasukkan ke dalam _clipboard_ (copy)
• paste timestamp ke file/folder  target

```
date "+%Y%m%d%H%M" | pbcopy && touch -mt `pbpaste` file

```

