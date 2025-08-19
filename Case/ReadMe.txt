1. Karakterleri Hazırlamak

Demon Mode mekaniklerini yapabilmek için tüm karakterlerin benzer özelliklere sahip olması gerekiyordu. Bu yüzden BP_ThirdPersonCharacter blueprint’ini temel aldım ve ondan 4 farklı child karakter oluşturdum.

Bunlardan biri ana karakterimiz, diğer üçü ise AI karakterleri olarak görev yaptı.

2. Karakterleri Yönetmek

Yeni bir PlayerController oluşturdum ve bu controller sayesinde haritadaki tüm karakterleri bir listeye ekledim.

Ana karakter bu listeden çıkarıldı, böylece AI karakterleriyle kolayca çalışabilecektim.

3. Demon Mode’u Aktif Etmek

Q tuşuna basıldığında önce cooldown süresi kontrol ediliyor, sonra ana karakterin canı 30 veya altında mı diye bakılıyor.

Eğer koşullar uygunsa Demon Mode aktif hale geliyor ve ana karakter, listedeki AI karakterlerden biri gibi davranıyor.

4. Demon Mode Süresi

Demon Mode 15 saniye boyunca aktif kalıyor. Bunun için Set Timer by Event kullandım.

Süre dolunca ana karakter tekrar kendi hâline dönüyor ve canı artıyor.

5. Cooldown UI

Bu özelliğin tekrar hemen kullanılmaması için bir cooldown UI yaptım.

Süre dolana kadar Demon Mode tekrar aktifleştirilemiyor.

6. Saldırı Mekanikleri

Ana karakter veya Demon Mode’a geçmiş karakterler animasyonlar eşliğinde saldırıyor.

Saldırılar için Line Trace kullanıldı, böylece düşmanlara isabet eden saldırılar tespit ediliyor.

Mouse sol tuşu ile oyuncu saldırı yapabiliyor.

7. Düşman Sağlık Sistemi

Tüm düşman AI’lara health sistemi eklendi.

Her düşman iki kez hasar aldığında ölüyor.

8. UI Kısımları

Ana menü oluşturuldu.

Tüm düşmanlar öldüğünde “You Win” ekranı, ana karakter öldüğünde “Game Over” ekranı gösteriliyor.

Cooldown ve health sistemi için Progress Bar kullanıldı.

9. Eklenebilecek Özellikler

Her düşmanın kendine özgü saldırı sistemi olabilir (ör. melee, ranged, magic, area attack).

UI geliştirmeleri: Oyuncuya hangi tuşlarla hangi aksiyonu yapması gerektiği daha görsel ve anlaşılır şekilde gösterilebilir.

Combo veya skill sistemi: Ana karakter ve AI karakterler için farklı kombinasyon saldırıları veya özel yetenekler eklenebilir.

Ses ve görsel efektler: Saldırılar ve Demon Mode için ekstra VFX/SFX eklenerek oyun deneyimi zenginleştirilebilir.

-> Unreal Engine 5.4 kullanıldı.