# Enhancement Types
SAP ‘de, orijinal kodu değiştirmeden SAP uygulamalarının standart işlevselliğini geliştirmek için çeşitli teknikler vardır. Bu teknikler, SAP standart programlarına veya uygulamalarına özel mantık veya işlevsellik eklemenizi sağlar. SAP ‘de yaygın olarak kullanılan bazı ABAP geliştirme türleri şunlardır: 

* 1.Enhancement Framework (Geliştirme Noktaları ve Geliştirme Bölümleri): Geliştirme Çerçevesi, SAP standart programlarında veya işlev modüllerinde önceden tanımlanmış noktalarda özel kod eklemenin bir yolunu sağlar. SAP geliştiricileri, standart kodlarında, özel kodunuzu ekleyebileceği kancalar görevi gören "Geliştirme Noktaları" veya "Geliştirme Bölümleri" oluşturur. Geliştirme Çerçevesi, geliştirmeleri yönetmeyi ve etkinleştirmeyi veya devre dışı bırakmayı kolaylaştıran özel kodu kapsamak için içerme yapılarını kullanır. Bu teknik, SAP uygulamalarını özelleştirmek için yaygın olarak kullanılır ve standart kodda yapılan doğrudan değişiklikler 

* 2.Business Add-Ins (BAdIs) İş Eklentileri: SAP standart uygulamalarında önceden tanımlanmış belirli konumlara özel kod eklemenize olanak tanıyan başka bir güçlü geliştirme tekniğidir. BAdI'ler, SAP'nin standart kodunda sağladığı arabirimlerdir ve bu arabirimleri kendi özel mantığınızla uygulayabilmesini sağlar. Bu şekilde, SAP uygulamalarının davranışını yükseltilebilir halde tutarken özelleştirebilirsiniz. BAdI'ler, özel kodu standart koddan ayırmanın bir yolunu sağlayarak SAP sistemlerinizin bakımını ve yükseltilmesini kolaylaştırır. 

* 3.Customer Exit (Müşteri Çıkışı): SAP tarafından çeşitli programlarda sağlanan kullanıcı çıkışlarıdır. Bunlar, SAP standart programlarında belirli noktalara özel mantık veya geliştirmeler eklemenizi sağlayan işlev modülü çıkışlarıdır. Müşteri çıkışlarıyla, iş gereksinimlerinize göre verileri değiştirebilir, çıktıyı geliştirebilir veya ek kontroller gerçekleştirebilirsiniz. BAdI’ler benzer şekilde müşteri çıkışları, özel kodu standart koddan ayırmanın bir yolunu sunarak daha sorunsuz yükseltmeler sağlar. 

* 4.User Exit:=Kullanıcı Çıkışı: SAP standart programlarındaki belirli noktalara özel kod eklemenize izin veren, SAP ‘deki eski bir geliştirme tekniğidir. Müşteri çıkışlarına benzer şekilde çalışırlar ancak bireysel programlara özgüdürler ve BAdI'ler veya Geliştirme Çerçevesi kadar standartlaştırılmamışlardır. Geliştirme Çerçevesi ve BAdI'lerin kullanıma sunulmasıyla, Kullanıcı Çıkışlarının kullanımı bu daha gelişmiş geliştirme teknikleri lehine azaltılmıştır. SAP'de bu geliştirme tekniklerini kullanmak, özelleştirmelerinizin gelecekteki yükseltmelerden ve yamalardan izole edilmesini sağlayarak SAP sisteminizi daha sağlam ve bakım yapılabilir hale getirir. SAP standart işlevselliğini geliştirirken, sistem yükseltmeleri ve bakımı sırasında sorunlara yol açabilecek standart kodda doğrudan değişiklik yapılmasını önlemek için SAP'nin en iyi uygulamalarını takip etmek ve bu geliştirme yöntemlerini kullanmak çok önemlidir.


