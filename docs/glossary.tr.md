---
tags:
  - Reference
  - SMPP
  - Getting Started
---

# Parlak

Power SMPP dokümanları boyunca kullanılan ortak terimlere hızlı bir referans kılavuzu.

---

## Messaging Şartları

| Term Term Term Term | Full Form | Açıklama |
|------|-----------|-------------|
| **SMS SMS SMS SMS** | Kısa Mesaj Servisi | Standart metin mesajlaşma protokolü mobil cihazlar için |
| **MT MT MT** | Mobile Terminated | gönderilen bir mesaj **toklanmak için** Bir mobil el (outbound) |
| **MO MO MO** | Mobile Originated | gönderilen bir mesaj **From from from from from from from from from from from from from from from from from from from from from from from from from from from from from from from from from from** Bir mobil el (inbound) |
| **DLR** | Teslimat Raporu | Bir MT mesajının teslim olup olmadığını doğrulama durumu bildirimi |
| **A2P** | Uygulama-to-Person | Kullanıcıyı sonlandırmak için bir uygulamadan gönderilen otomatik mesajlar |
| **P2P** | Kişi-to-Person | Bireysel kullanıcılar arasında paylaşılan mesajlar |

---

## SMPP Protokolü

| Term Term Term Term | Full Form | Açıklama |
|------|-----------|-------------|
| **SMPP** | Kısa Mesaj Peer-to-Peer | Sistem arasında değişen SMS için endüstri standart protokolü |
| **SMSC** | Kısa Mesaj Servisi Merkezi | Dükkanlar, rotalar ve SMS mesajları sunan merkezi sistem |
| **ESME** | Dış Kısa Messaging Entity | SMPP aracılığıyla SMSC'ye bağlanan dış bir uygulama |
| **PDU** | Protokol Data Unit | ESME ve SMSC arasında yapılan tek bir SMPP veri paketi |
| **Bin** | – | ESME ve SMSC arasında bir SMPP oturumu kurma süreci |
| **Tx** | 3. | Sadece bir SMPP seansı **Gönder** Mesaj mesajları |
| **Rx** | Alıcı | Sadece bir SMPP seansı **Kabul alın** Mesaj mesajları |
| **TRx** | Transceiver | Hem de bir SMPP seansı **Gönder ve alın** Mesaj mesajları |
| **TPS** | İkinci İşlemler | SMPP bağlantı kapasitesi |

---

## Adrese

| Term Term Term Term | Full Form | Açıklama |
|------|-----------|-------------|
| **TON** | Sayı Türü | Adresin biçimini tanımlar (e.g., International, Alfanumeric) |
| **NPI** | Sayılama Plan Göstergesi | Sayı standardını belirtir (örneğin, E.164, ISDN) |
| **Ey** | Originating Address | Bir mesaj (kaynak) |
| **DA DA DA** | Hedef Adres | Bir mesajın alıcı adresi (destination) |
| **MCC** | Mobile Country Code | Bir mobil abone ülkenin ülkesini tanımlayan 3 dijital kod |
| **MNC** | Mobile Network Code Code | Bir mobil ağ operatörü tanımlayan 2-3 sayısal kod |
| **MSISDNDN** | Mobile Station International Subscriber Directory Number | Bir mobil abonenin tam uluslararası telefon numarası |

---

## Platform Özellikler

| Term Term Term Term | Açıklama |
|------|-------------|
| **Hız Planı** | Per-message maliyetlerini farklı destinasyonlar için tanımlayan bir fiyat şablonu |
| **Routing Rule** | Hangi ağ geçidinin hedef, gönderici veya içerikli kriterlere dayanarak bir mesaj işlediğini belirleyen bir kural |
| **Gateway Gateway** | ITextPRO |
| **Interface** | Ortakların iTextPRO'e bağlanmasını sağlayan bir SMPP veya HTTP konektörü |
| **Blind Routing** | Önceden tanımlanmış maliyet fiyatları olmadan destinasyonlara mesaj gönderme izinler |
| **Kayıplık Dur** | Kör-routed mesajlardaki kayıpları önlemek için maksimum ağ geçidi maliyeti eşi |
| **HLR Lookup** | Home Location Register query, göndermeden önce bir mobil sayıyı doğrulamak için |
| **DLT** | Dağıtılmış Ledger Teknolojisi - Hindistan'ın A2P SMS'i önceden gönderilenler ve şablonlar gerektiren düzenleyici çerçeve |

---

## Billing & Business

| Term Term Term Term | Açıklama |
|------|-------------|
| **Pre ücretli** | Kullanıcıların göndermeden önce yeterli kredi dengesine sahip olması gerektiğini Billing modu |
| **Posta ücretsiz** | Kullanıcıların tüketim sonrası faturalandırıldığı Billing modu |
| **Base Para** | Tüm iç fatura hesaplamaları için kullanılan birincil para |
| **Faturayı Yeniden Al** | Düzenli aralıklarla üretilen otomatik fatura (haftada, aylık vb.) |

---

## Sistem ve İzleme

| Term Term Term Term | Açıklama |
|------|-------------|
| **Event Viewer** | Sistem olayları, hataları ve uyarıları izlemek için bir log viewer |
| **Denetim Log** | Tüm kullanıcı ve sistem eylemlerinin bir kronolojik kaydı uyumluluk için |
| **PDU Logger** | Çiğ SMPP protokolü veri paketlerini yakalamak ve incelemek için bir araç |
| **Enquire Link** | Aktif seansları korumak için düzenli olarak gönderilen SMPP keep-alive paketi |
| **QoS** | Hizmet kalitesi - ağ geçidi teslimat performansını değerlendirmek için kullanılan ölçümler |
