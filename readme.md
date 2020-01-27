Sistem Fingerprint menggunakan sensor fingerprint DY50 dengan nodemcu

### Prerequisites

Software yg perlu disiapkan

```
Arduino uno
Adafruit-Fingerprint-Sensor-Library : https://github.com/adafruit/Adafruit-Fingerprint-Sensor-Library

```

## Instalasi Hardware

```
RX(fingerprint) ke D7(nodemcu)
TX ke D6
GND ke GND
3v ke 3v
```
## Running test for pendaftaran sidik jari

```
Buka file enroll.ino
Upload ke nodemcu
Buka serial monitor
apabila sensor sudah terkoneksi dengan baik, serial monitor akan menampilkan "found fingerprint sensor"
masukkan ID yang diinginkan (1-127)
letakkan jari ke sensor
setelah ada penjelasan "image taken" "image converted" "remove finger", lepas jari
kemudian akan muncul pada serial monitor "ID yang diinput" "place same finger again"
letakkan jari ke sensor lagi
akan muncul "image converted" "creating for #ID" "prints matched" "ID yang diinput" "stored!"
proses enroll selesai
kemudian bisa melakukan enroll lagi
```
## Running test for baca sidik jari yang tersimpan

```
buka fingerprint.ino
upload ke nodemcu
buka serial monitor
apabila sensor sudah terkoneksi dengan baik, serial monitor akan menampilkan "found fingerprint sensor"
sistem akan menampilkan berapa templates sidik jari yang sudah tersimpan
setelah muncul "waiting for valid finger..", tempelkan jari yang sudah dienroll sebelumnya (sudah terdaftar)
apabila terbaca dengan benar, serial monitor akan menampilkan ID yang tersimpan dengan tingkat ketelitian tertentu.

```
