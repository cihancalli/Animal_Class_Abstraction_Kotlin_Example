# Animal_Class_Abstraction_Kotlin_Example
## Kotlin Uygulamasında Abstraction Kullanarak Sınıf Örneği

Abstraction, bir sınıfın veya nesnenin özelliklerini ve davranışlarını ayrıntılı uygulamadan tanımlamanıza olanak tanır. Bu, kodunuzu daha modüler, yeniden kullanılabilir ve okunabilir hale getirir.

Abstraction kullanarak bir sınıf örneği oluşturmak için aşağıdaki adımları izleyebilirsiniz:

1. Soyut Sınıf Tanımlama:

* abstract anahtar sözcüğünü kullanarak soyut bir sınıf tanımlayın.
* Sınıfın özelliklerini ve davranışlarını soyut yöntemler olarak tanımlayın.


```bash
abstract class Hayvan(val ad: String) {
    abstract fun sesCikar(): String
}

```

2. Soyut Sınıftan Türeyen Sınıflar:

* Soyut sınıftan türeyen somut sınıflar oluşturun.
* Soyut sınıftaki soyut yöntemleri somut hale getirin.

```bash
class Kedi(ad: String) : Hayvan(ad) {
    override fun sesCikar(): String {
        return "Miyav"
    }
}

class Kopek(ad: String) : Hayvan(ad) {
    override fun sesCikar(): String {
        return "Hav hav"
    }
}

```

3. Soyut Sınıf Örneği Oluşturma:

* Soyut sınıftan doğrudan bir örnek oluşturamazsınız.
* Somut sınıflar aracılığıyla soyut sınıftan örnekler oluşturabilirsiniz.

```bash
val kedi = Kedi("Mırmır")
val kopek = Kopek("Karamel")

println(kedi.ad + " " + kedi.sesCikar())
println(kopek.ad + " " + kopek.sesCikar())

```

```bash
Mırmır Miyav
Karamel Hav hav
```

Abstraction Kullanmanın Avantajları:

Kod tekrarı azalır.
* Kod daha modüler ve yeniden kullanılabilir hale gelir.
* Kodun okunabilirliği ve anlaşılırlığı artar.
* Değişikliklere karşı daha esnek bir kod elde edilir.

Abstraction Kullanmanın Dezavantajları:
* Somutlaştırılması gereken soyut yöntemler olması nedeniyle daha fazla kod yazma ihtiyacı doğar.
* Karmaşıklık artabilir.

Abstraction Örnekleri:
* Hayvan, Bitki, Araç gibi soyut kavramlar
* Geometrik şekiller (Daire, Kare, Üçgen)
* Veri tabanı bağlantısı, dosya okuma/yazma gibi işlemler