## Abap Badi Oluşturma Adımları
İhtiyaçları Belirleme: İlk adım olarak, standart SAP işlevselliğini özelleştirmeniz gereken spesifik ihtiyaçları belirlenmelidir. Bu, standart SAP işleyişini değiştirmek veya yeni işlevler eklemek için BADI kullanmanız gerekip gerekmediğini anlamak için önemlidir.
Enhancement Spot Belirleme: Özelleştirmeniz için en uygun yerleri belirlemek için standart SAP kodunu incelenerek ve gerekli olan "Enhancement Spot"ları tanımlanır. Enhancement Spotlar, BADI veya diğer özelleştirme yöntemlerinde kullanılabilir yerleri belirlemek için kullanılan yer tutucu noktalardır.
BADI Oluşturma: Belirlediğiniz Enhancement Spot'u kullanarak BADI oluşturun. Bunu, SAP sisteminde "SE18" veya "SE19" tcode ile oluşturulabilir. Bu adımda, BADI'yi tanımlayacak bir ad ve açıklama belirtmeniz gerekecektir.
BADI İmplementasyon Oluşturma: Oluşturduğunuz BADI ‘ye özel kod eklemek için BADI ‘ye bir veya daha fazla implementasyon eklemeniz gerekir. Bunu, BADI ‘nin tanımında bulunan "Implementasyon" sekmesinde yapabilirsiniz. Implementasyon adı ve açıklaması belirlemeniz ve uygulanacak sınıfı seçmeniz gerekecektir. Bu sınıf, BADI aracılığıyla eklediğiniz özel kodu içerecektir.
Implementasyonlara Kod Eklenmesi: Oluşturduğunuz BADI implementasyonlarının içine istediğiniz özel kodu ekleyin. Bu kod, BADI'nin içinde tanımlanan metotları veya işlevleri içerebilir ve özelleştirilmiş işlevselliği sağlamak için kullanılır.
BADI Implementasyonlarını Aktifleştirme: Eklediğiniz BADI implementasyonlarını aktif hale getirmeniz gerekir, böylece SAP sistemi bunları tanır ve çalıştırır. Bu adımı "SE19" transaksiyon kodu kullanarak yapabilirsiniz.
Böylece, ihtiyaçları belirleme, Enhancement Spot belirleme, BADI oluşturma ve BADI implementasyonlarını oluşturma ve aktifleştirme adımlarını takip ederek SAP ABAP projelerinde BADI kullanmış olursunuz. Bu şekilde, standard SAP işleyişini özelleştirmek için daha esnek ve yönetilebilir bir yöntem elde edebilir.

