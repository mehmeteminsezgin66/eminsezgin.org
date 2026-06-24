# eminsezgin.org

Demografi, sosyal politika ve aile politikaları üzerine kişisel araştırma sitesi.

**Teknik altyapı:** Quarto + GitHub Pages  
**Görsel kimlik:** Navy (#1F3864) + Gold (#9E7A1A)

---

## KURULUM KILAVUZU

### Adım 1: Yazılım Kurulumu (tek seferlik, ~15 dakika)

Aşağıdaki üç programı sırasıyla kurun. Üçü de "İndir → İleri → İleri → Kur" şeklindedir.

1. **R** — https://cran.r-project.org/bin/windows/base/
   - İndirilen .exe dosyasını çalıştırın, tüm varsayılanları kabul edin.

2. **RStudio Desktop** — https://posit.co/download/rstudio-desktop/
   - "Download RStudio Desktop" butonuna tıklayın, kurun.

3. **Quarto** — https://quarto.org/docs/get-started/
   - İşletim sisteminize uygun versiyonu indirip kurun.

4. **GitHub Desktop** — https://desktop.github.com/
   - İndirip kurun. GitHub hesabınızla giriş yapın.
   - (Hesabınız yoksa: https://github.com/join adresinden ücretsiz açın.)

### Adım 2: R Paketlerini Yükleme (tek seferlik, ~5 dakika)

RStudio'yu açın. Alt soldaki "Console" bölümüne şunu yapıştırıp Enter'a basın:

```r
install.packages(c("plotly", "htmlwidgets"))
```

Kurulum tamamlanana kadar bekleyin.

### Adım 3: GitHub Repository Oluşturma

1. GitHub Desktop'ta: File → New Repository
2. Name: `eminsezgin.org`
3. Local Path: İstediğiniz bir klasör (örn. Belgelerim)
4. "Create Repository" tıklayın.
5. Oluşan klasöre bu projedeki TÜM dosyaları kopyalayın.
6. GitHub Desktop'a dönün → tüm dosyalar "Changes" sekmesinde görünecek.
7. Sol altta "Initial commit" yazıp "Commit to main" butonuna basın.
8. Üstte "Publish repository" butonuna basın (Public olarak).

### Adım 4: GitHub Pages'i Etkinleştirme

1. Tarayıcıda: github.com → repository'nize gidin → Settings sekmesi.
2. Sol menüden "Pages" tıklayın.
3. "Source" altında "GitHub Actions" seçin.
4. Kaydedin. İlk build birkaç dakika sürecek.
5. Tamamlandığında siteniz `https://KULLANICIADI.github.io/eminsezgin.org` adresinde yayında olacak.

### Adım 5: Alan Adı Bağlama

1. **Alan adı satın alın:** Namecheap, Google Domains veya Cloudflare'dan `eminsezgin.org` satın alın (~$10-12/yıl).
2. **DNS ayarları:** Alan adı sağlayıcınızda şu kayıtları ekleyin:
   - Tip: CNAME, Host: www, Value: `KULLANICIADI.github.io`
   - Tip: A, Host: @, Value: `185.199.108.153`
   - Tip: A, Host: @, Value: `185.199.109.153`
   - Tip: A, Host: @, Value: `185.199.110.153`
   - Tip: A, Host: @, Value: `185.199.111.153`
3. **GitHub'da:** Repository → Settings → Pages → Custom domain → `eminsezgin.org` yazıp Save.
4. "Enforce HTTPS" kutusunu işaretleyin.
5. DNS yayılması 10 dakika - 24 saat sürebilir.

---

## YENİ İÇERİK EKLEME

### Yeni yazı eklemek:
1. RStudio'da `yazilar/` klasörüne sağ tıklayın → New File → Quarto Document.
2. Visual editörde (üstte "Visual" sekmesi) yazınızı yazın.
3. Dosyanın başındaki YAML bölümünü doldurun (tarih, başlık, kategori).
4. Kaydedin.
5. GitHub Desktop'a geçin → Changes'taki dosyayı Commit edin → Push.
6. Site 2-3 dakika içinde otomatik güncellenir.

### Mevcut içeriği düzenlemek:
1. İlgili `.qmd` dosyasını RStudio'da açın.
2. Değişikliği yapın, kaydedin.
3. GitHub Desktop → Commit → Push.
