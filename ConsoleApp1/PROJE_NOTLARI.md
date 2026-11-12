# Dilara Tepe Kişisel Web Sitesi

## Proje özeti

Bu proje, başlangıçta bir `.NET 10 Console App` olarak oluşturuldu. Daha sonra ASP.NET Core kullanılarak Dilara Tepe için fizyoterapi ve sağlık temalı, tek sayfalı kişisel web sitesine dönüştürüldü.

## Kullanılan teknolojiler

- **.NET 10:** Proje altyapısı
- **ASP.NET Core:** Web sunucusu ve uygulama başlangıcı
- **C#:** Uygulamanın çalıştırılması ve sunucu yapılandırması
- **HTML:** Sayfa yapısı ve içerik
- **CSS:** Renkler, düzen, kartlar ve responsive tasarım
- **JavaScript:** Mobil menü ve otomatik yıl bilgisi
- **SVG:** Yerel fizyoterapi illüstrasyonu
- **Visual Studio:** Geliştirme ortamı

## Yapılan adımlar

### 1. Console projesi web projesine dönüştürüldü

`ConsoleApp1.csproj` dosyasında ASP.NET Core Web SDK kullanıldı:

```xml
<Project Sdk="Microsoft.NET.Sdk.Web">
```

Proje hedef framework olarak `.NET 10` kullanmaktadır.

### 2. ASP.NET Core başlangıç yapısı oluşturuldu

`Program.cs` dosyasında uygulama başlatıldı ve `wwwroot` klasöründeki statik dosyaların sunulması sağlandı:

```csharp
var builder = WebApplication.CreateBuilder(args);
var app = builder.Build();

app.UseDefaultFiles();
app.UseStaticFiles();

app.Run();
```

### 3. Web sitesi HTML yapısı oluşturuldu

`wwwroot/index.html` dosyasında aşağıdaki bölümler oluşturuldu:

- Üst navigasyon menüsü
- Dilara Tepe marka alanı
- Ana tanıtım bölümü
- Fizyoterapi, hemşirelik ve sağlıklı yaşam kartları
- Hakkımda bölümü
- Instagram bağlantısı
- Footer bölümü

Site tek sayfalı yapıdadır. Menü bağlantıları sayfanın ilgili bölümlerine gider.

### 4. Site içeriği Dilara Tepe’ye göre düzenlendi

Sitede şu bilgiler kullanıldı:

- Dilara Tepe
- Fizyoterapi mezunu
- Hemşirelik mezunu
- Sağlık ve hareket odaklı profil
- Instagram: `@fzt.dilaratepe`

Tarayıcı sekmesindeki site adı:

```html
<title>Dilara Tepe</title>
```

### 5. Fizyoterapi temalı tasarım oluşturuldu

`wwwroot/styles.css` dosyasında aşağıdaki tasarım özellikleri uygulandı:

- Turkuaz ve yeşil sağlık renkleri
- Açık renkli arka plan
- Yuvarlatılmış kartlar
- Yumuşak gölgeler
- Hero görsel alanı
- Uzmanlık kartları
- Mobil uyumlu tasarım

### 6. Yerel SVG görseli eklendi

`wwwroot/physio-illustration.svg` dosyası oluşturuldu.

Bu görsel:

- Fizyoterapi ve hareket temasını temsil eder.
- Harici bir web sitesine bağlı değildir.
- Proje içinde bulunduğu için internet olmadan da kullanılabilir.
- Farklı ekranlarda kalite kaybetmez.

### 7. İletişim formu kaldırıldı

İletişim formu yerine yalnızca Instagram bağlantısı bırakıldı:

```html
https://www.instagram.com/dilaratepe/
```

### 8. Responsive tasarım yapıldı

Site aşağıdaki cihazlara uyumlu olacak şekilde hazırlandı:

- Masaüstü bilgisayar
- Laptop
- Tablet
- Mobil telefon

Mobil ekranlarda menü hamburger menüye dönüşür ve kartlar alt alta sıralanır.

### 9. JavaScript etkileşimleri eklendi

`wwwroot/script.js` dosyasında:

- Mobil menünün açılıp kapanması
- Footer yılının otomatik güncellenmesi

işlevleri oluşturuldu.

## Proje dosya yapısı

```text
ConsoleApp1/
│
├── ConsoleApp1.csproj
├── Program.cs
├── PROJE_NOTLARI.md
│
└── wwwroot/
    ├── index.html
    ├── styles.css
    ├── script.js
    └── physio-illustration.svg
```

## Çalıştırma

PowerShell veya Visual Studio terminalinde proje klasörüne gidin:

```powershell
cd C:\Users\gokha\source\repos\ConsoleApp1
```

Projeyi çalıştırın:

```powershell
dotnet run --project .\ConsoleApp1\ConsoleApp1.csproj
```

Terminalde gösterilen localhost adresini tarayıcıda açın. Örnek:

```text
http://localhost:39252
```

## Derleme

Projeyi derlemek için:

```powershell
dotnet build
```

## Yayınlama notu

`localhost` adresi yalnızca yerel bilgisayarda çalışır. Siteyi herkese açık yapmak için ASP.NET Core destekleyen bir sunucuya veya Azure App Service gibi bir hosting hizmetine yayınlamak gerekir.
