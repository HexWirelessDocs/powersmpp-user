---
tags:
  - FAQ
  - Help
---

# Sık Sorulan Sorular

Power SMPP hakkında ortak sorular için hızlı cevaplar bulun.

---

## Başlanmaya başladı

??? question "Kullanıcı paneline nasıl giriş yapıyorum?"
 Yöneticiniz tarafından sağlanan Power SMPP örneği URL'nize kaydolun. Enter your your your Enter your **Username** ve **Şifre Şifre** iText Hub kullanıcı paniğe erişmek için.

 Bilgilerinizi unutmuşsanız, sistem yöneticisine parola sıfırlama için ulaşın. Güvenlik için, ilk girişinizin ardından şifrenizi değiştirmeniz önerilir **Ayarlar > Change Password**.

??? question "Panel şovu nedir?"
 Panel (iText Hub), dört anahtar ölçümleri ile mesajlaşma aktivitenizin gerçek zamanlı bir genel bakışını sağlar:

    - **SMS Sent Bugün** - Mevcut günde tüm arayüzlerden gönderilen toplam SMS mesajları
    - **Bugün teslim edildi** - Mevcut günde başarıyla teslim edilen toplam SMS mesajları
    - **SMS Sent Dün** Önceki gün gönderilen mesajlar
    - **Dün teslim oldu** Önceki gün teslim edilen mesajlar

 Ayrıca her ikisi için de interaktif trafik izleme grafiklerini gösterir **MT (Mobile Terminated / giden)** ve **MO (Mobile Originated / incoming)** mesajlar. Panodan, hızlı bir şekilde kampanya oluşturma, iletişim yönetimi, trafik görüntüleme, rapor indirmeleri ve profil ayarları erişebilirsiniz. [Dashboard](user/dashboard/dashboard.md) Daha fazla ayrıntı için.

??? question "Şifremi nasıl değiştiririm?"
    1. Go to Go to Go to Go **Ayarlar > Change Password**
    2. Enter your your your Enter your **Geçerli şifre** doğrulama için
    3. Enter your your your Enter your **Yeni şifre** ( Yöneticiniz tarafından belirlenen güvenlik gereksinimleriyle tanışın)
    4. **Onay Onay Onay Onaylandı** Yeni şifre
    5. Click Click Click Click Click **Kaydet Kaydet Kaydet**

 Düzenli şifre güncellemeleri, hesap güvenliğini korumak ve en iyi uygulamalarla uyum sağlamak için önerilir. Yöneticiniz ayrıca periyodik güncellemeler gerektiren bir şifre değişikliği politikası uygulayabilir. [Değişim Şifresi](user/settings/changepassword.md).

??? question "Profil bilgilerimi nasıl güncelliyorum?"
 Go to Go to Go to Go **Ayarlar > Profilim** Aşağıdaki alanları güncelleyebilirsiniz:

    - **İlk Adı** - Ebeveynlerinizin invoicing için referans
    - **Mobile Number** - Hesap iletişimi ve doğrulama için kullanılır
    - **Ülke Kodu** - "Auto-add country code" seçeneği aracılığıyla kampanya numaralarına otomatik olarak uygulanabilir
    - **E-posta ID** İletişim, uyarılar, OTP ve bildirim teslimatları için kullanılır
    - **Ülke / Devlet** - Fatura ve referans amaçları için
    - **Timezone** — Kampanya zamanlaması ve raporları dahil olmak üzere tüm tarih/zaman ekranlarını etkiler

 Click Click Click Click Click **Kaydet Kaydet Kaydet** Değişiklikler yaptıktan sonra. [Benim Profilim](user/settings/myprofile.md).

??? question "Hangi zaman bölgesi platformu kullanıyor?"
 Platform, zaman Bölgesi'ni sizin tarafınızda yapılandırıyor **Profilim** ayarlar. Bu zaman bölgesi etkiler:

    - Dashboard metrics display
    - Kampanya planlama
    - Rapor tarihi/zaman damgaları
    - Mesaj count raporları

 Zaman bölgenizi her zaman alıcılarınız için amaçlanan zamanda gönderilmelerini sağlamak için zaman aralığınızı doğrulayın.

??? question "MT ve MO mesajları arasındaki fark nedir?"
    - **MT (Mobile Terminated)** - Mesajlar gönderildi **toklanmak için** Bir mobil elet. Bunlar sizin dışı / devam eden mesajlarınızdır (örneğin, kampanyalar, bildirimler, OTPs).
    - **MO (Mobile Originated)** - Mesajlar gönderildi **From from from from from from from from from from from from from from from from from from from from from from from from from from from from from from from from from from** Bir mobil elet. Bunlar, alıcılarınızdan alınan (örneğin, yanıtlar, opt-out talepleri).

 Hem MT hem de MO trafiği pano haritalarınız üzerinde gösteriliyor.

---

## SMS gönder

??? question "Bir SMS kampanyası nasıl oluşturup gönderiyorum?"
 SMS kampanyası oluşturmak ve göndermek için bu adımları izleyin:

    1. Click Click Click Click Click **SMS MT** Boş SMS sayfasını açmak için
    2. A girin a **Kampanya Adı** (auto- set "Camp " ve tarih-zaman ile veya özel bir isim girin)
    3. Select a Select a Select **Sender ID** Onaylanmış listeden (veya "Open Sender ID" nin yöneticiniz tarafından etkinleştirildiği bir dinamike gir)
    4. **Ek alıcılar ekleyin** Dört yöntemden birini kullanarak:
        - **Stored Grupları** - Pre-created temas gruplarından seçin
        - **Yerel Dosya** – Bir Excel/CSV dosyasını telefon numaraları ile yükleyin
        - **Manual Giriş** - Tip numaraları doğrudan ( ülke kodu ile eşleştirilir, + sembolü yoktur)
        - **Copy-Paste** - Başka bir kaynaktan gelen Paste numaraları
    5. **Mesajınız** Metin kutusunda (veya taslaklardan / işaretlerden seçilir)
    6. Seçmeli olarak etkinleştirin **Flash SMS SMS** için anlık ekran görüntüsü
    7. Sistem sistemi **Auto-detects Unicode** Özel karakterler kullanılırsa kullanılır
    8. Seçmek için **Şimdi Gönder** veya **Schedule Schedule** Daha sonra için
    9. Click Click Click Click Click **SMS gönder** - son onay önce bir maliyet önizlemesi gösterilir

    !!! tip
 Her zaman mesajınızı büyük ölçekli kampanyalar çalıştırmadan önce birkaç sayı üzerinde test edin, karakter sayaçları tarayıcı/encoding varyasyonları nedeniyle yaklaşıkdır.

 [Compose SMS](user/smsmt/compose.md) Tam rehber için.

