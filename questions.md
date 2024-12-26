# Sorular ve Cevaplar

Bu dosyada, Java/Spring mülakatlarında karşılaşılmış sorular ve cevapları yer almaktadır. Soruların üzerine tıklayarak cevapları görebilirsiniz.

---

<details>
  <summary><strong>1. JDK, JRE ve JVM nedir? Farkları nelerdir?</strong></summary>

  - **JDK (Java Development Kit):** Java uygulamaları geliştirmek için gereken araçları ve kütüphaneleri içerir. JRE ve ek araçları kapsar.  
  - **JRE (Java Runtime Environment):** Java uygulamalarını çalıştırmak için gereken ortamdır. JVM ve standart sınıf kütüphanelerini içerir.  
  - **JVM (Java Virtual Machine):** Java kodunu makine koduna dönüştürüp çalıştıran sanal makinedir. JVM, platform bağımsızlığı sağlar.

  **Farklar:**
  - JDK, geliştirme araçlarını ve çalıştırma ortamını içerir.
  - JRE, yalnızca çalıştırma ortamıdır.
  - JVM, JRE'nin bir parçasıdır ve kodun platformdan bağımsız çalışmasını sağlar.

</details>

<details>
  <summary><strong>2. Java'da String ve StringBuilder arasındaki fark nedir?</strong></summary>

  - **String:** Immutable'dır, yani değiştirilemez. Her değişiklik yeni bir String nesnesi oluşturur.  
  - **StringBuilder:** Mutable'dır, yani mevcut nesne üzerinde değişiklik yapılabilir. Performans açısından daha verimlidir.

</details>

