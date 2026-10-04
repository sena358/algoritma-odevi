# Kullanıcı Giriş Akışı

## Projenin Amacı

Bu projede kullanıcıların e-posta ve şifre ile sisteme giriş yapma sürecini gösteren bir akış diyagramı hazırladım. Giriş sırasında bilgilerin boş, doğru veya yanlış olması gibi farklı durumlar kontrol ediliyor. Üç kez yanlış giriş yapılması durumunda ise hesap kilitleniyor.

## Algoritmanın Çalışma Mantığı

- İlk olarak hesabın kilitli olup olmadığı kontrol edilir.
- Hesap kilitliyse kullanıcı giriş yapamaz.
- Hesap kilitli değilse kullanıcıdan e-posta ve şifre bilgileri alınır.
- E-posta veya şifre boş bırakılırsa kullanıcıya uyarı verilir ve bilgiler tekrar istenir.
- Alanların boş bırakılması başarısız giriş olarak sayılmaz.
- E-posta ve şifre doğruysa giriş başarılı olur.
- Bilgiler yanlışsa başarısız giriş sayacı 1 artırılır.
- Başarısız giriş sayısı 3'e ulaşmadıysa kullanıcı tekrar giriş yapabilir.
- 3 kez yanlış giriş yapılırsa hesap geçici olarak kilitlenir.

## Akış Diyagramı

Kullanıcı giriş sisteminin akış diyagramı aşağıda yer almaktadır.

![Akış Diyagramı](flowchart.png)

## Test Senaryoları

| Senaryo | Beklenen Sonuç |
|---|---|
| Hesap zaten kilitli | Kullanıcının giriş yapması engellenir |
| E-posta veya şifre boş | Uyarı verilir, sayaç artmaz |
| Bilgiler doğru | Giriş başarılı olur |
| Bilgiler yanlış | Başarısız giriş sayacı 1 artar |
| 3 kez yanlış giriş | Hesap geçici olarak kilitlenir |

## Algoritmayı Hazırlarken Dikkat Ettiklerim

Yanlış girişleri takip edebilmek için bir sayaç kullandım ve başlangıç değerini 0 olarak belirledim. E-posta veya şifrenin boş bırakılmasını yanlış giriş olarak saymadım. Bilgiler yanlış girildiğinde sayaç artıyor ve kullanıcı tekrar deneyebiliyor. Sayaç 3'e ulaştığında ise hesap kilitleniyor.

Akış diyagramında kullanıcıdan bilgi alınan, kontrol yapılan ve sonuç gösterilen adımları birbirinden ayırarak giriş sürecinin daha anlaşılır olmasını amaçladım.

