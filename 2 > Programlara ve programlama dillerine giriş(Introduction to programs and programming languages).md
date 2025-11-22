Modern bilgisayarlar inanılmaz derecede hızlıdır ve sürekli olarak daha da hızlanmaktadır. Ancak bilgisayarların bazı önemli kısıtlamaları da vardır: yalnızca sınırlı bir komut kümesini doğal olarak anlayabilirler ve tam olarak ne yapmaları gerektiğinin söylenmesi gerekir.

Bilgisayar programı, bir bilgisayara belirli eylemleri belirli bir sırayla gerçekleştirmesini emreden bir dizi talimattır. Bilgisayar programları genellikle, bilgisayarlar için talimat yazmayı kolaylaştırmak üzere tasarlanmış bir dil olan programlama dilinde yazılır. Her biri farklı bir ihtiyaç kümesine hitap eden birçok farklı programlama dili mevcuttur. Bir program yazma eylemine (ve sanatına) programlama denir. Bu bölümdeki gelecek derslerde C++'da programların nasıl oluşturulacağı hakkında daha detaylı konuşacağız.

Bir bilgisayar, bir bilgisayar programındaki talimatlarda açıklanan eylemleri gerçekleştirdiğinde, programı çalıştırıyor veya yürütüyor deriz. Bir bilgisayar, kendisine talimat verilene kadar bir programı yürütmeye başlamaz. Bu genellikle kullanıcının programı başlatmasını (veya çalıştırmasını veya yürütmesini) gerektirir, ancak programlar başka programlar tarafından da başlatılabilir.

Programlar, bilgisayarı oluşturan fiziksel bileşenlerden oluşan bilgisayarın donanımı üzerinde yürütülür. Tipik bir bilgi işlem cihazında bulunan önemli donanımlar şunlardır:

- Bilgisayarın talimatlarını gerçekten yürüten CPU (İşlemci - merkezi işlem birimi, genellikle bilgisayarın "beyni" olarak adlandırılır).
- Bellek(RAM-ROM...), programlar çalışmadan yada çalışırken veri işlemlerin yapıldığı birimdir.
- Bir kişinin bilgisayarla etkileşime girmesini sağlayan etkileşimli cihazlar (örneğin monitör, dokunmatik ekran, klavye veya fare).
- Bilgisayar kapalıyken bile bilgileri (yüklü programlar dahil) tutan depolama aygıtları (örneğin sabit disk, SSD veya flash bellek).

Buna karşılık, yazılım terimi genel olarak bir sistemdeki donanımda çalıştırılmak üzere tasarlanmış programları ifade eder.

Modern bilişimde, programlar genellikle yalnızca donanımla değil, sistemdeki diğer yazılımlarla (özellikle işletim sistemiyle) da etkileşime girer. Platform terimi, yazılımların çalışması için bir ortam sağlayan uyumlu bir donanım ve yazılım (işletim sistemi, tarayıcı vb.) kümesini ifade eder. Örneğin, "PC" terimi, günlük dilde x86 ailesi bir CPU üzerinde çalışan bir Windows işletim sisteminden oluşan platformu ifade etmek için kullanılır.

Platformlar genellikle üzerlerinde çalışan programlar için faydalı hizmetler sunar. Örneğin, bir masaüstü uygulaması işletim sisteminden kendisine bir miktar boş bellek vermesini, orada bir dosya oluşturmasını veya bir ses çalmasını isteyebilir. Çalışan programın bunun nasıl kolaylaştırıldığını bilmesi gerekmez. Bir program platform tarafından sağlanan yetenekleri veya hizmetleri kullanıyorsa, o platforma bağımlı hale gelir ve değiştirilmeden diğer platformlarda çalıştırılamaz. Bir platformdan diğerine kolayca aktarılabilen bir programa taşınabilir program denir. Bir programı farklı bir platformda çalışacak şekilde değiştirme işlemine ise taşıma (porting) denir.

Programlardan bahsettiğimize göre, şimdi programlama dillerine geçelim. Bu sadece bir tarih dersi değil, aynı zamanda gelecek derslerde karşımıza çıkacak terminolojiyi de tanıtacağız.

## Makine Dili

Bir bilgisayarın işlemcisi C++'ı anlayamaz. İşlemciler yalnızca makine dilinde (veya makine kodunda) yazılmış talimatları işleyebilir. Belirli bir işlemcinin anlayabileceği tüm olası makine dili talimatları kümesine komut seti denir.