<details>
  <summary><strong>3. equals() ve == operatörünün farkları nelerdir?</strong></summary>

  - **==:** Referansları karşılaştırır, yani iki nesnenin aynı bellek adresini işaret edip etmediğine bakar.  
  - **equals():** Genellikle nesnelerin içeriklerini karşılaştırmak için kullanılır (ör. String'lerde içerik karşılaştırması yapar).

</details>

<details>
  <summary><strong>4. String sınıfı neden değişmez (immutable) olarak tasarlanmıştır?</strong></summary>

  - **Güvenlik:** String'in içeriği değiştirilemediği için güvenlidir.  
  - **Performans:** Immutable nesneler hashCode'u bir kez hesaplar ve tekrar kullanır.  
  - **Thread-Safety:** String nesneleri değişmez olduğu için çoklu iş parçacıkları arasında güvenle paylaşılabilir.

</details>

<details>
  <summary><strong>5. Abstract sınıf nedir?</strong></summary>

  - **Abstract sınıf**, soyut metotlar (gövdesiz) ve gövdeli metotlar içerebilen bir sınıf türüdür.  
  - Alt sınıflar tarafından miras alınarak tamamlanmak üzere tasarlanır.

</details>

<details>
  <summary><strong>6. Abstract sınıfların constructor'ı olur mu?</strong></summary>

  - Evet, abstract sınıfların constructor'ı olabilir. Ancak abstract sınıflar doğrudan örneklendirilemez, constructor yalnızca alt sınıflar tarafından çağrılır.

</details>

<details>
  <summary><strong>Java'da final anahtar kelimesi nedir? Ne için kullanırız?</strong></summary>

  - **final** bir değişkenin değerinin değiştirilemez olduğunu belirtir.  
  - **final** bir metodun override edilmesini engeller.  
  - **final** bir sınıfın miras alınmasını önler.

</details>

<details>
  <summary><strong>7. Stack ve Heap memory arasındaki fark nedir?</strong></summary>

  - **Stack Memory:** Küçük boyutlu, hızlı ve metod çağrıları için kullanılır. Yerel değişkenler burada saklanır.  
  - **Heap Memory:** Daha büyük boyutlu, dinamik olarak nesnelerin saklandığı alan.

</details>

<details>
  <summary><strong>8. Idempotence nedir?</strong></summary>

  - **Idempotence**, bir işlemin birden fazla kez uygulanmasının aynı sonucu vermesi durumudur.  
  - Örneğin: HTTP GET ve DELETE istekleri genellikle idempotenttir.

</details>

<details>
  <summary><strong>9. Java JIT compiler nedir?</strong></summary>

  - **Just-In-Time (JIT) Compiler**, bytecode'u çalışma zamanında makine koduna çevirerek performansı artırır.  
  - Bu işlem, tekrar eden kodları optimize etmek için kullanılır.

</details>

<details>
  <summary><strong>10. Double check locking nedir?</strong></summary>

  - **Double-check locking**, thread-safe singleton oluşturma tekniğidir. Aynı nesnenin birden fazla kez oluşturulmasını engeller.

</details>

<details>
  <summary><strong>11. Functional Interface nedir? Interface ile arasındaki fark nedir?</strong></summary>

  - **Functional Interface**, yalnızca bir abstract metoda sahip bir arayüzdür.  
  - Functional Interface'ler, lambda ifadeleriyle kullanılabilir.  
  - Diğer arayüzler birden fazla abstract metoda sahip olabilir.

</details>

<details>
  <summary><strong>12. Interface'lerde içi dolu metot yazabilir miyiz?</strong></summary>

  - Evet, Java 8'den itibaren `default` ve `static` anahtar kelimeleri kullanılarak içi dolu metot yazılabilir.

</details>

<details>
  <summary><strong>13. try-with-resources nedir? Hiç kullandın mı?</strong></summary>

  - **try-with-resources**, kaynakların (ör. dosya, veritabanı bağlantıları) otomatik olarak kapatılmasını sağlayan bir yapıdır.  
  - Kapatılabilir sınıfların `AutoCloseable` arayüzünü implement etmesi gerekir.

</details>

<details>
  <summary><strong>14. Checked ve Unchecked Exception'ların farkı nedir?</strong></summary>

  - **Checked Exception:** Derleme zamanında (compile time) kontrol edilen istisnalardır. Kodda try-catch bloğunda yakalanmaları veya metot imzasında `throws` ile belirtilmeleri gerekir. Örnek: `IOException`, `SQLException`.
  - **Unchecked Exception:** Çalışma zamanında (runtime) oluşan istisnalardır. Try-catch bloğunda yakalanmaları zorunlu değildir. Örnek: `NullPointerException`, `ArrayIndexOutOfBoundsException`.

</details>

<details>
  <summary><strong>15. SOLID prensiplerinden bahseder misin?</strong></summary>

  - **S**ingle Responsibility Principle (SRP): Bir sınıfın yalnızca bir sorumluluğu (veya bir amacı) olmalıdır.
  - **O**pen/Closed Principle: Sınıflar genişletilmeye açık, ancak değiştirmeye kapalı olmalıdır.
  - **L**iskov Substitution Principle: Alt sınıflar, üst sınıflarının yerine kullanılabilir olmalıdır.
  - **I**nterface Segregation Principle: Kullanıcılar gereksiz metotlara bağımlı olmamalıdır, arayüzler spesifik olmalıdır.
  - **D**ependency Inversion Principle: Yüksek seviyeli modüller, düşük seviyeli modüllere bağımlı olmamalıdır. Her ikisi de bir soyutlamaya bağımlı olmalıdır.

</details>

<details>
  <summary><strong>16. Spring ile Spring Boot farkı nedir?</strong></summary>

  - **Spring:** Bir Java framework'üdür ve uygulama geliştirme için temel araçlar sağlar. Yapılandırma işlemleri manuel olarak yapılır (XML veya Annotation tabanlı).
  - **Spring Boot:** Spring Framework üzerine kurulmuş bir projedir. Otomatik yapılandırma (Auto-Configuration) özelliği sağlar, bağımlılık yönetimini kolaylaştırır ve gömülü sunucular (embedded servers) içerir. Spring Boot ile daha hızlı bir şekilde uygulama geliştirilir.

</details>

<details>
  <summary><strong>17. Bean nedir? Niye oluşturulur? Bahseder misin?</strong></summary>

  - **Bean**, Spring IoC (Inversion of Control) container tarafından yönetilen bir nesnedir.  
  - Uygulama içinde bağımlılık yönetimi ve yeniden kullanılabilirlik sağlamak için oluşturulur.  
  - Spring, Bean'leri anotasyonlar (ör. `@Component`, `@Service`) veya XML tabanlı yapılandırmalarla yönetir.

</details>

<details>
  <summary><strong>18. Spring Bean'lerini nasıl inject ediyorsun? Birkaç yöntemi var, onlardan da bahseder misin?</strong></summary>

  - **Constructor Injection:** Bağımlılıklar, sınıfın constructor'ı aracılığıyla atanır.  
  - **Setter Injection:** Bağımlılıklar, setter metotları kullanılarak atanır.  
  - **Field Injection:** `@Autowired` anotasyonu doğrudan sınıf değişkenlerinde kullanılır (tavsiye edilmez, test edilebilirliği düşürür).  
</details>

<details>
  <summary><strong>19. @Component ve @Service anotasyonlarının farkı nedir?</strong></summary>

  - **@Component:** Genel bir Spring Bean tanımlayıcısıdır. Herhangi bir bileşen (component) için kullanılabilir.  
  - **@Service:** Daha spesifik bir anotasyondur. İş mantığı (business logic) içeren sınıflar için kullanılır.  
  - Teknik olarak işlevsellik farkı yoktur, ancak kodun okunabilirliğini artırır.

</details>

<details>
  <summary><strong>20. Servlet nedir? Daha önce duymuş muydun?</strong></summary>

  - **Servlet**, Java'nın web tabanlı uygulamalar geliştirmek için sunduğu bir API'dir.  
  - HTTP isteklerini işler ve dinamik içerikler (ör. HTML, JSON) döndürür.  
  - Servlet'ler genellikle Spring MVC'de DispatcherServlet gibi yapılarda soyutlanmıştır.

</details>

<details>
  <summary><strong>@Transactional anotasyonu nedir?</strong></summary>

  - **@Transactional**, Spring'de işlemleri (transactions) yönetmek için kullanılan bir anotasyondur.  
  - Veritabanı işlemlerinde `commit` ve `rollback` yönetimini sağlar.  
  - Metot veya sınıf düzeyinde uygulanabilir.

</details>

<details>
  <summary><strong>@Transactional propagation type'lardan REQUIRED ile REQUIRED_NEW farkını biliyor musun?</strong></summary>

  - **REQUIRED:** Mevcut bir transaction varsa onu kullanır, yoksa yeni bir transaction oluşturur.  
  - **REQUIRED_NEW:** Her zaman yeni bir transaction oluşturur, mevcut transaction'ı askıya alır.

</details>

<details>
  <summary><strong>Hibernate nedir?</strong></summary>

  - **Hibernate**, Java için bir ORM (Object-Relational Mapping) aracıdır. Veritabanı işlemlerini nesne bazlı bir yaklaşımla gerçekleştirmeyi sağlar.  

</details>

<details>
  <summary><strong>Spring Security'den bahseder misin? Projeye nasıl ekliyoruz ve eklediğimizde neler oluyor?</strong></summary>

  - **Spring Security**, uygulamalar için kimlik doğrulama (authentication) ve yetkilendirme (authorization) sağlar.  
  - Spring Security eklendiğinde, varsayılan olarak temel bir güvenlik yapılandırması aktif olur (ör. HTTP Basic Authentication).  
  - Özelleştirmek için `SecurityFilterChain` veya `WebSecurityConfigurerAdapter` kullanılır.

</details>

<details>
  <summary><strong>Thread Safety nedir? Nasıl sağlanır?</strong></summary>

  - **Thread Safety**, birden fazla thread'in aynı anda bir nesneye erişirken tutarsızlıklara neden olmamasıdır.  
  - Thread Safety sağlamak için şu yöntemler kullanılabilir:
    - **volatile** anahtar kelimesini kullanarak sağlayabiliriz fakat bu sadece visibility problemine çözüm olur.
    - **Synchronized** blok veya metotlar kullanabiliriz.  
    - **Immutable Objects** kullanımı.  
    - **ReentratLock** kullanarak.
    - **wait & notify** metotlarını kullanarak.

</details>

<details>
  <summary><strong>Elimizde bir milyon tane Integer türünde sayı var. Kullanıcı bir sayı girdiğinde (örneğin 10), bu sayının listede kaç kez geçtiğini döndüren bir yapı oluşturmak istiyoruz. Örneğin, 10 sayısı 3 kez tekrar ediyorsa sonuç 3, hiç geçmiyorsa sonuç 0 olacak. Bu problemi hangi collection ile çözerdiniz?</strong></summary>

  **Cevap: HashMap**

  - **HashMap** tercih edilir çünkü:
    - Anahtar (key) olarak sayıyı, değer (value) olarak tekrar sayısını saklayabilir.
    - **O(1)** zaman karmaşıklığı ile hızlı ekleme ve arama işlemi sağlar.
    - TreeMap de kullanılabilir, ancak **O(log n)** zaman karmaşıklığı nedeniyle HashMap kadar hızlı değildir.

</details>


<details>
  <summary><strong>@PreAuthorize anotasyonu nedir?</strong></summary>

  - **@PreAuthorize**, Spring Security'de metod seviyesinde yetkilendirme kontrolü yapmak için kullanılan bir anotasyondur.  
  - Metot çağrılmadan önce, kullanıcının belirtilen yetkilere sahip olup olmadığını kontrol eder.  
  - Örneğin:
    - `@PreAuthorize("hasRole('ADMIN')")`: Yalnızca ADMIN rolüne sahip kullanıcılar bu metodu çağırabilir.
    - `@PreAuthorize("#user.id == authentication.principal.id")`: Kullanıcı bazlı kontrol yapılabilir.

</details>

<details>
  <summary><strong>Microservice mimarisinde iki servis var, bunlar birbiriyle iletişim halinde ve bir servis çöktü. Ne olur? Ne yaparsın?</strong></summary>

  - **Durum:** Bir servis çöktüğünde, diğer servis ona bağımlıysa istekler başarısız olur. Bu, sistemin tamamının etkilenmesine neden olabilir. Dağıtık bir sistemde CAP teorimine uygun yapı kurulmalıdır. Buradaki Partiton Tolerance'a uyarsak bu sorunları en aza indiririz.
  
  - **Ne yapılır?**
    - **Circuit Breaker (Devre Kesici) Kullanımı:** Çöken servise yapılan istekler belirli bir süreliğine durdurulur. Ör: Netflix Hystrix, Resilience4j.
    - **Fallback Mekanizması:** Çöken servise alternatif bir cevap döndürmek veya kullanıcıya uygun bir hata mesajı göstermek için kullanılır.
    - **Retry Mekanizması:** Servis tekrar aktif olduğunda işlemleri denemek için kullanılır.
    - **Asenkron İletişim:** Servisler arasındaki bağımlılığı azaltmak için mesajlaşma kuyrukları (RabbitMQ, Kafka) kullanılabilir.

</details>

<details>
  <summary><strong>Optimistic ve Pessimistic Locking nedir?</strong></summary>

  **Detaylı bilgi için Medium yazımı inceleyebilirsiniz: [Hibernate Optimistic ve Pessimistic Locking Nedir?](https://medium.com/@yunusemrenalbant/hibernate-optimistic-ve-pessimistic-locking-nedir-9429c422ccbd)**

</details>

<details>
  <summary><strong>Microservice projesinde bir servis yavaşladı. Response time yükseldi ve sistemi yavaşlattı. Ne yaparsın?</strong></summary>

  - **Durum:** Yavaşlayan bir servis tüm sistemi etkileyebilir, çünkü diğer servisler ona bağımlı olabilir.

  - **Ne yapılır?**
    - Servisin performansını izlemek için monitoring araçları (Prometheus, Grafana, ELK Stack) kullanılır.
    - Yavaşlayan servis için belirli bir zaman sınırı (timeout) koyulur.
    - Yavaşlayan servise yapılan istekler bir süre kesilir ve fallback mekanizması devreye alınır.
    - Yükü dengelemek için yük dengeleyiciler (Load Balancer) kullanılabilir.
    - Servise daha fazla kaynak (CPU, bellek) atanarak yanıt süresi iyileştirilebilir.
    - Eğer mümkünse, yavaşlayan servisin sık kullanılan yanıtları bir önbellekte (Redis, Memcached) saklanabilir.
    - Yavaşlayan servisin iç işlemleri gözden geçirilip, optimizasyon yapılabilir.
    - Thread dump alarak bir deadlock ya da uzun süren bir işlem var mı diye kontrol edilebilir.
    - I/O problemlerine veya CPU kullanımına odaklanabiliriz.


</details>

<details>
  <summary><strong>Apache Kafka'nın genel yapısından bahsedebilir misin?</strong></summary>

  Apache Kafka, yüksek performanslı, dağıtık bir mesajlaşma platformudur. Genellikle olay tabanlı mimarilerde, büyük veri işleme veya asenkron iletişim gereksinimlerinde tercih edilir.

  Kafka'nın temel yapısına gelirsek:

  - **Producer:** Verileri Kafka'ya gönderen bileşendir. Mesajlar belirli bir **topic**'e yazılır. Örneğin, bir mikro hizmet veriyi işledikten sonra Kafka'ya mesaj bırakabilir.
  
  - **Topic:** Kafka'da mesajlar **topic** adı verilen mantıksal kategorilere ayrılır. Her topic, birden fazla **partition**'a bölünerek paralel işleme imkanı sunar.

  - **Partition:** Her topic birden fazla bölüme ayrılır. Bu bölümler, mesajların disk üzerinde sıralı bir şekilde saklanmasını sağlar. Partition'lar aynı zamanda ölçeklenebilirlik açısından önemlidir. Mesajlar burada offset ile numaralandırılır.

  - **Consumer:** Kafka'daki mesajları okuyan bileşendir. Tüketiciler, genellikle bir **consumer group** içinde organize edilir. Böylece aynı mesaj birden fazla tüketiciye atanabilir ya da bölünerek paralel şekilde işlenebilir.

  - **Broker:** Kafka'nın temel çalışma birimidir. Broker'lar, mesajları saklayan ve istekleri işleyen sunuculardır. Birden fazla broker bir Kafka cluster'ını oluşturur.

  Kafka’nın güçlü yönlerinden biri de **partition** tabanlı yapısı sayesinde yatayda kolayca ölçeklenebilmesidir. Bunun yanında, hem **yüksek hacimli veriyi** işleyebilir hem de düşük gecikme süresiyle çalışabilir. Ayrıca, mesajlar disk tabanlı loglarda saklandığı için kalıcıdır.

  Eğer cluster yönetiminden bahsedecek olursak, eski versiyonlarda **Zookeeper** kullanılmakta; ancak yeni versiyonlarda Kafka, kendi metadata yönetim sistemine geçmiş durumda. Bu da Zookeeper bağımlılığını ortadan kaldırdı.

  Kafka’nın en yaygın kullanım senaryoları arasında olay tabanlı sistemler, log toplama, gerçek zamanlı veri işleme ve mikro hizmetler arasında asenkron iletişim sağlama bulunur.

</details>

<details>
  <summary><strong>Monolith ile Microservice mimarilerinin farkı nedir? Hangisi daha avantajlıdır?</strong></summary>

  **Monolith**, tüm uygulamanın tek bir kod tabanı ve süreçte çalıştığı bir mimaridir. Geliştirmesi ve dağıtımı başlangıçta daha kolaydır, ancak büyüdükçe karmaşıklaşır ve bakım zorlaşır.  

  **Microservice**, uygulamanın küçük, bağımsız servislerden oluştuğu bir yapıdır. Her servis kendi veri tabanına ve bağımsız süreçlerine sahiptir. Ölçeklenebilirlik ve hata izolasyonu açısından daha avantajlıdır, ancak dağıtık yapısı nedeniyle yönetimi daha karmaşıktır.

  **Hangi mimari daha avantajlı?**  
  Küçük projelerde monolith tercih edilirken, büyük ve uzun vadeli projelerde microservice daha uygun olur. Birinin diğerine bir üstünlüğü yoktur.

</details>

<details>
  <summary><strong>Bir Spring Boot projesini başlatırken, örneğin IDE'den run tuşuna bastığında neler olur?</strong></summary>

  Bir Spring Boot uygulamasını run ettiğimde ilk olarak **SpringApplication.run()** metodu çağrılır ve bu, uygulamanın tüm başlangıç sürecini tetikler. 

  İlk olarak, **ApplicationContext** oluşturulur. Bu aşamada Spring, projemdeki tüm Bean'leri tarar, bağımlılıkları enjekte eder ve IoC container'ını hazırlar. Eğer bir web uygulamasıysa, gömülü bir sunucu (örneğin Tomcat) otomatik olarak başlatılır.  

  Ayrıca, Spring Boot’un **auto-configuration** özelliği devreye girer ve kullandığım bağımlılıklara göre varsayılan yapılandırmalar uygulanır. Örneğin, bir veri tabanı bağımlılığı varsa, Spring bunun için otomatik bir `DataSource` oluşturur.

  Uygulamanın başlangıç sürecinde, eğer `CommandLineRunner` veya `ApplicationRunner` implement ettiysem, bunlar çalıştırılır. Bu, uygulama başlangıcında özel işlemler yapmak istediğimde kullanılır.

  Kısacası, Spring Boot benim için birçok yapılandırmayı otomatik yapar ve uygulamamı minimum manuel ayarla çalıştırır.

</details>

<details>
  <summary><strong>Bir projede memory leak olsun istemeyiz. Bunu önlemek için geliştirme aşamasında nelere dikkat edersin?</strong></summary>

  Memory leak gerçekten kritik bir problem. Geliştirme sırasında buna dikkat etmek için genelde şunları yapıyorum:  

  Öncelikle, kullandığım kaynakları düzgün bir şekilde kapattığımdan emin oluyorum. Örneğin, bir dosya ya da veritabanı bağlantısı açıyorsam, bunu mutlaka `try-with-resources` ile yönetiyorum ki açık kalıp bellek sızıntısına neden olmasın.  

  Statik değişkenler konusunda da hassasım. Özellikle büyük nesneleri statik alanlarda tutmak gibi bir şey yapmamaya çalışıyorum, çünkü bu nesneler garbage collector tarafından temizlenemez.  

  Bir de, listener’lar ve callback’ler kullandığım projelerde, bunların yaşam döngüsünü düzgün yönetmek önemli. Eğer artık kullanılmayan bir listener varsa, onu mutlaka kayıttan kaldırırım.  

  Koleksiyonlarda büyük verilerle çalışıyorsam, bu verileri gerektiği gibi temizlediğimden emin olurum. Mesela bir `Map` içinde veri tutuyorsam, kullanım ömrü bittiğinde eski kayıtları silerim.  

  Son olarak, geliştirme aşamasında `VisualVM` veya benzeri profiling araçlarıyla uygulamayı analiz ederim. Bu, potansiyel memory leak’leri erken fark etmemi sağlar.  

  Amacım, yazdığım kodun uzun süreli çalışsa bile bellek yönetiminde sorun yaratmamasını sağlamak.

</details>

<details>
  <summary><strong>Parallelism ve Concurrency aynı şeyler mi?</strong></summary>

  Hayır, Parallelism ve Concurrency aynı şeyler değildir.  

  **Concurrency**, aynı anda birden fazla görevin yönetilmesi anlamına gelir. Ancak bu görevler fiziksel olarak aynı anda çalışıyor olmayabilir. Örneğin, tek bir işlemci üzerinde bir görev durdurulup başka bir görev çalıştırılabilir. Concurrency'de odak, görevlerin birbiriyle çakışmadan çalıştırılmasıdır.  

  **Parallelism** ise fiziksel olarak birden fazla görevin aynı anda çalıştırılmasıdır. Genellikle çok çekirdekli işlemcilerde görülür. Her çekirdek bir görevi aynı anda çalıştırabilir.  

  Özetle:
  - **Concurrency**, görevlerin bir arada yönetilmesiyle ilgilidir.
  - **Parallelism**, görevlerin aynı anda çalıştırılmasıdır.  

  İkisi farklı kavramlardır ama birlikte kullanılabilirler. Örneğin, bir sistem hem concurrent hem de parallel olabilir.
</details>

<details>
  <summary><strong>Hibernate cache seviyelerini duymuş muydun?</strong></summary>

  Detaylı bilgi için Medium yazımı inceleyebilirsiniz: [Hibernate First Level ve Second Level Cache Nedir?](https://medium.com/@yunusemrenalbant/hibernate-first-level-ve-second-level-cache-nedir-2025643501c3)

</details>

<details>
  <summary><strong>ArrayList varken LinkedList neden kullanırız?</strong></summary>

  ArrayList ve LinkedList'in farklı kullanım senaryoları vardır. LinkedList kullanmayı tercih edeceğim durumlar:

  - **Sık Ekleme/Çıkarma İşlemleri:**  
    LinkedList, özellikle liste başına veya ortasına ekleme/çıkarma işlemlerinde daha hızlıdır (O(1)). Çünkü elemanlar dinamik olarak bağlanır ve diğer elemanların kaydırılmasına gerek kalmaz.  

  - **Büyük Listeler:**  
    Eğer liste çok büyükse ve sık sık elemanlar arasında gezinme yerine ekleme/çıkarma yapıyorsam, LinkedList daha avantajlıdır.

  Ancak, rastgele erişim gerektiğinde (örneğin get(i)) ArrayList çok daha hızlıdır (O(1)), çünkü LinkedList’in rastgele erişim süresi O(n)’dir. Bu yüzden, kullanım senaryosuna göre hangisini seçeceğimi belirlerim.  
</details>

<details>
  <summary><strong>Microservice mimarisinde transaction yönetimini nasıl sağlıyorsun?</strong></summary>

  Detaylı bilgi için Medium yazımı inceleyebilirsiniz: [Microservice Mimarisinde Transaction Yönetimi](https://medium.com/@yunusemrenalbant/microservice-mimarisinde-transaction-y%C3%B6netimi-70d3bb0ecc50)

</details>


<details>
  <summary><strong>DDD nedir?</strong></summary>

  DDD, yani **Domain-Driven Design**, iş gereksinimlerini doğru bir şekilde yazılıma yansıtmak için geliştirilmiş bir yaklaşım. Ben genellikle karmaşık projelerde kullanıyorum, çünkü bu yaklaşım sayesinde domain’i anlamlı parçalara ayırabiliyorum. Mesela, **Bounded Context** kavramı burada devreye giriyor. Her bounded context, iş alanının belirli bir bölümüne odaklanmamı sağlıyor ve farklı ekiplerin bağımsız çalışmasına olanak tanıyor.  

  Ayrıca **Ubiquitous Language** sayesinde, iş birimleriyle konuşurken aynı terimleri kullanıyoruz. Örneğin, finans sektöründe çalışıyorsam "hesap bakiyesi" veya "ödeme" gibi kavramlar yazılım kodlarında da aynı şekilde geçiyor.  

  DDD'nin bana en çok katkı sağladığı nokta, karmaşık iş kurallarını daha anlaşılır ve sürdürülebilir bir şekilde modellemek oluyor. Bu sayede projeler büyüdüğünde bile kontrol edilebilir kalıyor.

</details>

<details>
  <summary><strong>CQRS nedir?</strong></summary>

  CQRS, yani **Command Query Responsibility Segregation**, basitçe veri yazma ve veri okuma işlemlerini birbirinden ayırıyor. Ben genelde bu yapıyı performans problemleri olan projelerde kullanıyorum. Örneğin, bir kullanıcı sistemi geliştirdiğimizi düşünelim: Kullanıcı verilerini güncelleme (command) işlemleriyle sadece veri okuma (query) işlemlerini ayırdığınızda, her birine özel optimizasyon yapabiliyorsunuz.  

  Mesela okuma tarafında farklı bir veri modeli kullanarak çok hızlı bir sorgulama yapabiliyorum. Yazma tarafında ise daha kompleks iş kuralları uygulayabiliyorum. Özellikle büyük veri setlerinde CQRS sayesinde çok ciddi performans artışı elde ettim.  

  Genelde **Event Sourcing** ile birlikte kullanıyorum. Her değişikliği bir event olarak kaydettiğimde, sistem geçmişe yönelik tüm değişiklikleri izleyebiliyor.
</details>

<details>
  <summary><strong>Kafka ile RabbitMQ farkını biliyor musun?</strong></summary>

  **Kafka**, daha çok yüksek hacimli veri akışı ve olay tabanlı sistemler için kullanılıyor. Örneğin, log analitiği ya da gerçek zamanlı veri işleme gibi durumlarda tercih ederim. Mesajlar Kafka’da log olarak saklanır ve tüketildikten sonra bile sistemde kalır. Bu, mesajların yeniden oynatılmasını mümkün kılar. Ayrıca, Kafka’yı bir mesaj kuyruğundan çok bir veri akış platformu olarak görüyorum.  

  **RabbitMQ** ise daha klasik bir mesajlaşma sistemi. Özellikle point-to-point veya publish/subscribe modelleri için ideal. Eğer bir mesajın sadece bir tüketiciye ulaşmasını istiyorsam ya da hızlı bir şekilde mesaj alıp iletmem gerekiyorsa RabbitMQ’yu tercih ederim. RabbitMQ daha düşük hacimli ama daha hızlı teslimat gerektiren senaryolarda avantajlı oluyor.  

  Kısacası: Kafka’yı veri akışı ve olay bazlı sistemler için, RabbitMQ’yu ise hızlı ve güvenilir mesaj iletimi gereken durumlarda tercih ediyorum.

</details>
<details>
  <summary><strong>Spring Boot uygulamasının başlangıç süresini nasıl optimize edersiniz? Özellikle büyük ve bağımlı bir uygulamada bunu nasıl sağlarsınız?</strong></summary>
  Spring Boot başlangıç süresini iyileştirmek için @Lazy anotasyonu ile bean başlatmalarını gerektiğinde yapılacak hale getiririm. Ayrıca, bağımlı konfigürasyonları ve gereksiz Spring starter modüllerini projeden çıkartırım. Bir başka strateji olarak, uygulamayı native bir imaj haline getirip GraalVM ile başlatma süresini azaltmak da mümkündür.

</details>

<details>
  <summary><strong>Garbage Collection (GC) ayarlarını nasıl optimize edersiniz? Özellikle yüksek bellek tüketimi olan bir Spring Boot uygulamasında hangi ayarları tercih edersiniz?</strong></summary>
  Yüksek bellek tüketimi olan bir Spring Boot uygulamasında genellikle G1 Garbage Collector kullanmayı tercih ederim. JVM ayarlarını özelleştirerek maksimum heap boyutunu (Xmx) belirlerim ve XX:MaxGCPauseMillis ile beklenen GC süresini sınırlandırırım. GC loglarını inceleyerek sık veya uzun süren duraklamaları belirleyip gerektiğinde bellek yönetimi için farklı GC algoritmaları (örneğin ZGC veya Shenandoah) deneyebilirim.
</details>

<details>
  <summary><strong>Spring Cloud bileşenlerinden hangilerini kullandınız? Özellikle Netflix OSS araçları (Eureka, Ribbon, Hystrix) hakkında deneyiminiz var mı?</strong></summary>
Eureka ile mikroservisler arasında dinamik servis keşfi sağladım. Yük dengeleme için Ribbon’u, Circuit Breaker için ise Hystrix veya Resilience4j’yi kullanarak uygulamanın kesintisiz çalışmasını garanti altına alıyorum. Özellikle Hystrix ile fallback mekanizmaları kurarak bir serviste sorun çıktığında diğer servislerin etkilenmesini önledim.
</details>

<details>
  <summary><strong>Config Server kullanarak yapılandırma yönetimini nasıl merkezi hale getirirsiniz? Config Server’ın faydaları nelerdir?</strong></summary>
Config Server, her bir servisin yapılandırmasını merkezi olarak yönetmemi sağlıyor. Özellikle farklı ortamlarda (prod, dev, test) kullanılacak yapılandırmaları kolayca yönetmek için Spring Cloud Config Server ile her bir servise özel ayarları tanımlar ve git gibi bir kaynak yönetim sistemi ile entegre ederim. Böylece yapılandırmalar bir merkezden güncellenebilir ve değişikliklerde otomatik olarak yeniden yüklenir.
</details>

<details>
  <summary><strong>Spring Boot üzerinde uzun süre çalışan işlemler için nasıl optimizasyon yaparsınız? Timeout ve retry gibi stratejileri nasıl belirlersiniz?</strong></summary>
  Uzun süren işlemleri yönetmek için, zaman aşımı (timeout) sürelerini @Timeout anotasyonları veya özel konfigürasyonlarla belirlerim. Circuit Breaker desenini, özellikle mikroservisler arasındaki çağrılarda Hystrix veya Resilience4j kullanarak uygularım, bu sayede uzun süren işlemler devre dışı bırakılarak sistem performansının düşmesini engeller. Retry stratejileri için ise belirli aralıklarla yeniden denemeler yapılır, ancak her deneme arasında artan bir süre bırakılarak aşırı yükün önüne geçilir.
</details>
<details>
  <summary><strong>OAuth2 ile güvenlik sağlama konusunda neler biliyorsun?</strong></summary>
OAuth2, kullanıcıların yetkilendirme süreçlerini üçüncü taraf sağlayıcılar (Google, Facebook vb.) üzerinden yönetmesini sağlar.
</details>
<details>
  <summary><strong> Mikroservislerde güvenlik açıklarını tespit etmek için hangi araçlar kullanılabilir?</strong></summary>
OWASP ZAP, Burp Suite, SonarQube, Snyk gibi araçlar güvenlik açıklarını tespit etmek için kullanılabilir. Ayrıca, runtime güvenliği için Falco, Aqua ve Prisma gibi araçlar da tercih edilebilir.
</details>
<details>
  <summary><strong>Mikroservislerde backpressure nasıl yönetilir?</strong></summary>
Backpressure, bir servisin aşırı yüklenmesini önlemek için kullanılan bir mekanizmadır. Bu, istekleri sınırlayarak, kuyruk uzunluğunu kontrol ederek veya istemcilerin istek hızını yavaşlatarak sağlanabilir. Reactive programming ve akış kontrol mekanizmaları (örneğin, Reactive Streams) bu süreçte yardımcı olabilir.
</details>
