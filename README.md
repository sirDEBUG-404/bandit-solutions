# OverTheWire: Bandit Çözümleri (Level 0 - 33)

Bu depoda, Linux ve Siber Güvenlik temellerini öğrenmek için çözdüğüm OverTheWire Bandit CTF yarışmasının ilk 10 seviye notları yer almaktadır.

---

### Öğrenilen Temel Linux Komutları
- `ls -la`: Gizli dosyalar dahil tüm dosyaları listeler.
- `cd`: Dizinler (klasörler) arasında geçiş yapar.
- `cat`: Dosya içeriğini ekrana yazdırır.
- `find`: Belirli boyutta veya özellikteki dosyaları arar.
- `grep`: Metin veya dosya içinde kelime/desen arar.
- `uniq -u`: Yalnızca tekrar etmeyen (benzersiz) satırları gösterir.
- `base64 -d`: Base64 ile şifrelenmiş veriyi çözer.
- `strings`: Binary (çalıştırılabilir) dosyalardaki okunabilir yazıları çıkarır.

---

### Seviye Özetleri ve Yöntemler

* **Level 0 -> 1:** SSH ile sunucuya bağlanıldı, `readme` dosyası `cat` ile okundu.
* **Level 1 -> 2:** Tire ile başlayan `-` garip isimli dosya `cat ./-` şeklinde okundu.
* **Level 2 -> 3:** Boşluk içeren dosya adı tırnak içine alınarak açıldı.
* **Level 3 -> 4:** Gizli klasördeki gizli dosya `ls -la` kullanılarak bulundu.
* **Level 4 -> 5:** İnsan tarafından okunabilir tek dosya arandı. file./* komutu ile ASCII text olan tek dosya bulundu.
* **Level 5 -> 6:** `find` komutuyla boyutu tam 1033 byte olan dosya tespit edildi.
* **Level 6 -> 7:** Sunucunun tamamında kullanıcı ve grup yetkilerine göre dosya arandı.
* **Level 7 -> 8:** `grep` ile `data.txt` içinde 'millionth' kelimesi aratıldı.
* **Level 8 -> 9:** `sort` ve `uniq -u` birleştirilerek sadece 1 kez tekrar eden parola bulundu. " sort data.txt | uniq -u" kodu ile. sort data.txt alfabetik hale getirir, | ikinci komuta input girdi olarak verir. uniq -u ise benzersiz olanı alır.
* **Level 9 -> 10:** `strings` komutu ile dosyadaki okunabilir metinler çekildi. strings data.txt | grep "==*" komutu. string data.txt okunabilir ASCII kelime ve cumleleri ayırır. grep ise önünde = işareti olan ve bize lazım olanı önümüze getirir.
*  **Level 10 -> 11:** Base64 ile kodlanmış veriler çözüldü. Base64 -d data.txt komutu ile. Base64 komutu veriyi işleyen komuttur. -d ise (decode) verinin şifresini çizer ve ilk haline getirir.

---
*Siber güvenlik yolculuğumdaki ilk adımdır. Güncellenmeye devam edecektir.*