![image](https://github.com/sumeyyaakbulut/Enhancement_Types_in_SAP/assets/62395974/c62100ce-5585-48ea-8cfd-d2c473ec3e8c)

![image](https://github.com/sumeyyaakbulut/Enhancement_Types_in_SAP/assets/62395974/0e1b257a-848a-4b65-82f0-ee27e3cd0302)

![image](https://github.com/sumeyyaakbulut/Enhancement_Types_in_SAP/assets/62395974/58710a17-935b-4aab-882d-2710286b8fb0)

![image](https://github.com/sumeyyaakbulut/Enhancement_Types_in_SAP/assets/62395974/5f10864d-d85a-437e-8336-02175f98226d)

![image](https://github.com/sumeyyaakbulut/Enhancement_Types_in_SAP/assets/62395974/ef8a3160-033f-481d-b27d-f8b6d5df9a40)

![image](https://github.com/sumeyyaakbulut/Enhancement_Types_in_SAP/assets/62395974/71fe3098-5441-44fc-871b-01ac0c0c1d50)

![image](https://github.com/sumeyyaakbulut/Enhancement_Types_in_SAP/assets/62395974/ba2d7c13-7130-4ee2-9e50-a8a9f228f498)

Yukarıdaki görsellediki birim üretme kipini ve kullanılabilirlik inceleyelim.

## Kullanılabilirlik
### 1.Çoklu Kullanım (Çoklu Uygulama): 
BAdI'ler çoklu kullanımı veya çoklu uygulamaları destekler. Bu, tek bir BAdI tanımının birden fazla uygulamaya sahip olabileceği ve her uygulamanın farklı özel mantık içerebileceği anlamına gelir. Bu esneklik, farklı müşterilerin veya projelerin aynı BAdI'yi kendi özel gereksinimlerine göre kendi benzersiz yöntemleriyle uygulamasına olanak tanır.
Örneğin, SAP'nin bir satış siparişinin işlenmesini geliştirmek için bir BAdI sağladığını varsayalım. SAP kullanan farklı şirketler, satış siparişi işlemeyi kendi iş ihtiyaçlarına göre özelleştirmek için bu BAdI'yi uygulayabilir. Bir şirket, hepsi aynı BAdI'nin farklı uygulamalarını kullanarak, özel kontroller ve doğrulamalar ekleyebilirken, bir diğeri satış siparişini harici bir sistemle entegre edebilir.

### 2.SAP Dahili Uygulamaları: 
Bazı BAdI'lerin SAP tarafından dahili olarak kullanılması amaçlanmıştır. SAP, kendi geliştiricilerinin SAP uygulamalarının standart davranışını geliştirmesine veya değiştirmesine izin vermek için bu BAdI'leri oluşturabilir. Bu BAdI'ler öncelikle SAP'nin dahili kullanımı için olduğundan, belgelenmemiştir veya müşteri kullanımına yönelik değildir.

### 3.Sınırlı Filtre Kullanımı: 
Bazı BAdI'ler "filtre değerleri" veya "filtre kriterleri" ile gelir. Bu filtreler, belirli koşullara veya parametrelere dayalı olarak belirli uygulamaların yürütülmesini kontrol etmenize izin verir. Bir BAdI'de filtreler olduğunda, sistem hangi uygulama(lar)ın yürütüleceğine karar vermeden önce bu filtreleri kontrol eder.
Örneğin, satınalma siparişlerini doğrulamak için bir BAdI olduğunu hayal edin. BAdI, satın alma organizasyonuna dayalı bir filtreye sahip olabilir. Farklı satın alma organizasyonlarının farklı doğrulama gereksinimleri olabilir, bu nedenle her organizasyonun doğrulama mantığı ayrı ayrı uygulanabilir ve sistem, bir satınalma siparişini işlerken yalnızca eşleşen satın alma organizasyonu filtresiyle uygulamayı yürütür.


Özetle, ABAP BAdI'leri çoklu kullanım yeteneği sağlar, yani her biri farklı gereksinimleri karşılayan çoklu uygulamalara sahip olabilirler. Bazı BAdI'ler SAP'nin dahili kullanımına yönelik olabilir ve müşteri kullanımına yönelik olarak belgelenmemiştir. Ek olarak, belirli BAdI'lerde, belirli kriterlere göre hangi uygulamanın yürütüleceğini kontrol etmenize izin veren ve çeşitli koşullara dayalı daha fazla özelleştirme seçeneği sağlayan filtreler olabilir.


## Birim Üretme Kipi
### 1.Yeniden Üreten Birim Yaratma:(Newly Creating Instantiation) 

Interface oluşturalım. Bu interface de attribute olarak gv_val type integer bir değişken tanımlayalım. Method tanımlayalım(zif_demo_badi~display). Metodumuzun tipi instance seçelim.

```cadence
METHOD ZIF_DEMO_BADI~DISPLAY.
GV_VAR = GV_VAR  +1. 
WRITE: '   ' / GV_VAR.
ENDMETHOD.
```

Daha sonra bir program oluşturup aşağıdaki şekilde yazılır ise:
```cadence
DATA: LR_BADI1 TYPE REF TO BADI_NAME.
DATA: LR_BADI2 TYPE REF TO BADI_NAME.

GET BADI LR_BADI1.
GET BADI LR_BADI2.

CALL BADI  LR_BADI1>DISPLAY.
ULINE.
CALL BADI  LR_BADI2>DISPLAY.
```
Programın çıktısı aşağıdaki şekildedir.

	10 
	_____
	10

Bir badi den birden fazla referans alarak oluştulur ise newly creating Instantiation  kullanılır ise ilk badi çağrıldığı zaman ve nesne oluşturulunca bundan sonra her bir badi oluşturulduğu zaman gv_var  program ilk başladığı değer ile başlar .Bir önceki gv_var badi değerinden başlamaz .Çünkü her seferinde yeni bir nesne oluşturdu için programında ilk olarak gv_var ne olarak  tanımlandı ise bundan sonra her oluşturulan badi için de o değer kullanılır.

### 2.Yeniden Kullanılan Birim Üretme

Yukarıdaki örnekle aynı içeriklere sahip içerikler yapılır tek fark kullanabilirlik kısmında yeniden kullananım seçilir ise elimiz de iki badi oldu için ilk gv_var değeri ikinci badinin başlangıç değeri olarak kullanılacaktır.
O yüzden de çıktı:

	10
	______
	20
Olur.

### 3.Bağlama Özgü Örnekleme: (Context-Specific Instantiation)
Bu modda, sistem örnekleri BAdI tanımında belirtilen belirli kriterlere veya bağlama göre gruplandırır. Farklı bağlamlara göre birden çok örnek oluşturulabilir ve her örnek, aynı bağlam içindeki çağrılar arasında paylaşılır.
Kullanım Senaryosu: Örnekleri belirli kriterlere göre gruplamak istediğinizde bu modu kullanın ve her çağrı grubu aynı örnekle çalışmalıdır. Bağlama özgü örnekleme, farklı bağlamlara ait çağrılar için farklı durumları korurken BAdI uygulama durumunu ilgili çağrılar arasında paylaşmanıza olanak tanır.




