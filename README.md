# ESP8266-AppleHomeKit

Bu proje, ESP8266 tabanlı bir cihazın ev otomasyonu için basit bir örneğini sunar. Bu cihaz, iOS Home uygulaması üzerinden kontrol edilebilen bir anahtar anahtarlamasını gerçekleştirir. Ayrıca, projenin elektronik bileşenleri ve bağlantıları hakkında bilgi de içerir. Bu README, proje hakkında bilgi vermek, nasıl kullanılacağını anlatmak ve ESP8266 için IDE ayarlarını göstermek için hazırlanmıştır.

## Kurulum

Bu projeyi çalıştırmak için öncelikle Arduino IDE veya PlatformIO kurulumunu yapmanız gerekmektedir. Arduino IDE kullanarak kurulum yapmak istiyorsanız aşağıdaki adımları takip edebilirsiniz:

1. Arduino IDE'yi [resmi web sitesinden](https://www.arduino.cc/en/software) indirin ve kurun.
2. Arduino IDE'yi açın ve `Araçlar` > `Kart` > `Kart Yöneticisi`'ne gidin.
3. Açılan pencerede, `Ayarlar` simgesine tıklayın (sağ üst köşe).
4. `Eklenti URL'leri` alanına `http://arduino.esp8266.com/stable/package_esp8266com_index.json` adresini ekleyin.
5. Tamamlandıktan sonra `Kapat` düğmesine tıklayın.
6. `Kart Yöneticisi`'ne geri dönün ve `ESP8266` kütüphanesini arayın.
7. `ESP8266` kütüphanesini seçin ve `Yükle` düğmesine tıklayarak yükleyin.
8. Yükleme tamamlandıktan sonra, `Araçlar` > `Kart` > `ESP8266 Boards (…)` > `Generic ESP8266 Module` seçeneğini seçin.

Artık projeyi yüklemeye hazırsınız. Arduino IDE'yi kullanarak `.ino` dosyasını açıp ESP8266 tabanlı bir kart seçerek kodu yükleyebilirsiniz.

## Nasıl Kullanılır

1. Bu projeyi klonlayın veya indirin.
2. Arduino IDE veya PlatformIO gibi bir Arduino geliştirme ortamını açın.
3. `.ino` uzantılı dosyayı açın ve ESP8266 tabanlı bir kart seçerek kodu yükleyin.
4. ESP8266 cihazınıza güç sağlayın.
5. ESP8266 cihazınızın kurulum ekranına bağlanmak için Wi-Fi ayarlarınızdan "Kardo Ambiyans" ağını seçin. Bu Ağ adı şifresizdir ve direkt olarak katılınabilirdir.
6. Ağa girdikten sonra bir web server sayfası sizi karşılayacak ve burada Configure Wi-Fi alanından kendi Wi-Fi adresinize giriş yapmalısınız.
7. Giriş yapıldıktan sonra ESP01 Wifi modülü Erişim noktası modunu kapatarak hafızayasına yazdığı Wi-Fi bilgileri ile Wi-Fi ağınuza bağlanır.
8. Daha iPhone üzerinden Home (Ev) uygulamasına gidin ve yeni bir aksesuar ekleme ekranına gidin.
9. Daha Fazla seçeneği seçin.
10. Cihazınızı bulun ve ekleme işlemini tamamlayın.
11. Artık cihazınızı Home uygulamasından kontrol edebilirsiniz.

## Notlar

- ESP8266'ya kod yüklenirken USB programlayıcı kullanılarak yapılmıştır.
- USB programlayıcı ile ESP8266 kartına kod atarken, GPIO0 ve GND pinlerini kısa devre yaparak programlama moduna almanız gerekmektedir.


## Elektronik Bileşenler

Bu projede kullanılan ana bileşenler:

- ESP8266 mikrodenetleyici
- Anahtar anahtarlamak için bir röle (OPSİYONEL)
- 220V AC güç kaynağı
- Bağlantı telleri
- Prototip kartı veya devre kartı

## Devre Bağlantıları

- ESP8266'nın GPIO2 pini röle kontrolü için kullanılır.
- Röle, anahtarlama yapılacak cihazın güç kablosuna seri olarak bağlanır.
- ESP8266'nın VCC ve GND pinleri güç kaynağına bağlanır.
- Gerekirse, düğme veya başka bir tetikleyici bağlantısı yapılabilir.

## Schematic

![](https://github.com/bkaan99/ESP8266-AppleHomeKit/blob/main/Schematic_espp_2024-03-12_page-0001.jpg)


## Proje Yapısı

- `src` klasörü: Arduino kaynak kodları.
  - `main.ino`: Ana Arduino kodu.
- `LICENSE`: Proje lisans dosyası.
- `README.md`: Bu dosya, proje açıklaması.

## Gereksinimler

- ESP8266 tabanlı bir cihaz
- Arduino IDE veya PlatformIO

## Katkıda Bulunma

1. Bu depoyu fork edin.
2. Yeni özellikler ekleyin veya hataları düzeltin.
3. Değişikliklerinizi commit edin.
4. Bir pull isteği gönderin.

## Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Daha fazla bilgi için [LICENSE](LICENSE) dosyasına bakın.