İşte bir makine dili talimatı örneği: ```10110000 01100001```.

Her komut, CPU tarafından "bu iki sayıyı karşılaştır" veya "bu sayıyı şu bellek konumuna kopyala" gibi çok özel bir görevi yerine getiren bir komut olarak algılanır. Bilgisayarlar ilk icat edildiğinde, programcılar programları doğrudan makine dilinde yazmak zorundaydı ve bu çok zor ve zaman alıcı bir işti.

Bu talimatların nasıl düzenlendiği ve yorumlandığı bu eğitim dizisinin kapsamı dışındadır, ancak birkaç noktaya dikkat çekmekte fayda var.

İlk olarak, her talimat 1'ler ve 0'lardan oluşan bir diziden oluşur. Her bir 0 veya 1, ikili basamak veya kısaca bit olarak adlandırılır. Bir makine dili talimatındaki bit sayısı değişir; örneğin, bazı CPU'lar her zaman 32 bit uzunluğundaki talimatları işlerken, bazı diğer CPU'lar (kullanıyor olabileceğiniz x86 ailesindekiler gibi) değişken uzunlukta olabilen talimatlara sahiptir.

İkincisi, uyumlu CPU ailelerinin her birinin (örneğin x86, Arm64) kendi makine dili vardır ve bu makine dili, diğer CPU ailelerinin makine dilleriyle uyumlu değildir. Bu, bir CPU ailesi için yazılmış makine dili programlarının farklı bir CPU ailesindeki CPU'larda çalıştırılamayacağı anlamına gelir!

> ### Önerilen İçerik
> Bir "CPU ailesi" resmi olarak "komut seti mimarisi" (kısaca "ISA") olarak adlandırılır. Wikipedia'da farklı [CPU ailelerinin bir listesi](https://en.wikipedia.org/wiki/Comparison_of_instruction_set_architectures#Instruction_sets) bulunmaktadır.

## Assembly Dili

Makine dili talimatları (örneğin ```10110000 01100001```) bir CPU için idealdir, ancak insanların anlaması zordur. Programlar (en azından tarihsel olarak) insanlar tarafından yazıldığı ve yönetildiği için, programlama dillerinin insan ihtiyaçları göz önünde bulundurularak tasarlanması mantıklıdır.

Bir derleme dili (kısaca "assembly" olarak da adlandırılır), özünde daha anlaşılır bir makine dili gibi çalışan bir programlama dilidir. Yukarıdakiyle aynı talimatın x86 derleme dilindeki hali şöyledir: ```mov al, 0x61```.

> ### Opsiyonel Okuma
> Bu talimat, assembly dilini makine dilinden daha okunabilir kılan birçok özelliği göstermektedir.

> - İşlem (talimatların ne yaptığı) kısa bir anımsatıcıyla (genellikle 3-5 harfli bir ad) tanımlanır. mov, bitleri bir konumdan diğerine kopyalayan bir işlem olan "taşı" için bir anımsatıcı olduğu kolayca anlaşılabilir.
> - Kayıtlara (CPU'nun bir parçası olan hızlı bellek konumları) bir isimle erişilir. al, x86 CPU'daki belirli bir kaydın adıdır.
> - Sayılar daha kullanışlı bir biçimde belirtilebilir. Assembly dilleri genellikle hem ondalık sayıları (örneğin 97) hem de onaltılık sayıları (örneğin 0x61) destekler.

> mov al, 0x61 komutunun onaltılık sayı 0x61'i al CPU kaydına kopyaladığını anlamak oldukça kolaydır.

İşlemciler assembly dilini anlamadığından, assembly programlarının çalıştırılabilmesi için makine diline çevrilmesi gerekir. Bu çeviri, assembly adı verilen bir program tarafından yapılır. Her assembly dili talimatı genellikle eşdeğer bir makine dili talimatını yansıtacak şekilde tasarlandığından, çeviri süreci genellikle basittir.

Tıpkı her CPU ailesinin kendi makine dili olduğu gibi, her CPU ailesinin de kendi assembly dili vardır (bu dil, aynı CPU ailesi için makine diline dönüştürülmek üzere tasarlanmıştır). Bu, birçok farklı assembly dili olduğu anlamına gelir. Kavramsal olarak benzer olsalar da, farklı assembly dilleri farklı talimatları destekler, farklı adlandırma kuralları kullanır vb.

