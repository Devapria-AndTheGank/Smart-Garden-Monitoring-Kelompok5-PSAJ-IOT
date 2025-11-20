# Smart-Garden-Monitoring-Kelompok5-PSAJ-IOT
Proyek sistem otomasi smart garden berbasis ESP32 yang dilengkapi sensor suhu, kelembaban udara, dan kelembaban tanah. Data ditampilkan pada OLED dan juga dikirim ke dashboard Blynk.

Fitur

Monitoring suhu, kelembaban udara, dan kelembaban tanah,
Relay otomatis,
Tampilan OLED (logo, sensor, anggota kelompok),
Dashboard Blynk IoT,
Mode manual & otomatis.

Cara Kerja

Relay 2 aktif otomatis ketika suhu ≥ 31°C,
Relay 3 aktif otomatis ketika kelembaban tanah ≤ 20%,
Data dikirim ke Blynk dan ditampilkan di OLED,
Mode manual bisa menyalakan relay via smartphone.

Library yang Dibutuhkan

Blynk,
DHT,
Adafruit SSD1306,
Adafruit GFX.


Wiring (koneksi hardware)

DHT11

Data → pin DHTPIN (pin 4)

VCC → 5V (atau 3.3V tergantung modul), GND → GND


Soil sensor (analog)

Out/A0 → SOIL_PIN (pin 34 pada ESP32)

VCC → 3.3V, GND → GND


OLED (I2C)

SDA → pin 21, SCL → pin 22 (sesuai Wire.begin(21,22))

VCC → 3.3V, GND → GND


Pushbutton (NO) untuk mode OLED

Satu kaki tombol → BUTTON_PIN (pin 13)

Kaki lain tombol → GND

Kenapa: karena di kode pinMode(BUTTON_PIN, INPUT_PULLUP), jadi pin di-pull-up internal (default HIGH). Tekan → hubung ke GND → reading LOW.


Relay module (RELAY1, 2, 3)

IN1 → pin 16 (RELAY1), IN2 → pin 17 (RELAY2), IN3 → pin 18 (RELAY3)

VCC relay module → Adaptor 5V 2A (pastikan ground bersama), GND → GND

Perhatikan: relay module dan ESP32 harus punya GND yang sama.


Anggota

1. Devapria (25)
2. Dwi Aldika (26)
3. Dwi Oktriana (27)
4. Dzawwas N.A (28)
5. Efa Fitriyani (29)
6. Fadlan Mubina (30)

THANKS YOU..
SEMOGA BERMANFAAT!!!
