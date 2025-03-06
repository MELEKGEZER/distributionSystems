
# Dağıtık Sistem Mimarisi Projesi

Bu proje, Docker ve Docker Compose kullanılarak oluşturulmuş bir dağıtık sistem mimarisini içerir. Sistemde Nginx, Spring Boot uygulamaları, PostgreSQL ve Redis gibi bileşenler yer almaktadır.

## 📋 Proje Detayları

### 🛠️ Kullanılan Teknolojiler
- **Nginx**: Yük dengeleyici olarak kullanıldı.
- **Spring Boot**: İki replikasyonlu uygulama sunucuları.
- **PostgreSQL**: Veritabanı olarak kullanıldı.
- **Redis**: Önbellek sunucusu olarak kullanıldı.
- **Docker & Docker Compose**: Tüm servislerin container olarak çalıştırılması.

### 📂 Dosya Yapısı
- `docker-compose.yml`: Tüm servislerin tanımlandığı Docker Compose dosyası.
- `Dockerfile`: Spring Boot uygulamasının imajını oluşturmak için kullanılan Dockerfile.
- `nginx/nginx.conf`: Nginx yapılandırma dosyası.
- `README.md`: Proje dokümantasyonu (bu dosya).

## 🚀 Projeyi Çalıştırma

### Ön Koşullar
- Docker ve Docker Compose'un sisteminizde yüklü olması gerekmektedir.

### Adımlar
1. Proje dosyalarını bilgisayarınıza indirin:
   ```bash
   git clone https://github.com/MELEKGEZER/distributionSystems.git
   ```
2. Docker Compose ile servisleri başlatın:
   ```bash
   docker-compose up --build
   ```
3. Tarayıcınızda `http://localhost` adresine giderek Nginx üzerinden uygulamaya erişebilirsiniz.

## 🧪 Failover Testi
1. Çalışan Spring Boot uygulamalarından birini durdurun:
   ```bash
   docker stop <container_id>
   ```
2. Sistemin diğer uygulama sunucusuna otomatik olarak yönlendirme yaptığını gözlemleyin.
3. Durduğunuz uygulamayı tekrar başlatın ve diğerini durdurun. Sistemin sorunsuz çalışmaya devam ettiğini kontrol edin.

## 📹 Tanıtım Videosu
Projenin nasıl çalıştığını ve failover testini gösteren bir tanıtım videosu hazırladım. Videoyu [buradan]([videolinki.mp4](https://drive.google.com/file/d/1bghRGH01YujZ_mFeJJWY0eH5VB3oH5Ew/view?usp=drive_link)) izleyebilirsiniz.


**Teşekkürler!** 🎉

