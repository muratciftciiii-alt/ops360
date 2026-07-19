# OPS360 — Operasyon Yönetim Sistemi

OPS360; personel, görev, teslimat, kurulum ve saha operasyonlarını tek bir modern çalışma alanında birleştirmek için hazırlanmış modüler bir web uygulamasıdır. Arayüz tamamen Türkçedir ve masaüstü, tablet ve mobil ekranlara uyum sağlar.

## Kapsam

- Operasyon odaklı genel bakış dashboard'u
- Personel, görev, teslimat ve kurulum modülleri
- Takvim, rapor, doküman ve bildirim alanları
- Kullanıcı profili ve sistem ayarları
- Açık/koyu tema
- Gelecekteki kimlik doğrulama, veri, rol/yetki ve yapay zekâ entegrasyonları için sağlayıcı bağımsız sözleşmeler
- Supabase veya Netlify veri adapter'larının UI katmanını değiştirmeden eklenebileceği backend sınırları

Satış ve muhasebe modülleri bu projenin kapsamına dahil değildir.

## Teknolojiler

- React 19 ve TypeScript
- TanStack Start ve TanStack Router
- Tailwind CSS 4
- Lucide ikonları
- Vite
- Netlify dağıtım altyapısı

## Yerel Çalıştırma

```bash
npm install
npm run dev
```

Uygulama varsayılan olarak Vite geliştirme adresinde açılır. Netlify özellikleriyle yerel çalışmak için Netlify CLI üzerinden geliştirme sunucusu kullanılabilir.

## Proje Yapısı

```text
src/
  components/       Ortak layout ve UI bileşenleri
  features/         Özellik bazlı ekran kompozisyonları
  lib/backend/      Supabase uyumlu servis adapter sözleşmeleri
  routes/           Dosya tabanlı uygulama sayfaları
  styles.css        Tema token'ları ve responsive tasarım sistemi
```

## Dağıtım

Proje `netlify.toml` ve Netlify TanStack Start Vite eklentisi ile dağıtıma hazırdır. Üretim çıktısı `dist/client` dizinine oluşturulur.
