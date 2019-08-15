# Şans Oyunları İstatistikleri
LotoHUB Android uygulamam için yazdığım JSON dosyalarından verileri alan, sayıların çıkma frekansı ve son görülmesini hesaplayarak .json dosyası üreten bir python single-file

## Algoritma

Tüm algoritma iki fonksiyon üzerine kurulmuştur, FetchDrawDates ve fetchDraw.

fetchDrawDates, verilen oyunun çekiliş tarihlerini halihazırdaki json dosyası üzerinden alır.
fetchDraw, verilen oyun ve tarihi parametre alarak ilgili sonuç json dosyasına erişir. 

Her bir oyunun kendine ait bir fonksiyonu oluşturulmuştur.
Bu fonksiyonlarda, fetchDrawDates ile alınamayan eski tarihlerin kayıtlı istatistikleri ilk değer olarak eklenmiştir.
-Örneğin: Verileri barındıran noktada Sayısal Loto'nun ilk çekilişi 2018 yılında gözükmektedir. Ancak Sayısal Loto 1996'dan beri oynatılmakta, verileri 2002'den beri internet ortamında paylaşılmaktadır. 2018 öncesi veriler, başka kaynaklardan bulundu.

## Nasıl Çalıştırılır

Dosyada calcSuperStatistics() metodu ile Süper Loto istatistikleri çalıştırılmaktadır.
İstediğiniz şans oyunu istatistiklerini, ilgili fonksiyonu çalıştırarak elde debilirsiniz.