??? question "Bir Excel dosyasından kişiselleştirilmiş SMS nasıl gönderiyorum?"
 Excel özelliğinden gelen SMS, web sitenizi kullanarak kişiselleştirilmiş mesajlar göndermenize olanak sağlar:

    1. Açıklayın **SMS From Excel** sekmesi
    2. Download the Download the Download the **Örnek dosya dosyası** Gerekli formatı görmek için "View Sample" sekmesi aracılığıyla
    3. Excel dosyasını bir sütunda ve kişiselleştirme verileri ile hazırlayın (isimler, miktarlar, tarihler vs.) diğer sütunlarda
    4. **download** Excel dosyası - en üst 5 satır doğrulama için gösterilir
    5. **Köşeyi seçin** Mobil sayılar içeren
    6. A girin a **Sender ID**
    7. Mesajınızı yazın ve tıklayın **"Insert Placeholder"** Ortam sütunlarından dinamik değişkenler eklemek (örneğin, <span data-ph="0"></span>, <span data-ph="1"></span>)
    8. Click Click Click Click Click **Öfke** En iyi 5 kişiselleştirilmiş mesajları karakter sayısı ile görmek
    9. Seçmek için **Schedule Schedule** veya **Şimdi Gönder**
    10. Yorum yapın **Son önizleme ekranı** Ülkeye göre maliyet bozulması
    11. Click Click Click Click Click **Send Send Send Gönder**

 Bu, randevu hatırlatmaları, sipariş onayları veya ödeme bildirimleri gibi kişiselleştirilmiş içerik için idealdir. See [SMS From Excel](user/smsmt/smsfromexcel.md).

??? question "İletişim yüklemeleri için hangi dosya formatları desteklenir?"
 Power SMPP, iletişim yüklemeleri için aşağıdaki dosya formatlarını destekler:

    | Format Format | Extension Extension Extension | Vaka Kullanımı |
    |--------|-----------|----------|
    | Excel Excel | .xls, .xlsxls | Çoğu yaygın, birden çok sütunu destekler |
    | Kataloğu | .csv | Hafif, evrensel uyumluluk |
    | Text Text Text Text | .txt | Basit sayı listeleri liste listeleri |

 **Gereksinimler:**

    - Telefon numaraları içermelidir **ülke kodu** (e.g., 919909945175, +9199045175)
    - Do Do Do Do Do Do **Değil değil** Kullanımı <span data-ph="0"></span> Ülke kodundan önce sembolü
    - Ek sütunlar kişiselleştirme verilerini (isimler, miktarlar vs.) içerebilir.
    - Yüklemeden sonra sistem otomatik sütunları

??? question "Flash SMS nedir ve ne zaman kullanmalıyım?"
 Flash SMS, özel bir mesaj türüdür, **Doğrudan alıcının ekranında hemen görünüyor** Gelen kutularında saklanmadan. Mesaj, ellerde bir popup overlay olarak gösteriliyor.

 **Flash SMS kullanırken:**

    - Acil uyarılar ve acil bildirimleri
    - Acil dikkat gerektiren zaman hassas bilgiler
    - OTP'nin kurtarılması gereken kodları
    - Eleştirel sistem bildirimleri

 **Nasıl etkinleştirilir:** Check the Check the **Flash SMS SMS** Mesajınızı Boş SMS sayfasında oluştururken çekbox. Flash SMS davranışının alıcının el ve taşıyıcısına bağlı olarak değişebilir unutmayın.

??? question "Unicode / özel karakter tespiti nasıl çalışır?"
 Power SMPP **Otomatik olarak algılar** Mesajınız Unicode karakterleri içerdiğinde. İşte nasıl çalışır:

    - **GSM 7-bit encoding** (default): Standart İngilizce mektupları, sayıları ve temel sembolleri destekler. Limit: **160 karakter** SMS segmenti başına.
    - **Unicode encoding** (auto-detected): Latince olmayan senaryolar (Arapça, Hindi, Çince, vs.), emojiler veya özel karakterler tespit edilir. Limit: **70 karakter** SMS segmenti başına.

 **Önemli:** Unicode tespit edildiğinde, karakter karşı güncellemeler otomatik olarak. Tek bir emoji veya özel bir karakter Unicode encoding'e tüm mesajı değiştirir, segment başına mevcut karakterleri azaltır.

    !!! warning
 Gösterilen mesaj ve karakter sayacı **Indicative only indicative only** Tarayıcı ve kodlama varyasyonları nedeniyle. Her zaman büyük kampanyalardan önce küçük bir toplu test edin.

??? question "SMS başına karakter sınırı nedir ve nasıl koncatenasyon çalışması yapılır?"
 **SMS segmentinde Karakter sınırları:**

    | Encoding | Tek SMS | Concatenated SMS (per segment) |
    |----------|-----------|-------------------------------|
    | GSM 7bit (standart) | 160 karakter | 153 karakter |
    | Unicode | 70 karakter | 67 karakter |

 Bir mesaj tek SMS limitini aştığında, otomatik olarak otomatik olarak bölünür **(multi-part) SMS**Her ek segment biraz daha az karakter kullanır (153 veya 67), çünkü bazı astes parçalara nasıl yeniden kurulacağını söyleyen koncatenasyon başlığı için ayrılmıştır.

 **Örnek: Örnek:** 320-karacter GSM mesajı = 3 SMS segmentleri (153 + 153 + 14 karakter). Segment başına faturalandınız.

