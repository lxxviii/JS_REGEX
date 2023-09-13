FSA AYARLAR
İFADE 	      AÇIKLAMA
  i 	      karakter diziliminin karşılaştırılmasında büyük harf / küçük harf ayrımının yapılıp yapılmayacağının tanımlamasında kullanılır.
  g 	      karakter diziliminin tamamının karşılaştırmada kontrol edilip edilmeyeceğini tanımlamada kullanılır.
  m 	      karakter diziliminin birden fazla satırı varsa tüm satırlarının karşılaştırmada kontrol edilip edilmeyeceğini tanımlamada kullanılır.

KONUM BELİRLEYİCİLER (Özel Belirleyiciler var ifade = new RegExp("\\konumBelirleyiciveAranacakIfade") şeklinde uygulanmalıdır) (\ kaçınma karakteri) (\\ konum belirleyici)
İFADE 	      AÇIKLAMA 
  ^ 	      karakter diziliminin başlangıcı ile düzenli ifade arasında bir eşleşme aramak için kullanılır
  $ 	      karakter diziliminin sonu ile düzenli ifade arasında bir eşleşme aramak için kullanılır
  \b 	      düzenli ifadeye uygun olabilecek metin parçalarını, karakter diziliminin içerisindeki kelimelerin başında yada sonunda aramak için kullanılır 
            (boşluk karakterinden sonra yeniden başlar, arama başta olacaksa /b aranacak ifadenin başında, arama sonda olacaksa /b aranacak ifadenin sonunda olur)
  \B 	      düzenli ifadeye uygun olabilecek metin parçalarını, karakter diziliminin içerisindeki kelimelerin içerisinde aramak için kullanılır 
            (boşluk karakterinden sonra yeniden başlar)
  ?= 	      karakter dizilimi içerisindeki belirtilen bir referans değerin önünde düzenli ifade ile eşleşebilecek değerleri aramak için kullanılır
            (var ifade = new RegExp("aranacakIfade(?=aranacakIfadedenSonraGelecekDeger)"))
  ?! 	      Karakter dizilimi içerisindeki belirtilen bir referans değer ile takip edilmeyen değerleri düzenli ifade ile eşleşebilecek değerleri aramak için kullanılır
            (var ifade = new RegExp("aranacakIfade(?=aranacakIfadedenSonraGelmeyecekDeger)"))

NİCELİK BELİRLEYİCİLER
İFADE 	      AÇIKLAMA 
            Karakter diziliminde bulunan değerin;
 {x} 	      x defa tekrarlanmış olması gerektiğini belirtmek için kullanılır. Dizi olarak döndürür.
            Return ederken x kısmını split eder, x miktarı tekrar ediyorsa tekrar miktarı kadar split etmeye devam eder => Number = x;
 {x,} 	    x defa yada daha fazla tekrarlanmış olması gerektiğini belirtmek için kullanılır
            Return ederken x, kadar olduğunu gösterilir, karakter katarı daha uzunsa serinin sonuna kadar gider -Tek Sefer Döner Dizi Oluşturmaz -   => Number = x;
{x,y} 	    en az x defa yada en fazla y defa tekrarlanmış olması gerektiğini belirtmek için kullanılır
            Return karakter katarı daha uzunsa serinin sonuna kadar gider  -Tek Sefer Döner Dizi Oluşturmaz-   => Number = x , y;
  + 	      1 defa yada daha fazla tekrarlanmış olması halinde değeri yakalar, fazlası olması halinde değeri döndürmez, dizi döndürür 
  ? 	      0 defa yada 1 defa tekrarlanmış olması halinde değeri yakalar, fazlası olması halinde değeri döndürmez, dizi döndürür
  * 	      0 defa yada daha fazla tekrarlanmış olması halinde değeri yakalar, dizi döndürür

