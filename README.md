# SkywellADBOperations
Instructions how you can manage ADB operations in your Skywell ET5
NOTE: English instructions, instruction images and a how to video is coming soon.

```
███████╗████████╗   ██████╗ 
██╔════╝╚══██╔══╝   ██╔══██╗
███████╗   ██║█████╗██████╔╝
╚════██║   ██║╚════╝██╔══██╗
███████║   ██║      ██║  ██║
╚══════╝   ╚═╝      ╚═╝  ╚═╝
```

## Türkçe: Skywell ET5 Aracımıza Nasıl ADB ile Android Uygulamaları Yükleyebiliriz?

Herkese Merhaba,

Skywell ET5 aracımıza uygulama silmek ve yüklemek için ADB (Android Debug Bridge) kullanabiliriz. Aracımızın multimedya sistemi Android işletim sistemi üzerine kuruludur. Her Android cihazın hata ayıklama amaçlarıyla kurulmuş bir ADB arayüzü bulunur. Bu teknikte, ADB sistemini kullanarak aracımıza bağlanabilir, yeni uygulamalar yükleyebilir ve bu uygulamaları silebiliriz.

### Gerekenler:
+ Kişisel erişim noktası açılabilen herhangi bir cihaz. (Ör: Cep telefonunuz)
+ Bir bilgisayar (Windows)

### İndirmeler:
+ [Skywell Klasörü](https://drive.google.com/file/d/1_5Ux8xSb4I_E_NUmiDYTvRxZo4r_Vkwi/view?usp=sharing)

**Önemli Not:** Bu işlemleri adım adım dediğim gibi yaptığınız takdirde, cihazınıza hiçbir zarar gelmeyecek, cihazınız garanti kapsamından çıkmayacaktır. Yapılan tüm işlemler geri alınabilir türdendir. Garanti tarafında sorun yaşamamak adına, aracı yetkili servise götürmeden önce yüklediğiniz uygulamaları silmenizi öneririm. Herhangi bir sorun çıktığı takdirde bana **onureser12@gmail.com** mail adresinden ulaşabilirsiniz.

#### Adım 1: Gerekli dosyaların kurulumu:

İşlemlere başlamadan önce bu sayfaya bilgisayarınız ile girip, [buraya](https://drive.google.com/file/d/1_5Ux8xSb4I_E_NUmiDYTvRxZo4r_Vkwi/view?usp=sharing) tıklayarak gerekli tüm dosyaları indirebilirsiniz. "Skywell" klasörünü rar dosyasından çıkardıktan sonra masaüstüne taşıyınız. Yüklemek istediğiniz .apk dosyalarını bu "Skywell" klasörünün içine atmanız gerekmekte.

#### Adım 2: Bilgisayarı araba ile aynı Wi-Fi ağına bağlamak:

Telefonunuzdan bir kişisel erişim noktası oluşturup hem arabanızı hem de bilgisayarınızı aynı Wi-Fi ağına bağlayınız. Bu noktada Arabanızın IP adresini öğrenmeniz gerekecek. Bunun için araba ayarlarındaki Wi-Fi ayarlarına girin ve bağlı olduğunuz Wi-Fi bağlantısının üzerine tıklayın. Açılan pencerede "192.168.1.34" benzeri bir IP adresi göreceksiniz.

#### Adım 3: ADB ile bilgisayarı arabaya bağlamak:

Bilgisayarınızın klavyesinin ```Windows Tuşu + R``` tuşlarına aynı anda basarak "Çalıştır" penceresini açın. Açılan pencerede "Aç:" yazan metin kutusuna ```cmd``` yazın ve "Tamam" tuşuna basın. Açılan siyah ekranda ```C:\Users\Kullanıcı Adınız>``` yazacak. Buraya yazdığımız her komuttan sonra "Enter" tuşuna basarak komutların çalışmasını sağlayabiliriz. Komutlarımızı yazarken büyük-küçük harflere önem göstermeliyiz.

Öncelikle masaüstüne attığımız klasörün içine girmek adına aşağıdaki komutu yazalım:

```cd Desktop\Skywell```

Siyah ekranda artık ```C:\Users\Kullanıcı Adınız\Desktop\Skywell>``` yazdığını göreceksiniz. Sonrasında arabaya bağlanmak için arabadan öğrendiğimiz IP adresini kullanarak aşağıdaki komutu yazalım: (Ben 192.168.1.34 örneğinden gittim. Siz ne IP adresi gördüyseniz onu yazın.)

```adb connect 192.168.1.34```

Bağlantı kurulduktan sonra aşağıdaki komutu yazarak istediğimiz apk dosyasını kurabiliriz: (Örnekteki info.apk dosyası, indireceğiniz Skywell klasörünün içinde örnek olarak koyulmuştur. Deneme amaçlı bu uygulamayı yükleyebilirsiniz. info.apk uygulaması sayesinde aracın özelliklerini ve yüklü donanımı görebiliriz.)

```adb install ./info.apk```

#### Adım 4: Yüklemeyi doğrulamak:

Bazen yükleme gereğinden uzun sürebilir, takılabilir veya bağlantı kopabilir. Bu durumlar hiçbir kötü sonuç doğurmaz, sadece işlemi tekrar yapmanız gerekir. Yükleme işlemi bittikten sonra aracımızdan uygulama merkezine girelim. Eğer yüklemiş olduğumuz uygulamayı göremiyorsak, sol üstteki çarpı işaretine tıklayarak uygulama merkezini kapatıp tekrar açalım.

## Türkçe: ADB Kullanarak Yüklediğimiz Uygulamaları Nasıl Silebiliriz?

Aynı yükleme işlemindeki gibi, silme işleminde de "Skywell" klasörü masaüstünde, araba ile bilgisayar aynı Wi-Fi ağına bağlı olmalıdır. Bu koşullar sağlanıyorsa, cmd ekranını tekrar açabiliriz.

#### Adım 1: ADB ile bilgisayarı arabaya bağlamak:

Bilgisayarınızın klavyesinin ```Windows Tuşu + R``` tuşlarına aynı anda basarak "Çalıştır" penceresini açın. Açılan pencerede "Aç:" yazan metin kutusuna ```cmd``` yazın ve "Tamam" tuşuna basın. Açılan siyah ekranda ```C:\Users\Kullanıcı Adınız>``` yazacak. Buraya yazdığımız her komuttan sonra "Enter" tuşuna basarak komutların çalışmasını sağlayabiliriz. Komutlarımızı yazarken büyük-küçük harflere önem göstermeliyiz.

Öncelikle masaüstüne attığımız klasörün içine girmek adına aşağıdaki komutu yazalım:

```cd Desktop\Skywell```

Önceden kalma herhangi bir bağlantı olmasını önlemek adına, ADB'nin bağlantığı tüm cihazlardan bağlantıyı koparalım:

```adb disconnect```

Aracın IP adresini kullanarak araç ile bağlantı kuralım:

```adb connect 192.168.1.34```

#### Adım 2: ADB kullanarak tabletin "Ayarlar" gizli menüsünü açma:

ADB bağlantısı kurulduktan sonra aşağıdaki komutu girerek "Ayarlar" gizli menüsünü açabiliriz. Bu menüde yaptığınız her şey kendi sorumluluğunuzdadır.

```adb shell am start -a android.settings.SETTINGS```

Açılan ayarlar menüsünden uygulama ayarlarına giderek istediğiniz uygulamayı silebilirsiniz.

Not: Yakında resimli ve videolu anlatım eklenecek.

İyi Çalışmalar,

Onur Eser

*ST-R Motors*
