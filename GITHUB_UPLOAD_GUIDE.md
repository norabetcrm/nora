# GitHub'a Yükleme Kılavuzu

Bu kılavuz, WhatsApp Mesaj Gönderim Simülatörü projesini yerel bilgisayarınıza indirip, GitHub'a nasıl yükleyeceğinizi adım adım anlatır.

## 1. Projeyi İndirme

Öncelikle projeyi Replit'ten yerel bilgisayarınıza indirin:

1. Replit'te üst menüden "⋮" (üç nokta) simgesine tıklayın
2. "Download as zip" seçeneğini tıklayın
3. İndirilen ZIP dosyasını bilgisayarınızda bir klasöre çıkartın

## 2. Git Deposu Oluşturma

Projede bir Git deposu oluşturun:

```bash
# Proje klasörüne gidin
cd yol/to/whatsapp-simulator

# Git deposu başlatın
git init

# Tüm dosyaları ekleyin
git add .

# İlk commit'i yapın
git commit -m "İlk commit: WhatsApp Mesaj Gönderim Simülatörü"
```

## 3. GitHub'da Yeni Depo Oluşturma

1. GitHub hesabınızda oturum açın
2. Sağ üst köşedeki "+" simgesine tıklayın ve "New repository" seçin
3. Aşağıdaki bilgileri girin:
   - Repository name: `norawp` (veya istediğiniz bir isim)
   - Description: "WhatsApp Mesaj Gönderim Simülatörü"
   - Visibility: Public veya Private (tercih size kalmış)
   - README dosyası, .gitignore veya lisans ekleme seçeneklerini işaretlemeyin
4. "Create repository" butonuna tıklayın

## 4. Yerel Depoyu GitHub'a Bağlama

GitHub'da repo oluşturduktan sonra, sayfada görünen komutları kullanarak yerel deponuzu GitHub'a bağlayın:

```bash
# Uzak depoyu ekleyin (KULLANICI_ADINIZ yerine GitHub kullanıcı adınızı yazın)
git remote add origin https://github.com/KULLANICI_ADINIZ/norawp.git

# Yerel depoyu uzak depoya gönderin
git push -u origin master
# veya ana dalınız main ise:
# git push -u origin main
```

## 5. GitHub'da Projenizdeki Dosyaları Doğrulama

1. GitHub'da deponuzun sayfasına gidin
2. Tüm dosyaların başarıyla yüklendiğinden emin olun
3. README.md dosyasının düzgün bir şekilde görüntülendiğini kontrol edin

## 6. Yerel Bilgisayarda Kurulum (İsteğe Bağlı)

Projeyi yerel bilgisayarınızda çalıştırmak için:

1. PostgreSQL'i kurun ve yapılandırın:
   ```bash
   # Windows/macOS/Linux için PostgreSQL kurulum adımları işletim sistemine göre değişir
   # Kurulumun ardından veritabanı oluşturun:
   createdb whatsapp_simulator
   ```

2. Proje bağımlılıklarını yükleyin:
   ```bash
   npm install
   ```

3. `.env.example` dosyasını kopyalayarak `.env` dosyası oluşturun:
   ```bash
   cp .env.example .env
   ```

4. `.env` dosyasını düzenleyerek veritabanı bilgilerinizi güncelleyin

5. Veritabanı şemasını oluşturun:
   ```bash
   npm run db:push
   ```

6. Uygulamayı başlatın:
   ```bash
   npm run dev
   ```

## 7. GitHub Actions ile CI/CD (İsteğe Bağlı)

Projede GitHub Actions ile otomatik derleme ve test işlemleri yapılandırılmıştır. `.github/workflows/nodejs.yml` dosyasını düzenleyerek dağıtım adımlarını ihtiyaçlarınıza göre özelleştirebilirsiniz.

## 8. Docker ile Dağıtım (İsteğe Bağlı)

Docker kullanarak projeyi dağıtmak için:

```bash
# Docker imajını oluşturun
docker-compose build

# Uygulamayı başlatın
docker-compose up -d
```

## 9. Heroku Dağıtımı (İsteğe Bağlı)

Heroku ile dağıtım yapmak için:

```bash
# Heroku CLI'yı kurun
npm install -g heroku

# Heroku'ya giriş yapın
heroku login

# Uygulama oluşturun
heroku create norawp-app

# PostgreSQL eklentisi ekleyin
heroku addons:create heroku-postgresql:hobby-dev

# Uygulamayı dağıtın
git push heroku main
```

## 🎉 Tebrikler!

WhatsApp Mesaj Gönderim Simülatörü projeniz artık GitHub'a yüklenmiş ve herkesle paylaşıma hazır durumdadır!