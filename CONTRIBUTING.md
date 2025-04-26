# Katkıda Bulunma Rehberi

## Başlarken

Katkıda bulunmak istediğiniz için teşekkürler! Projeyi geliştirmek için birkaç adım:

1. Projeyi forklayın
2. Yeni bir branch oluşturun (`git checkout -b feature/amazing-feature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Harika özellik eklendi'`)
4. Branch'inizi push edin (`git push origin feature/amazing-feature`)
5. Pull Request açın

## Geliştirme Ortamı

Projeyi yerel geliştirme ortamınızda çalıştırmak için:

1. Repository'yi klonlayın
2. Bağımlılıkları yükleyin: `npm install`
3. `.env.example` dosyasını `.env` olarak kopyalayıp konfigüre edin
4. Veritabanı şemasını oluşturun: `npm run db:push`
5. Geliştirme sunucusunu başlatın: `npm run dev`

## Kod Stilleri

- TypeScript kodları için ESLint kurallarına uyun
- React bileşenleri için functional component ve hooks kullanın
- Tailwind sınıflarını kullanırken şirket stil rehberine uyun

## Dallanma Stratejisi

- `main`: Stabil sürüm
- `develop`: Geliştirme sürümü
- `feature/*`: Yeni özellikler
- `bugfix/*`: Hata düzeltmeleri
- `hotfix/*`: Acil düzeltmeler

## Testler

Yeni özellikler eklerken ilgili testleri de eklemeyi unutmayın. Testleri çalıştırmak için:

```bash
npm run test
```

## Pull Request Süreci

1. PR açmadan önce kodunuzu test edin
2. PR açarken yaptığınız değişiklikleri detaylı olarak açıklayın
3. PR'nizin mevcut testlerle çalıştığından emin olun
4. PR'niz gözden geçirilene kadar sabırla bekleyin