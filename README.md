# 🛡️ OverTheWire: Bandit Çözümleri (Level 0 - 10)

Bu depoda, Linux ve Siber Güvenlik temellerini öğrenmek için çözdüğüm OverTheWire Bandit CTF yarışmasının ilk 10 seviye notları yer almaktadır.

---

### 🚀 Öğrenilen Temel Linux Komutları
- `ls -la`: Gizli dosyalar dahil tüm dosyaları listeler.
- `cd`: Dizinler (klasörler) arasında geçiş yapar.
- `cat`: Dosya içeriğini ekrana yazdırır.
- `find`: Belirli boyutta veya özellikteki dosyaları arar.
- `grep`: Metin veya dosya içinde kelime/desen arar.
- `uniq -u`: Yalnızca tekrar etmeyen (benzersiz) satırları gösterir.
- `base64 -d`: Base64 ile şifrelenmiş veriyi çözer.
- `strings`: Binary (çalıştırılabilir) dosyalardaki okunabilir yazıları çıkarır.

---

### 📝 Seviye Özetleri ve Yöntemler

* **Level 0 -> 1:** SSH ile sunucuya bağlanıldı, `readme` dosyası `cat` ile okundu.
* **Level 1 -> 2:** Tire ile başlayan `-` garip isimli dosya `cat ./-` şeklinde okundu.
* **Level 2 -> 3:** Boşluk içeren dosya adı tırnak içine alınarak açıldı.
* **Level 3 -> 4:** Gizli klasördeki gizli dosya `ls -la` kullanılarak bulundu.
* **Level 4 -> 5:** İnsan tarafından okunabilir tek dosya arandı.
* **Level 5 -> 6:** `find` komutuyla boyutu tam 1033 byte olan dosya tespit edildi.
* **Level 6 -> 7:** Sunucunun tamamında kullanıcı ve grup yetkilerine göre dosya arandı.
* **Level 7 -> 8:** `grep` ile `data.txt` içinde 'millionth' kelimesi aratıldı.
* **Level 8 -> 9:** `sort` ve `uniq -u` birleştirilerek sadece 1 kez tekrar eden parola bulundu.
* **Level 9 -> 10:** `strings` komutu ile dosyadaki okunabilir metinler çekildi.

---
📌 *Siber güvenlik yolculuğumdaki ilk adımdır. Güncellenmeye devam edecektir.*
