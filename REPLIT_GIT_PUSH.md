# Replit'ten GitHub'a Kod Yükleme Rehberi

Replit arayüzü ile projenizi GitHub'a göndermek için şu adımları izleyin:

## 1. Replit'in GitHub Entegrasyonunu Kullanma

1. Replit projenizin sol tarafındaki gezinme menüsünde **"Version control"** (Sürüm Kontrolü) sekmesine tıklayın (git simgesi)

2. İlk kez kullanıyorsanız:
   - "Connect to GitHub" (GitHub'a Bağlan) butonuna tıklayın
   - GitHub hesabınıza izin verin
   - İzinleri onaylayın

3. Bağlantı kurulduktan sonra:
   - **Repository URL** alanına şunu yazın: `https://github.com/norabetcrm/norawp.git`
   - **Branch** olarak `master` ya da `main` seçin
   - "What a diff!" ekranında tüm değişikliklerin listelendiğini göreceksiniz
   - İlk commit için "Commit message" alanına şunu yazın: `WhatsApp Mesaj Gönderim Simülatörü ilk sürüm`
   - "Commit & push" düğmesine tıklayın

## 2. Veya Projeyi İndirip Yerel Olarak Yükleme

Eğer Replit'in GitHub entegrasyonu çalışmazsa:

1. **Projeyi indirin:**
   - Replit'te sağ üstteki menüden "⋮" (üç nokta) simgesine tıklayın
   - "Download as zip" seçeneğini seçin
   - Zip dosyasını bilgisayarınıza indirin ve çıkartın

2. **Git komutlarını kullanarak GitHub'a yükleyin:**
   ```bash
   # İndirdiğiniz klasöre gidin
   cd yol/to/extracted-project
   
   # Git deposu başlatın
   git init
   
   # Tüm dosyaları ekleyin
   git add .
   
   # İlk commit'i yapın
   git commit -m "WhatsApp Mesaj Gönderim Simülatörü ilk sürüm"
   
   # GitHub reposunu ekleyin
   git remote add origin https://github.com/norabetcrm/norawp.git
   
   # GitHub'a gönderin
   git push -u origin master
   # veya
   # git push -u origin main
   ```

3. **GitHub kimlik bilgilerinizi girin:**
   - Kullanıcı adı: GitHub kullanıcı adınız
   - Şifre: GitHub kişisel erişim belirteciniz (token)

## 3. Olası Hata Durumları ve Çözümleri

### Uzak repoda zaten dosyalar varsa:

```bash
# Önce uzak depodaki içeriği çekin ve birleştirin
git pull --allow-unrelated-histories origin master

# Ardından tekrar push yapın
git push -u origin master
```

### Force Push Kullanımı (sadece boş repolarda veya içeriği tamamen değiştirmek istediğinizde):

```bash
git push -f origin master
```

## 4. GitHub'da Doğrulama

Yükleme tamamlandıktan sonra, https://github.com/norabetcrm/norawp adresini ziyaret ederek projenizin başarıyla yüklendiğinden emin olun.