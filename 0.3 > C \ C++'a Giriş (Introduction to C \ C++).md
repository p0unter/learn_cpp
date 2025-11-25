### C++'dan önce C vardı.
C dili, 1972 yılında Dennis Ritchie tarafından Bell Telephone laboratuvarlarında, öncelikle bir sistem programlama dili (işletim sistemleri yazmak için kullanılan bir dil) olarak geliştirilmiştir. Ritchie'nin temel hedefleri, derlemesi kolay, belleğe verimli erişim sağlayan, verimli kod üreten ve kendi kendine yeten (diğer programlara bağımlı olmayan) minimalist bir dil üretmekti. Yüksek seviyeli bir dil olan C, programcılara çok fazla kontrol sağlarken, geliştiricilerin farklı platformlarda çalıştırılabilen programlar yazabilmelerini sağlamak için tasarlanmıştır.

C, o kadar verimli ve esnek bir dil haline geldi ki, 1973 yılında Ritchie ve Ken Thompson, Unix işletim sisteminin çoğunu C kullanarak yeniden yazdılar. Önceki işletim sistemlerinin çoğu assembler dilinde yazılmıştı. Yalnızca belirli CPU'larda çalışabilen programlar üreten assembler dilinden farklı olarak, C mükemmel bir taşınabilirliğe sahiptir, bu da Unix'in birçok farklı bilgisayar türünde kolayca yeniden derlenebilmesini ve hızla benimsenmesini sağlamıştır. C ve Unix'in kaderi birbirine bağlıydı ve C'nin popülaritesi, kısmen Unix'in bir işletim sistemi olarak başarısına bağlıydı.

1978 yılında Brian Kernighan ve Dennis Ritchie, “The C Programming Language” adlı bir kitap yayınladı. Yazarların soyadlarından esinlenerek K&R olarak bilinen bu kitap, dil için gayri resmi bir spesifikasyon sağladı ve fiili bir standart haline geldi. Maksimum taşınabilirlik gerektiğinde, programcılar K&R'deki önerilere bağlı kalırlardı, çünkü o dönemde çoğu derleyici K&R standartlarına göre uygulanıyordu.

1983 yılında, Amerikan Ulusal Standartlar Enstitüsü (the American National Standards Institute - ANSI) C dili için resmi bir standart oluşturmak üzere bir komite kurdu. 1989 yılında (komiteler oldukça uğraştılar), çalışmaları tamamlayarak C89 standardını yayınladılar; bu standart daha çok ANSI C olarak bilinir. 1990 yılında Uluslararası Standartlar Örgütü (the International Organization for Standardization -ISO) ANSI C'yi (birkaç küçük değişiklikle) kabul etti. C'nin bu sürümü C90 olarak biliniyordu. Derleyiciler sonunda ANSI C/C90 ile uyumlu hale geldi ve maksimum taşınabilirlik isteyen programlar bu standarda göre kodlandı.

1999 yılında, ISO komitesi gayri resmi olarak C99 olarak adlandırılan C dilinin yeni bir sürümünü yayınladı. C99, derleyicilere uzantı olarak eklenmiş veya C++'da uygulanmış birçok özelliği benimsedi.

