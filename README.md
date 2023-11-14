# ImageStitching-MPI
## Topologi
## 1. Install MPI
```sh
sudo apt-get install -y mpich-doc mpich
```
```sh
pip install mpi4py
```
output 
![MPI](https://github.com/feliana444/ImageStitching-MPI/assets/145323449/0a4b646e-f73b-4060-9364-49c5f43f4f2a)
## 2. Konfigurasi
### 2.1 Konfigurasi /etc/hosts <br>
cek alamat ip komputer menggunakan perintah `ip a` `if config` `hostname -  I`
**MASTER**
```sh
192.168.135.181 danserver
192.168.135.39 slave
192.168.135.75 slave2
192.168.135.168 slave3
```
**SLAVE**
```sh
192.168.135.181 danserver
192.168.135.39 slave
```
### 2.2 Konfigurasi SSH
    copy id

## 3. Install numpy, imutils dan opencv
### 3.1 numpy
    pip install numpy
### 3.2 imutils
    pip install imutils
### 3.3 opencv
    pip install opencv-python

## 4. Input bahan projek melalui github
```sh
git clone https://github.com/kaliadi/image-Stitching.git\
```

## 5. Copy Seluruh File ke dalam Slave
### 5.1 Copy File
```sh
scp image-Stiching/* mpiuser@slave:/home/mpiuser/
scp image-Stiching/* mpiuser@slave2:/home/mpiuser/
scp image-Stiching/* mpiuser@slave3:/home/mpiuser/
```
### 5.2 Cek Path File pada Master dan Slave
**MASTER**
![master](https://github.com/feliana444/ImageStitching-MPI/assets/145323449/99b8c0c3-d4fe-4737-ab2d-5d7cf5d3c67a)
**SLAVE**
![slave](https://github.com/feliana444/ImageStitching-MPI/assets/145323449/0e2a4f5a-fa9b-430f-ae80-e35f5889f397)

## 6. Program

## Jalankan Image Stitching dengan MPI dan Multinode
### 7.1 Image yang digunakan
![WhatsApp Image 2023-11-14 at 9 08 26 PM](https://github.com/feliana444/ImageStitching-MPI/assets/145323449/683ac523-28c9-4ff9-9ebf-318ba52b3577)
![WhatsApp Image 2023-11-14 at 9 08 26 PM (1)](https://github.com/feliana444/ImageStitching-MPI/assets/145323449/ec3cfff3-5c5d-4488-b932-39097f1245bb)
![WhatsApp Image 2023-11-14 at 9 08 26 PM (2)](https://github.com/feliana444/ImageStitching-MPI/assets/145323449/9b9d8ae3-9f0e-484a-99c6-c485242b49d7)
### 7.2 Waktu Running
![image](https://github.com/feliana444/ImageStitching-MPI/assets/145323449/48f457a7-3f7f-4b11-b85e-529dc3b22d40)
### 7.3 Melihat Hasil Output <br>
Tampilan jika output sudah tersimpan
![image](https://github.com/feliana444/ImageStitching-MPI/assets/145323449/3448576c-6cd8-45e4-80cd-17398e9847ad)
7.4 Output
![image](https://github.com/feliana444/ImageStitching-MPI/assets/145323449/2abddfe2-001c-493a-965d-871f6e180928)
















