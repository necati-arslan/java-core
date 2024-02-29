# Public VS Static for Method in class
Özetle, public bir erişim belirleyicidir ve bir değişkenin veya metodun erişim düzeyini belirlerken, 
static bir anahtar kelimedir ve bir değişkenin veya metodun sınıf seviyesine yerleştirilmesini sağlar, 
böylece nesne oluşturmadan çağrılabilir hale gelir.

# Public VS Static for Variable
- Sınıf Seviyesinde: static değişkenler, sınıfın kendisine aittirler ve sınıfın herhangi bir örneği (instance) oluşturulmadan kullanılabilirler.
- static değişkenler, bir sınıfın tüm örnekleri (instance) arasında paylaşılır ve sadece bir kopyası bellekte tutulur.
- static değişkenler, bir sınıfın örneğine (instance) bağlı değildirler. Bu nedenle, bir sınıf örneği oluşturulmadan da kullanılabilirler.

# Private Constructor
- Java'da bir sınıfın private constructor'ı, bu sınıftan nesne oluşturulmasını engeller. private constructor,
  yalnızca aynı sınıf içinden çağrılabilir ve bu sınıfın dışından erişilemez.
  
public class Singleton {
    private static Singleton instance;

    // Private constructor
    private Singleton() {
        // Constructor body
    }

    // Static method to get the instance of Singleton class
    public static Singleton getInstance() {
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }
}```

```
