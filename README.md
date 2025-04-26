# WhatsApp Mesaj Gönderim Simülatörü

![WhatsApp Simülatör Banner](https://via.placeholder.com/1200x300/4CAF50/FFFFFF?text=WhatsApp+Mesaj+G%C3%B6nderim+Sim%C3%BClat%C3%B6r%C3%BC)

## 📌 Proje Açıklaması

WhatsApp Mesaj Gönderim Simülatörü, bireysel WhatsApp hesaplarından kişi listenize otomatik mesaj gönderimi simüle etmenize olanak tanıyan kapsamlı bir uygulamadır. Uygulama, günlük mesaj gönderim limitlerini yönetir, mesaj şablonları sunar ve mesaj geçmişini takip eder.

### Temel Özellikler

- 👥 **Kişi Yönetimi**: Kullanıcıları ekleyebilir, düzenleyebilir, silebilir ve CSV ile içe aktarabilirsiniz
- 👪 **Grup Yönetimi**: Kullanıcıları kategorilere ayırabilirsiniz
- 📝 **Şablon Yönetimi**: Mesaj şablonları oluşturabilir ve kategorilendirebilirsiniz
- 📲 **Gönderim Simülasyonu**: WhatsApp mesaj gönderimini simüle edebilirsiniz
- 📊 **Raporlama**: İşlem geçmişini ve logları takip edebilirsiniz
- 📅 **Günlük Limit Yönetimi**: Hesap başına günlük gönderim limitlerini yapılandırabilirsiniz

## 🔧 Teknolojiler

### Frontend
- **React** - Kullanıcı arayüzü geliştirmek için
- **TypeScript** - Tip güvenliği ve kod kalitesi için
- **TailwindCSS** - Stil ve CSS yönetimi için
- **Shadcn/UI** - Modern, özelleştirilebilir UI bileşenleri için
- **TanStack Query** - Veri alma, önbelleğe alma ve eşitleme için
- **React Hook Form** - Form yönetimi ve doğrulama için
- **Zod** - Şema doğrulama için

### Backend
- **Node.js** - Sunucu tarafı uygulaması için temel platform
- **Express** - REST API ve HTTP sunucusu işlemleri için
- **Drizzle ORM** - Veritabanı işlemleri için ORM çözümü
- **PostgreSQL** - Kalıcı veri saklama için ilişkisel veritabanı
- **Multer** - Dosya yükleme işlemleri için

## 🚀 Kurulum Adımları

### Önkoşullar
- Node.js (v16 veya üstü)
- PostgreSQL (v12 veya üstü)
- npm veya yarn

### Veritabanı Kurulumu
1. PostgreSQL kurulumunu tamamlayın
2. Aşağıdaki SQL komutunu çalıştırarak veritabanını oluşturun:
```sql
CREATE DATABASE whatsapp_simulator;
```

### Uygulama Kurulumu
1. Repository'yi klonlayın:
```bash
git clone https://github.com/kullaniciadi/norawp.git
cd norawp
```

2. Bağımlılıkları yükleyin:
```bash
npm install
```

3. `.env.example` dosyasını `.env` olarak kopyalayıp veritabanı bağlantı bilgilerinizi güncelleyin:
```bash
cp .env.example .env
```

4. Veritabanı şemasını oluşturun:
```bash
npm run db:push
```

5. Uygulamayı başlatın:
```bash
npm run dev
```

6. Tarayıcınızı açıp `http://localhost:5000` adresine gidin

## 📊 Veri Modelleri

### Kullanıcılar (Users)
Kişi bilgilerini içerir: isim, telefon, e-posta, grup üyeliği

### Kullanıcı Grupları (User Groups)
Kişileri kategorilere ayırmak için kullanılır

### Mesaj Şablonları (Message Templates)
Önceden tanımlanmış mesaj içerikleri

### Şablon Kategorileri (Template Categories)
Mesaj şablonlarını kategorilere ayırma

### Gönderim Geçmişi (Message History)
Gönderilmiş mesajların kaydı

### Sistem Logları (Logs)
Sistem işlemleri ve hatalar

### Yapılandırma (Config)
Günlük limit ve aktif hesap sayısı

## 🖼️ Ekran Görüntüleri

![Ana Sayfa](https://via.placeholder.com/800x450/3F51B5/FFFFFF?text=Ana+Sayfa)
![Kişi Yönetimi](https://via.placeholder.com/800x450/FF5722/FFFFFF?text=Ki%C5%9Fi+Y%C3%B6netimi)
![Şablon Yönetimi](https://via.placeholder.com/800x450/009688/FFFFFF?text=%C5%9Eablon+Y%C3%B6netimi)

## 📄 Lisans

Bu proje [MIT Lisansı](LICENSE) altında lisanslanmıştır.

## 🚢 Dağıtım Rehberi

### Kendi Sunucunuzda Dağıtım
1. Projeyi sunucunuza klonlayın: `git clone https://github.com/kullaniciadi/norawp.git`
2. Node.js ve PostgreSQL kurulumunu yapın
3. Veritabanını oluşturun: `CREATE DATABASE whatsapp_simulator;`
4. Çevresel değişkenleri ayarlayın (`.env` dosyası)
5. Bağımlılıkları yükleyin: `npm install --production`
6. Projeyi derleyin: `npm run build`
7. Uygulamayı başlatın: `npm start`

### Docker ile Dağıtım
1. Docker ve Docker Compose'u kurun
2. `docker-compose up -d` komutu ile uygulamayı başlatın

## 👥 Katkıda Bulunma

Katkılarınızı memnuniyetle karşılıyoruz! Lütfen önce [katkıda bulunma rehberimizi](CONTRIBUTING.md) inceleyin.

## 📞 İletişim

Sorularınız için lütfen [issues sayfasını](https://github.com/kullaniciadi/norawp/issues) kullanın veya doğrudan iletişime geçin.