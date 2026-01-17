# 🍎 Hackintosh – Dell Inspiron 2-in-1 7425 (AMD Ryzen)

EFI được tinh chỉnh cho **Dell Inspiron 2-in-1 7425 (Ryzen 5 5625U)**,  
đạt mức **Native FULL cho sử dụng hằng ngày**,  
**ngoại trừ AirDrop & Microphone** do **giới hạn phần cứng Intel AC7260**.

---

## 💻 Thông tin máy
- 🖥️ **Model:** Dell Inspiron 2-in-1 7425  
- 🧠 **CPU:** AMD Ryzen 5 5625U  
- 🎮 **GPU:** AMD Radeon Vega 7 (iGPU)  
- 📡 **Wi-Fi / Bluetooth:** Intel Dual Band Wireless-AC 7260  
- ✋ **Touchscreen:** Có  
- 🚀 **Bootloader:** OpenCore  
- 🍏 **macOS:** Monterey / Ventura / Sonoma  

---

## ✅ Tình trạng hoạt động

### 🟢 Working
- 🧠 CPU Ryzen 5 5625U (power management ổn định)
- 🎮 GPU Vega 7 (QE/CI đầy đủ, UI mượt)
- 🖥️ Màn hình + Touchscreen
- 🔊 Speaker
- 🎧 Jack tai nghe 3.5mm
- 📡 Wi-Fi Intel AC7260 (sau khi patch OCLP)
- 🔵 Bluetooth (chuột, bàn phím, tai nghe)
- 📷 Webcam
- ⌨️ Bàn phím
- 🖱️ Touchpad (đa điểm, gesture)
- 🔋 Pin & Power Management
- 🌙 Sleep / Wake
- 🔌 USB 2.0 / 3.0
- 🔆 Điều chỉnh độ sáng & phím FN
- ☁️ iCloud / App Store / iMessage (SMBIOS hợp lệ)

### 🟡 Partial
- 🔵 Bluetooth Audio (độ trễ nhẹ)
- 🎞️ DRM (Netflix 1080p, không 4K)

### 🔴 Not Working
- ❌ AirDrop / Handoff / Continuity
- ❌ Microphone (Mic)

> ℹ️ Lưu ý: Đây là **giới hạn phần cứng**, không phải lỗi EFI.

---

## 📡 Wi-Fi Intel AC7260 – **BẮT BUỘC PATCH BẰNG OCLP**

Card **Intel AC7260** không hoạt động native hoàn toàn trên macOS mới.  
➡️ **BẮT BUỘC phải sử dụng OpenCore Legacy Patcher (OCLP)** để Wi-Fi hoạt động ổn định.

### 🧩 Kext sử dụng
- `itlwm.kext` *(hoặc AirportItlwm – tùy macOS)*
- `IntelBluetoothFirmware.kext`
- `BlueToolFixup.kext`

### 🛠️ Patch bằng OCLP
1. 🚀 Boot vào macOS
2. 🧰 Mở **OpenCore Legacy Patcher**
3. 🧩 Chọn **Post-Install Root Patch**
4. ✅ Áp dụng **Legacy Wi-Fi / Networking Framework**
5. 🔄 Reboot

⚠️ Sau mỗi lần **update macOS → cần patch lại bằng OCLP**  
📌 OCLP **chỉ dùng để patch Wi-Fi**, **không dùng để boot**  
➡️ Bootloader chính vẫn là **OpenCore EFI**

---

## 🎤 Microphone
- ❌ Microphone không hoạt động native
- ✅ Speaker & jack tai nghe vẫn hoạt động

### 🔧 Giải pháp thay thế
- 🎧 Tai nghe Bluetooth
- 🎙️ USB Sound Card / USB Micro

---

## 📤 AirDrop
- ❌ Intel AC7260 **không hỗ trợ AirDrop trên macOS**
- ❌ Không thể fake bằng kext hay OCLP

### 🔁 Giải pháp thay thế
- ☁️ iCloud Drive
- 🖧 SMB / LAN
- 💾 USB
- 📲 Nearby Share

---