??? question "Daha sonra bir kampanya nasıl planlıyorum?"
    1. SMSinizi hesaplamak ( Excel'den SMS veya SMS almak), seçin **Schedule Schedule** seçenek seçeneği
    2. İstediğinizi seçin **tarih ve zaman**
    3. Doğruyu seçin **Zaman Bölgesi** ( profilinize zaman bölgesine)
    4. Kampanya kurulumunun geri kalanını tamamlayın ve tıklayın **Send Send Send Gönder**
    5. Kampanya kuyruklanacaktır ve planlanan zamanda otomatik olarak gönderilir.

 **Planlanan kampanyaları yönetmek:**

    - Go to Go to Go to Go **Rapor > My Schedules** Tüm planlanan kampanyaları görmek için
    - Yapabilirsiniz **reschedule** Beklenmeyen bir kampanyaya tıklayarak **Edit** Action sekmesinde
    - Her zaman seçilmiş zaman Bölgesi, amaçlanan teslimat saatinizi doğrulayın

 [My Schedules](user/report/schedule.md).

??? question "Taslaklar ve Şablonlar arasındaki fark nedir?"
    | Özellik | Taslaklar | Şablonlar |
    |---------|--------|-----------|
    | **Editability** | Tamamen düzenlenebilir - tüm içeriği değiştirebilirsiniz | Sadece yer sahipleri değiştirilebilir; statik içerik kilitli |
    | **Onay Onay** | Hiçbir onay gerekli | Kullanılmadan önce yönetici onayı gerektirebilir |
    | **Use case** | İş kodlama mesajları | Reusable, onaylanmış mesaj formatları |
    | **Uyumluluk** | Hiçbir uyum sağlama | DLT-compliant (Hindistan için) |

 **Taslaklar** Hala üzerinde çalıştığınız mesajları kurtarmak için idealdir. **Şablonlar** Standart, önceden onaylanmış mesajlar için idealdir, tutarlı format tutmalıdır.

    !!! warning "API Kullanıcılar"
 API aracılığıyla şablonları kullanırken, tam spacing, commas ve punctuation maçlarını onaylanan şablonla karşılayın. Biçimlendirmedeki herhangi bir tutarsızlık, şablonda geçersiz olarak reddedilebilir.

??? question "Bir ülke kodu otomatik olarak tüm sayılara ekleyebilir miyim?"
 Evet. İki yol vardır:

    1. **Kampanya kompozisyonu sırasında** - Check the **"Auto-add country code"** Alıcıları ekliyorken çekbox. Sistem, yapılandırılan ülke kodunu tüm sayılara önleyecek.
    2. **Profilinizde** - Go to **Ayarlar > Profilim** ve varsayılan olarak yapılandırın **Ülke Kodu**. Bu ayar, oto-add seçeneği etkinleştirildiği zaman kullanılır.

 Bu, iletişim listesiniz ülke önceden ek olmadan yerel sayılar içerdiğinde faydalıdır.

---

## Sender ID & Şablonlar

??? question "Yeni bir Sender kimliği nasıl talep ediyorum?"
    1. Go to Go to Go to Go **SMS MT > Yönetici Gönderer ID**
    2. Click the Click the **"Add Sender ID"** sekmesi
    3. Bir yapılandırma popup görünüyor - istenen Sender kimlik bilgilerini yöneticinizin yönergelerini takip edin
    4. Click Click Click Click Click **Kaydet Kaydet Kaydet**
    5. Sender ID bir girer **Beklenmeyen onay** devlet devleti devlet devleti
    6. Yönetici yorumlarınız ve onaylarınız / istekleri onaylar
    7. Onaylandıktan sonra, Sender ID, kampanya yaparken düşüşünüzde görünüyor

 görebilirsiniz **onay durumu** Tüm Sender kimliklerinizin Yönetimi Sender ID listesinde. Hesabınız varsa **"Open Sender ID"** Yönetici tarafından etkinleştirin, bu adımı atabilirsiniz ve herhangi bir Sender ID doğrudan hesaplama yaparken. [Manage Sender ID](user/smsmt/managesenderid.md).

??? question "Mesaj şablonlarını nasıl yaratırım ve yönetirim?"
    1. Go to Go to Go to Go **SMS MT >Data Template**
    2. Click the Click the **"Add Template"** sekmesi
    3. Şablon adı girin ve içeriği oluşturun
    4. Click Click Click Click Click **"Insert Placeholder"** Kişiselleştirme için dinamik değişkenler eklemek (örneğin, <span data-ph="0"></span>, <span data-ph="1"></span>)
    5. Click Click Click Click Click **Kaydet Kaydet Kaydet** - şablon yönetici onayı gerektirebilir

 **Onaydan sonra:**

    - **Statik içerik** (Yer sahipleri hariç her şey kilitli ve değiştirilemez
    - Sadece Sadece Sadece Sadece Sadece Sadece **yer sahibi değerler** Kampanyayı kampanyalarda kullanırken değiştirilebilir
    - Listedeki tüm şablonlar için onay durumunu görebilirsiniz

    !!! warning "API kullanıcıları için önemli"
 API aracılığıyla şablonları kullanırken, emin olun **kesin kesin kesin** Spacing, commas, punctuation, and formatting match the correct template. Küçük bir tutarsızlık bile şablonun geçersiz olarak tedavi edilmesine neden olabilir ve mesaj reddedilebilir.

 Hesabınız varsa **"Açık Şablon"** etkinleştirin, şablon yapılandırmasını atlayabilirsiniz. [Manage Şablonu](user/smsmt/managetemplate.md).

??? question "DLT nedir ve neden şablonu/Sender ID onayı gereklidir?"
 **DLT (Distributed Ledger Teknolojisi)** Tarafından verilen bir düzenleyici çerçeve **TRAI (Hindistan'ın Televizyon Düzenlemesi)** Hindistan'da tüm Uygulama-Person (A2P) mesajlaşma için.

 **Anahtar gereksinimleri:**

    - Bütün Bütün Hepsi **Sender IDs** DLT platformunda kayıtlı olmalıdır
    - Bütün Bütün Hepsi **Mesaj şablonları** Daha önce DLT üzerinde önceden onaylanmalı
    - Onaylanmış şablonlarla eşleşmeyen mesajlar operatörler tarafından engellenebilir
    - Bu, Hindistan'da gönderilen tüm ticari ve işlemsel SMS için geçerlidir

 **Neden var:**

    - Boş olmayan ticari iletişimi azaltır (spam)
    - Tüketicileri sahte mesajlardan korumak
    - Tüm A2P mesajlaşma için denetim edilebilir bir iz oluşturun
    - Telecom operatörleri için düzenleyici uyum sağlayın

 Eğer Hindistan dışında çalışırsanız, DLT geçerli olmayabilir, ancak yöneticiniz hala kalite kontrolü için şablon onayını alabilir.

??? question "Gönderer ID veya şablonum reddedilirse ne olur?"
 Sender ID veya şablonunuz yöneticiniz tarafından reddedilirse:

    - Durum gösterecek **Rejected** İlgili yönetim sayfasında
    - Bir yaratmanız gerekecek **Yeni istek** düzeltilmiş ayrıntılarla
    - Ortak reddedilme nedenleri şunlardır: olmayan içerik, yanlış formatlama, tekrar girişler veya politika ihlalleri
    - Belirli reddedilme nedenleri ve yönergeleri için yöneticinize ulaşın

---

## İletişim İletişim İletişim

??? question "İletişim grupları nasıl yaratırım ve yönetirim?"
 **Bir grup oluşturmak:**

    1. Go to Go to Go to Go **İletişim > Yönetim Grupları**
    2. Click Click Click Click Click **Ekle Grup Ekle**
    3. Bir grup adı girin ve tasarruf edin

 **Mevcut grupları yönetmek - mevcut eylemler:**

    | Eylem | Açıklama |
    |--------|-------------|
    | **Edit Group Name** | Rename an existing group |
    | **Bulk Import İletişim İletişim** | Bir dosyadan bir kez birden fazla temas ekleyin |
    | **Boş Grup** | Tüm temasları kaldır ama grubu tut |
    | **Delete Group** | Sürekli olarak grubu ortadan kaldırır ve tüm temaslar |

 Gruplar alıcıları organize etmek ve hızlı bir şekilde onları hesaplamak için seçerler. Görsün [Manage Grupları](user/contacts/managegroups.md).

??? question "Nasıl iletişim kuruyorum?"
 Power SMPP teklifleri sunuyor **Üç ithalat yöntemi**:

 **Yöntem 1: Bir Dosyadan İthalat**

    - Büyük veri kümeleri için en iyisi
    - Destekler **.xls**, **.csv**Ve **.txt** format format format format format format format format format format format format format format format format format format format format format format format format format format format format
    - Hedef grubu seçin, dosyayı yükleyin ve onaylayın

 **Yöntem 2: Kopya ve Paste**

    - Hızlı ve esnek
    - Doğrudan bir Excel sayfası veya diğer kaynaktan kopyala
    - Giriş alanına yapıştırın

 **Method Manual 3: Giriş**

    - Bir kişi tarafından birini ekleyin
    - Küçük sayıda temas için en iyisi

 **Adımlar:**

    1. Seç **Hedef grubu** Ölmüşlerden
    2. import yöntemini seçin
    3. İletişimlerinizi ekleyin
    4. Click Click Click Click Click **Done** İthalatı doğrulamak için

 [İmport İletişimi](user/contacts/importcontacts.md).

??? question "Nasıl temasa geçtim?"
    1. Go to Go to Go to Go **İletişim > İhracat İletişimi**
    2. Seç **Grup(s)** checkboxes kullanarak ihracat yapmak istiyorsunuz
    3. Click Click Click Click Click **İhracat İhracatı**
    4. Tercih ettiğiniz formatı seçin:
        - **.xls** - Excel format
        - **.csv** — Comma-separated values
        - **.txt** - Plain text
    5. ihraç edilen dosyayı indirin

    !!! tip
 Yalnızca yönetilebilir dosya boyutları için ihtiyacınız olan gruplar. Sistem arasındaki yedek amaçlar veya migrating kontakları için ihracat kullanın.

 [Export İletişimi](user/contacts/exportcontacts.md).

---

## Raporlar Raporları Raporlar Raporlar Raporları

??? question "Kampanya raporlarını nasıl görüyorum?"
 Go to Go to Go to Go **Rapor > Kampanya Raporu** Birden çok görüşe sahip olduğunuz yerde:

 **Kampanya View:**

    - Tüm kampanyaların listesi
    - Kampanya durumu, teslimat oranları, yürütme tarihleri ve anahtar istatistikler göster
    - Ayrıntılara döşemek için bir kampanyaya tıklayın

 **Liste View:**

    - DLR (Delivery Receipt) mesaj seviyesinde ayrıntılı rapor
    - Bireysel mesaj teslimat durumu gösterir

 **Kampanya durumu:**

    - Gerçek zamanlı mesaj kuyruk takip
    - Tamamlanan ve bekleyen teslimatlar

 **Eylemler Tab:**

    - Teslim edilen mesaj sayısı
    - Pending message count
    - Başarısız mesaj sayısı
    - Diğer durum kategorileri

 Filtre Tarafından **tarih aralığı** Belirli kampanyalar bulmak için. [Campaign Report](user/report/campaign.md).

??? question "DLR durumları ne anlama geliyor?"
 DLR (Delivery Report) durumları her mesajın teslim sonucunu göstermektedir:

    | Durum durumu | Anlam | Eylem |
    |--------|---------|--------|
    | **Teslimat teslim edildi** | Mesaj, alıcının ellerine başarıyla teslim oldu | Hiçbir eylem gerekli değildi |
    | **Başarısızlık** | Mesaj teslim edilemez (tavalid sayısı, ağ sorunu, bloke veya DND) | Sayı geçerliliğini kontrol edin; listeden kaldırmayı düşünün |
    | **Pending Pending** | Operatöre gönderilen mesaj ancak teslimat onayı henüz almadı | Bekle – durum güncellenebilir; bazı operatörler DLR'leri geciktirebilir |
    | **Queued** | Mesaj, sistemde işlenmek ve gönderilmek için bekliyor | İşleme için bekleyin |
    | **Rejected** | Mesaj operatör veya ağ geçidi tarafından reddedildi | Kontrol şablonu uyumluluğu, gönderici ID veya içerik kısıtlamaları |

    !!! tip
 Kullanın **Mesaj Count** Bir tarih aralığı üzerinde bir statüye göre özet almak ve kullanmak için rapor **Download Report** ayrıntılı Excel ihracat için.

??? question "Mesaj sayımı raporlarını nasıl görüyorum?"
    1. Go to Go to Go to Go **Rapor > Mesaj Count**
    2. Select a Select a Select **tarih aralığı** veya spesifik **ay ay**
    3. Görme mesajı statü tarafından kırıldı (Öyle, Pending, Başarısız, vs.)
    4. Click the Click the **hiperlink** Bir ay içinde, bir ay içinde, **gün çöküntü**

 Rapor, yapılandırılmış zaman bölgenize göre sayılır. Hedef trafik analizi için tarih aralığı ve durum filtreleri kullanın. [Message Count](user/report/messagecount.md).

??? question "Excel formatında raporları nasıl indirebilirim?"
    1. Go to Go to Go to Go **Rapor > Download Report**
    2. Listeyi görüntüle **Daha önce talep edilen raporlar** (Eğer varsa)
    3. Click Click Click Click Click **İstek Raporu** Yeni bir rapor oluşturmak için
    4. Rapor girer **Pending Pending** Sistem verileri getirdiğinde durum
    5. Bir kez işleme tamamlandıktan sonra, statü değişiklikleri **Hazır Hazır Hazır Hazır**
    6. Rapora tıklayın **download indir** Excel (.xls) formatında

 Raporlar ayrıntılı mesaj seviyesi verileri içerir: alıcı numarası, durum, zamantamps, maliyet, gönderici ID ve daha fazlası. See [Download Report](user/report/downloadreport.md).

??? question "Bir kampanyadan başarısız mesajları geri alabilir miyim?"
 Evet, ama koşullarla:

    1. Kampanyayı açın **Kampanya Raporu**
    2. Git **Resend** sekmesi
    3. Başarısız veya bekleyen mesajları tekrarlamak için seçin

 **Sorumluluk kuralları:**

    | Scenario | Resend kullanılabilir mi? |
    |----------|-------------------|
    | Executed kampanya (resmi) | Evet Evet Evet |
    | Kampanya hala kuyrukta | Hayır hayır hayır |
    | Uzun mesajlar hala işleme | Hayır hayır hayır |

    !!! tip
 Raporu indirin **Daha önce resending** Hedef listesini doğrulamak ve zaten mesajı almış olabilecek sayılara tekrar teslimatlardan kaçınmak.

??? question "Bir koşu kampanyasını nasıl durduracağım?"
    1. Go to Go to Go to Go **Rapor > Kampanya Raporu**
    2. Aktif kampanyayı bulun
    3. Click the Click the **Dur Dur Dur Dur Dur** düğme düğmesi

 **Önemli:**

    - Mesajlar **Zaten çoktan gönderildi zaten** hatırlanamaz
    - Sadece Sadece Sadece Sadece Sadece Sadece **Kalan kuyruk mesajları** iptal edilecek
    - Bu eylem derhal ve geri alınamaz
    - Kampanya içerikinizde bir hata keşfettiğinizde veya acilen teslimatı durdurmanız gerektiğinde bunu kullanın

??? question "Beklemek bir kampanyayı nasıl reschedule ediyorum?"
    1. Go to Go to Go to Go **Rapor > My Schedules**
    2. Reschedule'i yeniden almak istediğiniz kampanyayı bulun
    3. Click the Click the **Edit** Action sekmesinde
    4. Yeni seçin **Zaman Bölgesi**
    5. Yeni setleri ayarlayın **Tarih ve Zaman**
    6. Click Click Click Click Click **Kaydet Kaydet Kaydet**

 Kampanyanın alıcılarınız için doğru yerel zamanda gönderilmesini sağlamak için her zaman seçilen zaman bölgesini doğrulayın. [My Schedules](user/report/schedule.md).

---

## WhatsApp WhatsApp WhatsApp

??? question "WhatsApp Business hesabımı nasıl bağlarım?"
 **Önlemler:**

    - Doğrulanmış bir **Facebook Business** Hesap hesabı
    - A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A **WhatsApp Business Profile** Facebook hesabınızla bağlantılı

 **Adımlar:**

    1. WhatsApp bölümüne geçiş
    2. Click Click Click Click Click **"Facebook'u kullanarak bağlantı"**
    3. Bir diyalog kutusu görünür - Facebook hesabınızı iTextPro ile kayıt edin
    4. Create or link your your link your **WhatsApp Business Profile** (Bu Meta ve iTextPro arasındaki köprü olarak hareket eder)
    5. ITextPro içindeki WhatsApp mesajlaşma ayarları

 Bağlandığında, şablonlar, kampanyalar oluşturmaya başlayabilir ve müşteri desteği için Team Inbox kullanabilirsiniz. [Başlangıç başladı](plugins/whatsapp/whatsappuser/overview.md).

??? question "Bir WhatsApp kampanyası nasıl yaratıyorum?"
    1. Click the Click the **Kampanya Kampanyası** WhatsApp bölümündeki düğme
    2. **Sender Nameer Name** Aşağıdan (düşmanlara)
    3. **Ek alıcılar ekleyin** Üç yöntemden birini kullanarak:
        - **Manual Giriş** - Tip mobil sayılar doğrudan
        - **İthalat İletişim** – Bir Excel /CSV dosyasını yükleyin
        - **Mevcut grupları kullanın** - Pre-created temas grupları seçin
    4. Click Click Click Click Click **"Use Template"** Ve önceden onaylanmış bir şablon seçin
    5. **Mesajı özelleştirin:**
        - Gerekirse kafayı değiştirin
        - Dinamik değişkenleri değiştirin ({{1}= {{2}Tamam, vs.) gerçek değerlerle
        - A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A A **Gerçek zamanlı önizleme** Sağ tarafta görünür
    6. Seçmek için **Schedule Schedule** ( kutuyu kontrol edin ve tarih/zaman) veya **Şimdi Gönder**
    7. Click Click Click Click Click **Send Send Send Gönder**

 Sadece Sadece Sadece Sadece Sadece Sadece **Meta onaylı şablonlar** Düzenleyici uyum sağlamak için kullanılabilir. [Campaign](plugins/whatsapp/whatsappuser/campaign.md).

??? question "WhatsApp şablon kategorileri nedir ve bir tane nasıl yaratırım?"
 WhatsApp şablonları Meta tarafından üç türe kategorize edilir:

    | Kategori Kategori | Amaç | Örnekler |
    |----------|---------|---------|
    | **Pazarlama Pazarlama Pazarlama** | Birden çok alıcıya promosyon mesajları | Teklifler, ürün fırlatma, haber |
    | **Çözüm** | Zaman zaman alışveriş/müşteri yolculuğu ile ilgili güncelleştirmeler | Sipariş onayı, nakliye güncelleştirmeleri, randevu hatırlatmaları |
    | **Kimlik Doğrulama** | OTP ve doğrulama mesajları | Giriş kodları, hesap doğrulama kodları |

 **Bir şablon oluşturmak:**

    1. Go to Go to Go to Go **WhatsApp > Şablon**
    2. Seç **kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori kategori** (Marketing, Utility veya Authentication)
    3. Seç **dil dili** (Meta birçok dili destekler)
    4. **Add Header** (İsviçre): Hayır, Text veya Media (image, video, belge, yer)
    5. **Body Add Body**: Değişkenlerle Değişkenlerle Ana mesaj içeriği Değişken düğme (format: {{1}= {{2}= {{3})
    6. Provide Provide Provide provide **örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler örnekler** Her değişken için ( Meta'nun anlamasına ve daha hızlı onaylamasına yardımcı olur)
    7. **Add Footer** (optional): Marka metni veya feragatname
    8. **Ek Özellikler Ekle** (İsviçre):
        - **Opt-Out Düğme** - Unsubscribe seçeneği
        - **CTA Düğmeleri** – Web Sitesini ziyaret edin ( 2) veya Telefon Numarası çağırın
    9. Click Click Click Click Click **Taslak Olarak Kaydet** (edit later) veya **Kaydet ve gönder** Meta onayı için

 Onay genellikle bir tane alır **Birkaç saniye**Onaylandıktan sonra, önyükleme, düzenleme (kesinlikle geri ödeme), silinebilir veya doğrudan şablondan bir kampanya başlatabilirsiniz. [Template](plugins/whatsapp/whatsappuser/template.md).

??? question "Team Inbox'ı müşteri desteği için nasıl kullanırım?"
 Team Inbox, WhatsApp konuşmalarını yönetmek için merkezi bir platformdur:

 **Adminler için:**

    - Tam görünürlük **Tüm sohbetler** (hem insan ajanı hem de sohbet konuşmaları)
    - **Instant Takeover** Hızlı sorun çözümü için devam eden herhangi bir konuşma
    - Arama ve filtre konuşmaları

 **Agents için:**

    - Her ajan için benzersiz giriş kimlikleri
    - Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to Access limited to **atanan sohbetler** Sadece sadece sadece sadece sadece sadece sadece sadece sadece sadece sadece sadece
    - Gerçek zamanlı müşterilere yanıt verin

 **Anahtar özellikler:**

    - Bir yerde tüm WhatsApp etkileşimlerinin merkezileştirilmesi
    - Admin tırmanma yeteneği arttı
    - Gizlilik ve veri koruma sağlamak için benzersiz girişlere güvenli erişim
    - Hızlı sohbet görünümü için Arama ve filtre

 [Takım Inbox](plugins/whatsapp/whatsappuser/teaminbox.md).

??? question "Ajan hesaplarını nasıl yaratırım ve yönetirim?"
 Agent hesapları destek ekibiniz için bireysel giriş erişim sağlar:

    1. Go to Go to Go to Go **WhatsApp > Agent Hesapları ile Takım**
    2. Click Click Click Click Click **Yeni Agent ekle**
    3. Gerekli ayrıntılarda doldurun
    4. Click Click Click Click Click **Kaydet Kaydet Kaydet** - Ajan hesabı anında oluşturulur

 **Bireysel ajan hesaplarının Faydaları:**

    - **Geliştirilmiş Takım Yönetimi** - Farklı konular veya müşteri segmentleri için özel gruplar oluşturun
    - **Geliştirilmiş Güvenlik** - yetkili ajanlara erişimi sadece yetkili ajanlara erişimi
    - **Artan Hesapability** Bireysel ajan performansını izleyin ve zaman zaman zaman yanıt
    - **Flex Shift Scheduling** Farklı geçişler veya zaman bölgeleri için ayrı hesaplar

 [Team Agent](plugins/whatsapp/whatsappuser/teamagent.md).

??? question "WhatsApp için gelişmiş routing kuralları nasıl ayarlarım?"
 Gelişmiş routing otomatik olarak gelen WhatsApp mesajlarını doğru ajana veya chatbot'a yönlendirir:

    1. Go to Go to Go to Go **WhatsApp > Gelişmiş Routing Kuralları**
    2. Click Click Click Click Click **"Add New Rule"**
    3. Bu parametrelerle kuralı yapılandırın:

    | Parametre parametresi | Açıklama |
    |-----------|-------------|
    | **Kural Adı** | Clear, tanımlayıcı adı kolay kimlik için |
    | **Kapsam -©** | Belirli webchat konektörünü seçin |
    | **Kapsam - Time Frame** | Kural aktif olduğunda set |
    | **Mantık - Payload Type** | İçerik türü ile yol (text, image, vs.) |
    | **Mantık - Payload Text** | Belirli anahtar kelimeler veya cümlelerle yollayın |
    | **Mantık - Payload Caption** | Yol Tarafından Image/video caption |
    | **Mantık - Sender Info** | Rota by sender details (isim, telefon) |
    | **Mantıksal Operatörler** | AND/OR mantığı ile birlikte koşulları birleştirin |
    | **Fulfillmentment** | Belirli bir yol için **Agent Agent** veya **Bot Bot Bot** |

 [Gelişmiş Routing](plugins/whatsapp/whatsappuser/advancerouting.md) Ve [Rule Konsülasyonu](plugins/whatsapp/whatsappuser/ruleconfiguration.md).

??? question "Otomatik sohbetbot akışları nasıl yaratıyorum?"
    1. Go to Go to Go to Go **WhatsApp > Flow Flow Flow Flow**
    2. seçin: **Pre- built Template** (quick kurulumu) veya **Surdan Yapın** (eğer özel)
    3. Yeniden yapılandırın **Bot** - sohbetbotunu etkinleştiren belirli bir metin /phrase
    4. Set the Set the Set the Set **Retry Mechanism** Başarısız tetikleyici girişimler için
    5. Configure **Idle Timeout** Otomatik takip için, kullanıcı cevap verirken yanıt verir

 **Mevcut akış bina blokları:**

    | Block Block Block | Açıklama |
    |-------|-------------|
    | **Mesaj Gönder** | Kullanıcıya bir metin mesajı gönder |
    | **Top Girişi Toplayın** | Hızlı bir şekilde görüntüleyin ve kullanıcının yanıtını değişken bir şekilde ele alın |
    | **Seçenek seçeneği** | Seçmeli görüntü ile 3 seçenek (Meta limit) ile mevcut; akış seçime dayanıyor |
    | **Şube** | Daha önce toplanan girdilere dayanan koşullu yollar oluşturun |
    | **Gönder** | Belgeleri, fotoğrafları veya videoları gönderin |

 Bu blokları SSS'leri ele alan otomatik konuşmaları oluşturmak için bir araya getirin, bilgi toplamak, doğru yol açar ve gerektiğinde insan ajanlarına yollayın. [Manage Flow](plugins/whatsapp/whatsappuser/manageflow.md).

??? question "WhatsApp iletişim loglarını nasıl izliyorum?"
 Go to Go to Go to Go **WhatsApp > İzleme** ayrıntılı işlem kayıtlarını görüntülemek için:

    - Uygulamanız ve Meta (WhatsApp) arasındaki her etkileşim giriş
    - Her ikisi de **Talepler** ve **Yanıtlar** kaydedilir.
    - Teslimat sorunlarını sorunmak ve teknik sorunları teşhis etmek için kullanışlı

    !!! warning
 İzleme logları için tutulur **Son 3 gün** Sadece. Bir sorunu araştırmak için hemen girişleri kontrol edin.

 Görün (a.s.)(plugins/whatsapp/whatsappuser/monitoring.md).

??? question "WhatsApp kampanya raporlarını nasıl görüyorum?"
 Go to Go to Go to Go **WhatsApp > Raporlar** Birden fazla rapor türü için:

 **Kampanya Raporu:**

    - **Kampanya View View** Kampanya adı, gönderici, içerik, toplam mesajlar, statü ve maliyet göstermek için
    - **Liste View** - Alıcı numarası, şablonlar, teslim tarihi, teslimat tarihi, durumu ve hata kodları dahil olmak üzere mesaj düzeyinde ayrıntılar

 **Mesaj Count Report:**

    - Seçilen bir tarih aralığında gönderilen toplam mesajların hızlı bir bakış

 **My Schedule:**

    - Tüm planlanan WhatsApp kampanyalarını statü ve mesaj numaralarıyla görüntüle

 **Download Report:**

    - Export detailed WhatsApp kampanyası çevrimdışı analiz için raporlar
    - SMS raporlarından ayrı olarak daha iyi organizasyon için

 [Campaign Report](plugins/whatsapp/whatsappuser/reports/campaignreport.md).

---

## Geliştirici API API

??? question "API belgelerine nasıl erişebilirim?"
    1. Go to Go to Go to Go **Geliştirici API > API Document**
    2. Click Click Click Click Click **API Doküman Dokümanı Görüntüle**
    3. Sistem yönlendirilir **Swagger** interaktif API aracı
    4. Son noktaları göz önünde bulundurun, görüş talebi/response formatları ve API çağrılarını doğrudan test edin

 Belgeler, ödeme hatları, cevap yapıları, kimlik doğrulama detayları, hata işleme ve en iyi uygulamaları içerir. [API Dokümanı](user/apidocument/document.md).

??? question "API kimliklerini nasıl üretirim ve nasıl başladım?"
 API erişimi yöneticiniz tarafından belirlenir:

    1. Yöneticiniz size olanak sağlar **HTTP API erişimi** Hesabınız için
    2. Bir tane alıyorsunuz **Username** ve **API Anahtar** Onaylama için
    3. Go to Go to Go to Go **Geliştirici API > Geliştirici API** Bilgilerinizi görüntülemek için
    4. Click Click Click Click Click **API Doküman Dokümanı Görüntüle** Swagger aracı test etmek için

 API isteklerinizin yetki başlığında bu bilgileri kullanın. Swagger aracı, uygulamanıza entegre etmeden önce tüm API uç noktalarını interaktif olarak test etmenizi sağlar. [De Developmenter API](user/apidocument/developerapi.md).

??? question "API uç noktaları nelerdir?"
 Power SMPP, için kapsamlı REST API sağlar:

    - **SMS gönder** Tek ve toplu mesaj gönderme
    - **Teslimat durumunu kontrol edin** - gönderilen mesajlar için DLR statüsü
    - **Yönetim İletişim Yönetimi** – Create, update, and delete contact /groups
    - **Retrieving Reports** - Pull kampanyası ve mesaj raporları programmatik olarak

 Tüm uç noktaları standart kabul eder **HTTP yöntemleri** (GET, POST) ve geri dönüş **JSON yanıtlar**. Tüm son nokta listesi parametreler, örnekler ve yanıt kodları [API Dokümanı] mevcuttur.(user/apidocument/document.md).

??? question "Power SMPP'yi kendi uygulamamla entegre edebilir miyim?"
 Evet. Power SMPP, üçüncü taraf entegrasyonunu destekler:

    - **REST API** - Programmatik erişim için tam özellikli HTTP API
    - **Webhooks** - DLR ve MO bildirimleri için gerçek zamanlı çağrılar
    - **SMPP Protokolü** - Direct SMPP v3.4 yüksek hacimli entegrasyonlar için bağlantı (admin tarafından yapılandırılır)

 Swagger belgeleri, sorunsuz entegrasyon için istek / soru örnekleri ve en iyi uygulamalar sağlar. SMPP bağlantı detayları için yöneticinize ulaşın.

---

## Hesap ve Billing

??? question "Hız planımı nasıl görüyorum?"
 Go to Go to Go to Go **Uygulama Bar > Benim Puan Planım** Mevcut fiyatlarınızı görmek için:

    - Fiyatlar başına gösteriliyor **Ülke ülkesi ülkesi** ve **ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ ağ**
    - Oranlar ebeveyn hesabınız/administratorunuz tarafından belirlenir
    - Bunlar belirlemeyi belirler **mesaj başına maliyet** Her hedef için
    - Kampanya maliyetlerini önceden göndermeden önce tahmin etmek için bunu kullanın

 Kampanya kompozisyonunda gösterilen maliyet önizlemesi bu oranları kullanır. [My Rate Plan](user/applicationbar/rateplan.md).

??? question "Pre ücretli ve Post ücretli faturalama arasındaki fark nedir?"
    | Özellik | Pre ücretli | Posta ücretsiz |
    |---------|---------|----------|
    | **Denge dengesi** | göndermeden önce yeterli krediye sahip olmalı | Satın alındıktan sonra Billed |
    | **Kredi Check Check** | Sistem işlemeden önce dengeyi kontrol eder | Ön kontrol gerekli değil |
    | **Overspending** | Mümkün değil – kampanya krediler tükendiğinde durur | Mümkün - invoicing için takip edildi |
    | **Vaka Kullanımı** | Son kullanıcılar için en yaygın | Tipik olarak güvenilir / katılımcı hesapları |

 Fatura modunuz yöneticiniz tarafından yapılandırılır. Check Check Check Check **Uygulama Bar > İşlemlerim** Mevcut bakiyenizi ve işlem tarihini görmek.

??? question "İşlem tarihimi nasıl kontrol edebilirim?"
 Go to Go to Go to Go **Uygulama Bar > İşlemlerim** Görmek için:

    - Hesabınız ve ebeveyn hesabınız arasındaki tam işlem tarihi
    - Kredi ekleri (top-up)
    - Kredi kesintiler (campaign maliyetler)
    - şeffaflık için tam denetim yolu

 Bu, harcamayı takip etmenize yardımcı olur, üst ücretlileri doğrulayın ve mesajlaşma bütçenizi yönetmenize yardımcı olur. Görüm [My Transactions](user/applicationbar/transaction.md).

??? question "Gerçek zamanlı bildirimleri için webhooks nasıl ayarlarım?"
 Webhooks uygulamanıza gerçek zamanlı DLR ve MO bildirimleri zorlar:

    1. Go to Go to Go to Go **Uygulama Bar > WebHooks**
    2. Click Click Click Click Click **"Add New Webhook"**
    3. Webhook'u yapılandırın:

    | Field | Açıklama |
    |-------|-------------|
    | **Dostu Ad** | Webhook için tanımlayıcı bir isim |
    | **Endpoint Base URL** | Sunucunuzun çağrı URL |
    | **Yöntem Yöntemi** | GET veya POST |
    | **Handler** | MO (incoming messages) veya DLR (delivery replicas) |

 **Teknik gereksinimler:**

    - Son noktanız geri dönmeli **HTTP 200 Tamam** Zaman içinde
    - Varsayılan zaman süresidir **10 saniye**
    - Eğer sunucunuz zamanında yanıt vermezse, bildirim tekrarlanabilir veya düşmüş olabilir veya düştü

 [WebHooks](user/applicationbar/webhook.md).

??? question "Bildirim e-postalarını nasıl yapılandırabilirim?"
 Go to Go to Go to Go **Uygulama Bar > Bildirim Emails** e-posta uyarıları kurmak için:

    - Varsayılan olarak, bildirimler sizin için gönderilir **kayıtlı e-posta** adresi
    - Ekleyebilirsiniz **Ek pay sahibi e-posta adresleri** Uyarılar almak için
    - hangisinin **olaylar olayları** E-posta bildirimleri

 E-posta bildirimleri hesap iletişimi, kampanya uyarıları, OTP teslimat ve sistem bildirimleri için kullanılır. Görün [E-postayı değiştir](user/applicationbar/notificationemail.md).

---

## Sorun Giderme

??? question "Neden uzun zamandır ‘Pending’ olarak gösteren mesajlarım?"
 Birkaç neden uzun süre bekleme süresine neden olabilir:

    - **Operatör gecikme gecikme gecikmeleri** - Bazı mobil operatörler teslimat onaylarını geri almak için daha uzun sürer
    - **Recipient telefonunu kapat** - Mesaj operatörde telefonla ulaşılıncaya kadar sıralanır
    - **Network congestion** - Yüksek trafik dönemleri DLR işlemlerini geciktirebilir
    - **Gateway sorunları** – Yükselen ağ geçidi gecikmeleri yaşayabilir

 **Ne yapmalı:** Makul bir süre bekleyin ( ülke/operatör) Eğer mesajlar 2448 saat sonra bekliyorsa, teslim edilmeleri mümkün değildir. Sorun devam ederse yöneticinizle kontrol edin.

??? question "Mesajım neden reddedildi ya da başarısız oldu?"
 Mesaj başarısızlığı için ortak nedenler:

    | Sebep Sebep Sebep Sebep | Çözüm Çözüm çözümü |
    |--------|----------|
    | Invalid telefon numarası | Sayı formatı doğru ülke kodu içeriyor |
    | DND/Do Not Disturb | Recipient ticari mesajlardan ayrıldı |
    | Şablon yanlış | Onaylanan şablonları tam olarak karşılayın |
    | Sender ID onaylanmadı | Onaylanmış bir Sender ID kullanın veya onay onayı |
    | Yetersiz kredilerde | Top up your account bakiye (pre ücretli) |
    | Blacklisted numara | yöneticinizle kontrol edin |
    | Content blocked engelledi | Sınırlı anahtar kelimeler için mesaj içeriği |

??? question "Kampanyam neden beklediğimden farklı?"
 Kampanya maliyetleri bağlıdır:

    - **Alıcı sayısı** - Her benzersiz sayı şarj edilir
    - **Mesaj segmentleri** Uzun mesajlar birden çok segmente bölünür, her fatura ayrı ayrı ayrı ayrı ayrı
    - **Unicode vs GSM** - Unicode mesajlarının daha düşük karakter sınırları vardır, daha fazla segmentle sonuçlanan
    - **Hedef oranları** - Farklı ülkeler / ağlar per-messaj maliyetleri farklı
    - **DLR tazminat tazminat** - Bazı konfigürasyonlar teslimat durumuna göre maliyetleri ayarlanabilir

 Her zaman kontrol et **Maliyet önizleme** Bir kampanya onaylamadan önce ve [Rate Planını] gözden geçirmeden önce(user/applicationbar/rateplan.md) Hedefe özgü fiyatlar için.

??? question "Şifremi unuttum. Nasıl sıfırlıyorum?"
 Şifre sıfırlamaları sizin tarafınızdan yönetilir **Sistem yöneticisi**. Onları doğrudan bir reset talep etmek için iletişime geçin. Bir kez sıfırlandığında, geçici şifre ile giriş yapın ve hemen onu değiştirir **Ayarlar > Change Password**.

 Yöneticiniz ayrıca kendi servis parola sıfırlama seçeneğine sahip olabilir - belirli işlem için onlarla kontrol edin.