---
### C++
C++ (telaffuz: “see plus plus”), 1979 yılında Bell Labs'ta Bjarne Stroustrup tarafından C dilinin bir uzantısı olarak geliştirilmiştir. C++, C diline birçok yeni özellik ekler ve belki de en iyi şekilde C'nin bir üst kümesi olarak düşünülebilir, ancak bu tam olarak doğru değildir (çünkü C99, C++'da bulunmayan birkaç özellik getirmiştir). C++'ın C'ye göre en önemli yeniliği, nesne yönelimli programlamayı desteklemesidir. “Nesne”nin ne olduğu ve geleneksel programlama yöntemlerinden nasıl farklı olduğu konusuna ise sonraki bölümlerde değineceğiz.

C++, 1998 yılında ISO komitesi tarafından standartlaştırılmıştır. Bu, ISO standartlar komitesinin C++ dilinin resmi tanımını içeren bir belgeyi (standartlar belgesi - standards document olarak adlandırılır) onayladığı anlamına gelir. Standartlaştırmanın amacı, C++ kodunun farklı derleyiciler ve platformlarda tutarlı bir şekilde çalışmasını sağlamaktır.

2003 yılında dilde küçük bir güncelleme yayınlandı (gayri resmi olarak C++03 olarak adlandırıldı).

O zamandan bu yana C++ diline beş büyük güncelleme (gayri resmi olarak C++11, C++14, C++17, C++20 ve C++23 olarak adlandırılır) yapılmış ve her biri ek işlevler eklemiştir. Özellikle C++11, çok sayıda yeni özellik eklemiştir ve yaygın olarak dilin yeni temel sürümü olarak kabul edilmektedir. Dilin gelecekteki güncellemeleri yaklaşık üç yılda bir yapılması bekleniyordu.

Onaylanmış standartların resmi adı karmaşık olduğundan (C++20'nin resmi adı ISO/IEC 14882:2020'dir), standartlar geleneksel olarak yayınlandığı (veya yayınlanması beklenen) yılın son iki rakamını içeren gayri resmi adlarla anılır. Örneğin, C++20, 2020 yılında yayınlanan dil sürümünü ifade eder.

---
### C ve C++'ın Felsefesi
C ve C++'ın temel tasarım felsefesi, “programcıya güven” olarak özetlenebilir - bu hem harika hem de tehlikelidir. C++, programcıya istediğini yapmak için yüksek derecede özgürlük sağlamak üzere tasarlanmıştır. Ancak bu, dilin genellikle mantıksız şeyler yapmanı engellemeyeceği anlamına da gelir, çünkü bunu anlamadığın bir nedenden dolayı yaptığını varsayar. Yeni programcılar, farkında olmadan düşebilecekleri pek çok tuzağa sahiptir. Bu, C/C++'da yapmamanız gerekenleri bilmenin, yapmanız gerekenleri bilmek kadar önemli olmasının başlıca nedenlerinden biridir.

> ### S: C++ ne konuda iyidir?
> C++, yüksek performans ve bellek ve diğer kaynaklar üzerinde hassas kontrolün gerekli olduğu durumlarda mükemmeldir. C++'ın mükemmel performans göstereceği birkaç uygulama türü şunlardır:
>
> - Video oyunları
> - Gerçek zamanlı sistemler/Real-time systems  (örneğin ulaşım, üretim vb. için)
> - Yüksek performanslı finansal uygulamalar (örneğin, yüksek frekanslı ticaret)
> - Grafik uygulamaları ve simülasyonlar
> - Verimlilik / ofis uygulamaları
> - Gömülü yazılım
> - Ses ve video işleme
> - Yapay zeka (Artificial Intelligence - AI) ve sinir ağları
>
> C++ ayrıca, geliştirme sürelerini önemli ölçüde kısaltabilen çok sayıda yüksek kaliteli üçüncü taraf kütüphaneye sahiptir.

> ### S: C++ ölmek(bitmek) üzere değil mi?
> Hayır. Anketler, C++'ın en popüler ikinci veya üçüncü derlenmiş dil olduğunu (Java ve bazen C#'ın ardından, C'nin hemen önünde) ve genel olarak en popüler beşinci veya altıncı dil olduğunu (HTML, SQL ve shell scripting dilleri hariç) tutarlı bir şekilde göstermektedir.
> 
> C++ is one of the most popular languages for learning to code, owing to the abundance of teaching resources, the large community, and the number of college courses that teach it.
>
> Üç yılda bir yapılan dil güncellemeleri, çok sayıda kullanışlı üçüncü taraf kütüphanesi ve popüler video oyun endüstrisindeki hakimiyeti ile C++ gelişmeye devam ediyor.

> ### S: Bu dersleri yapmadan önce C dilini bilmem gerekir mi?
> Hayır! C++ ile başlamak tamamen uygundur ve size bu süreçte bilmeniz gereken her şeyi (kaçınmanız gereken tuzaklar dahil) öğreteceğiz.
>
> C++'ı öğrendikten sonra, ihtiyacınız olursa standart C'yi öğrenmek oldukça kolay olacaktır. Günümüzde C, çoğunlukla niş kullanım alanlarında kullanılmaktadır: gömülü cihazlarda çalışan kodlar, yalnızca C ile arayüz oluşturabilen diğer dillerle etkileşim kurmanız gerektiğinde vb. Diğer çoğu durumda C++ kullanılması önerilir.