ÖZEL BELİRLEYİCİLER
İFADE 	      AÇIKLAMA
            Düzenli ifadelerde;
  () 	      grup tanımlamak için kullanılır (g kullanılmazsa | operatöründe aynı döngüler üzerinden iki kere çevirir) 
   \ 	      ardından gelecek olan karakterin özel bir karakter olup olmadığını belirtmek için kullanılır 
  (?:) 	    içerisinde alt grup oluşturmak için kullanılır (g kullanılmazsa | operatöründe aynı döngüler üzerinden iki kere çevirir) - Hafızada yer kaplamaz -

             Karakter diziliminde bulunan değerin;
  [abc] 	   belirtilen karakterlerden herhangi birisi ile eşleşmesi gerektiğini belirtmek için kullanılır (a , b , c birer sorgulanan karakter olmak üzere) /g olursa hepsini sorgular, olmazsa ilk denk geleni döndürür
  [a-z] 	   belirtilen karakterler aralığından herhangi birisi ile eşleşmesi gerektiğini belirtmek için kullanılır
  [^abc] 	   belirtilen karakterlerin dışındaki karakterlerden herhangi birisi ile eşleşmesi gerektiğini belirtmek için kullanılır 
  [^a-z] 	   belirtilen karakterler aralığı dışındaki karakterlerden herhangi birisi ile eşleşmesi gerektiğini belirtmek için kullanılır 
  (x|y) 	   belirtilen x ya da y karakterlerinden herhangi birisi ile eşleşmesi gerektiğini belirtmek için kullanılır 
    .	       yeni satır karakterleri hariç herhangi birisi ile eşleşmesi gerektiğini belirtmek için kullanılır 
   \w 	     harf ve rakamlardan veya _ (alt çizgi) karakterlerinden herhangi birisi ile eşleşmesi gerektiğini belirtmek için kullanılır 
   \W 	     harf ve rakamlardan veya _ (alt çizgi) karakterler dışındaki karakterlerden herhangi birisi ile eşleşmesi gerektiğini belirtmek için kullanılır 
   \d 	     sadece rakam karakterlerinden herhangi birisi ile eşleşmesi gerektiğini belirtmek için kullanılır 
   \D 	     rakam karakterleri dışındaki karakterlerden herhangi birisi ile eşleşmesi gerektiğini belirtmek için kullanılır 
   \s 	     sadece boşluk karakteri ile eşleşmesi gerektiğini belirtmek için kullanılır 
   \S 	     boşluk karakteri dışındaki karakterlerden herhangi birisi ile eşleşmesi gerektiğini belirtmek için kullanılır 
   \0 	     sadece null karakteri ile eşleşmesi gerektiğini belirtmek için kullanılır (\u0000 : 16 Bit Yazım Şekli)
   \n 	     sadece yeni satır karakteri ile eşleşmesi gerektiğini belirtmek için kullanılır  (\u000A : 16 Bit Yazım Şekli)
   \f 	     sadece form besleme karakteri ile eşleşmesi gerektiğini belirtmek için kullanılır (\u000C : 16 Bit Yazım Şekli)
   \r 	     sadece paragraf sonu karakteri ile eşleşmesi gerektiğini belirtmek için kullanılır (\u000D : 16 Bit Yazım Şekli)
   \t 	     sadece yatay sekme (Tab) karakteri ile eşleşmesi gerektiğini belirtmek için kullanılır (\u0009 : 16 Bit Yazım Şekli)
   \v 	     sadece dikey sekme karakteri ile eşleşmesi gerektiğini belirtmek için kullanılır (\u000B : 16 Bit Yazım Şekli)
 \000 	     octal numeral system (sekizlik sayı sistemi) tabanında ASCII (American Standard Code for Information Interchange) (Bilgi Değişimi için Amerikan Standart Kodlama Sistemi) karşılığı olan karakteri ile eşleşmesi gerektiğini belirtmek için kullanılır 
 \x00 	     hexadecimal numeral system (onaltılık sayı sistemi) tabanında ASCII (American Standard Code for Information Interchange) (Bilgi Değişimi için Amerikan Standart Kodlama Sistemi) karşılığı olan karakteri ile eşleşmesi gerektiğini belirtmek için kullanılır 
\u0000 	     16 bit’lik unicode (evrensel kod) formatındaki karşılığı olan karakteri ile eşleşmesi gerektiğini belirtmek için kullanılır

