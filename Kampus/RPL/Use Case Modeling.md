---
tags:
  - College
  - notes
  - rpl
  - use_case_modeling
---
# Core Elements
![[Pasted image 20231018222603.png]]

# Core Relationships
![[Pasted image 20231018222621.png]]
![[Pasted image 20231018222629.png]]
## Include & Extend
```
Penting banget buat uts dan tugas-tugas
```
### Include
![[Pasted image 20231018222836.png]]
Dari base case ke included case, mengharuskan included case untuk dijalankan ketika menjalankan base case.
Dalam kasus ini log in harus dijalankan setiap kita ingin check balance, withdraw money, atau transfer money.
### Extend
![[Pasted image 20231018222853.png]]
Dari extension case ke base case, artinya kita bisa menjalankan si extension case ketika kita menjalankan base case.
Dalam kasus ini ketika kita return books kita bisa menghitung fines yang harus kita bayarkan tapi tidak wajib kita lakukan.