DÜZENLİ İFADELERLE BİRLİKTE KULLANILAN FONKSİYONLAR

global :      '/g' kullanılıp kullanılmadığını kontrol eder.                                              var kontrol = ifade.global //return bool
ignoreCase :  '/i' kullanılıp kullanılmadığını kontrol eder.                                              var kontrol = ifade.ignoreCase //return bool
multiline :   '/m' kullanılıp kullanılmadığını kontrol eder.                                              var kontrol = ifade.multiline //return bool

match()      :                                                                                            var metin = "Örnek Metin";
Aranan dizi işleşmesi durumunda eşleşmeyi sağlayan değişken içeriği/içerikleri değerinden                 var ifade = new RegExp("Bulunacak Değer","olması halinde gim"); // var ifade = /Bulunancak Değer/ ve olması halinde igm  
Yeni bir dizi oluşturarak yeni bir dizi döndürür.                                                         var sonuc = metin.match(ifade); //True-"Bulunacak Değer" //False-null
                                                                                               
test()       : Bulunacak değerin kontrol eder. Return bool                                                var metin = "Örnek Metin"; var kontrol = ifade.test(metin) //return bool                                                                      
input()      : Aranan değerin tüm değerini geriye döndürür. --Aranan ifadesi olmadanda çalışır--          var metin = "Örnek Metin"; var kontrol = ifade.input(metin) //  If-Else ile Check yapılabilir
source()     : Deseni geri döndürür. Return controlValue instance Not Return /gim                         var metin = "Örnek Metin"; var kontrol = ifade.source(metin) // -- 
search()     : Eşleşen ilk düzenli ifadenin başlangıç değerinin indis değerini döndürür.                  var kontrol = metin.search(ifade) return Number
lastIndex()  : search() ile başlayan IndexOf değerinin bittiği yerden sonraki Index değerini döndürür.    var kontrol = metin.lastIndex(ifade) return Number (Tüm Sorgunun çalışması için /g ile sorgulanır)  
                                                                                                          var ifade = new RegExp("script","g"); while(ifade.test(metin) == true) { document.write(sonuc + "<br/>") }

lastMatch    : Aranan değerin son eşleşen değerini döndürür.              (tüm değer için /g kullanılır)  var kontrol = ifade.lastMatch            var ifade = new RegExp("aranan ifade - (|) Or Kullanılabilir -","g"); ifade.test(metin); var sonuc = RegExp.lastMatch;
leftContext  : Aranan değerin solunda kalan tüm değerleri geriye döndürür.(tüm değer için /g kullanılır)  var kontrol = ifade.leftContext          var ifade = new RegExp("aranan ifade - (|) Or Kullanılabilir -","g"); ifade.test(metin); var sonuc = RegExp.leftContext;
rightContext : Aranan değerin sağında kalan tüm değerleri geriye döndürür.(tüm değer için /g kullanılır)  var kontrol = ifade.rightContext         var ifade = new RegExp("aranan ifade - (|) Or Kullanılabilir -","g"); ifade.test(metin); var sonuc = RegExp.rightContext;

replace ()   : Aranan içerik eşleşirse yeni değer oluşturup geriye döndürür.(tüm değer için /g kullanılır)var metin = "Örnek metin"; var ifade = new RegExp("değişecek ifade"); var sonuc = metin.replace (ifade, "değişim sonrasında kullanılacak ifade");
split()      : split() gibi çalışır. Dizi haline getirir. (tüm değer için /g kullanılır)                  var metin = "Örnek metin"; var ifade = new RegExp("yakalanacak ifade","g"); var sonuc = metin.split(ifade);
exec()       : lastIndex(for-in) fonkisyonu gibi çalışır. Yeni dizi geriye döndürür.g yoksa baştan başlar var metin = "Örnek metin"; var ifade = new RegExp("yakalancak ifade", "g"); var sonucBir = ifade.exec(metin); var sonucIki = ifade.exec(metin); 
toString()   : İçeriği String'e çevirerek döndürür
compile()    : Aranan İfadeyi atama yaparak değiştirir
