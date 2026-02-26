# YiSA-S Sistem Durum Raporu

> **Son Guncelleme:** 2026-02-26 23:00 UTC
> **Hazirlayan:** Devin AI Engineer
> **Talep Eden:** Serdinc Altay (@serdincaltay-ai)

---

## a) Su Ana Kadar Yapilanlar

### Tamamlanan Gorevler

| # | Gorev | Repo | PR | Durum |
|---|-------|------|----|-------|
| 1 | Fenerbahce Spor Okullari landing page | v0-3-d-landing-page | [PR #1](https://github.com/serdincaltay-ai/v0-3-d-landing-page/pull/1) | CI Gecti, Merge Bekliyor |
| 2 | "Franchise bulunamadi" bug fix (middleware) | tenant-yisa-s | [PR #38](https://github.com/serdincaltay-ai/tenant-yisa-s/pull/38) | CI Gecti, Merge Bekliyor |
| 3 | bjktuzlacimnastik tenant landing page | tenant-yisa-s | [PR #38](https://github.com/serdincaltay-ai/tenant-yisa-s/pull/38) | CI Gecti, Merge Bekliyor |
| 4 | Instagram/WhatsApp/Google Business API route'lari | tenant-yisa-s | [PR #38](https://github.com/serdincaltay-ai/tenant-yisa-s/pull/38) | CI Gecti, Merge Bekliyor |
| 5 | ManyChat webhook GET endpoint | tenant-yisa-s | [PR #38](https://github.com/serdincaltay-ai/tenant-yisa-s/pull/38) | CI Gecti, Merge Bekliyor |
| 6 | RBAC sistemi (patron, franchise_sahibi, antrenor, veli) | app-yisa-s | [PR #11](https://github.com/serdincaltay-ai/app-yisa-s/pull/11) | CI Gecti, Merge Bekliyor |
| 7 | Patron auth: cookie -> DB role alani | app-yisa-s | [PR #11](https://github.com/serdincaltay-ai/app-yisa-s/pull/11) | CI Gecti, Merge Bekliyor |
| 8 | Demo hesaplar silme migration'i | app-yisa-s | [PR #11](https://github.com/serdincaltay-ai/app-yisa-s/pull/11) | CI Gecti, Merge Bekliyor |
| 9 | 3 pre-existing TypeScript build error duzeltmesi | tenant-yisa-s | [PR #38](https://github.com/serdincaltay-ai/tenant-yisa-s/pull/38) | CI Gecti, Merge Bekliyor |
| 10 | 10 sayfalik YISA-S sunum (HTML) | - | Dosya teslim edildi | Tamamlandi |
| 11 | SQL migration: demo hesap silme + patron role | Supabase DB | Manuel calistirildi | Tamamlandi |
| 12 | user_tenants role constraint guncelleme | Supabase DB | Manuel calistirildi | Tamamlandi |
| 13 | demo_requests source constraint (manychat eklendi) | Supabase DB | Manuel calistirildi | Tamamlandi |

### Supabase'de Manuel Calistirilan Migration'lar (Onaylandi)

- [x] Demo hesaplar silindi (coach@demo.com, kayit@demo.com, mudur@demo.com, owner@demo.com)
- [x] serdincaltay@gmail.com -> patron rolu atandi (user_tenants tablosu)
- [x] user_tenants.role CHECK constraint eklendi (patron, franchise_sahibi, antrenor, veli, admin, kasa)
- [x] demo_requests.source constraint'e 'manychat' eklendi

### Merge Edilen PR'lar

| PR | Repo | Durum |
|----|------|-------|
| [PR #37](https://github.com/serdincaltay-ai/tenant-yisa-s/pull/37) | tenant-yisa-s | Merged (cart-curt-full-sprint) |

### Calisan Sayfalar / Preview URL'ler

| Sayfa | URL | Durum |
|-------|-----|-------|
| tenant-yisa-s Preview | [Preview](https://tenant-yisa-s-git-devin-1772-07d9bb-serdincaltay-5864s-projects.vercel.app) | Calisiyor (PR branch) |
| app-yisa-s Preview | [Preview](https://app-yisa-s-git-devin-1772096-fe35eb-serdincaltay-5864s-projects.vercel.app) | Calisiyor (PR branch) |
| v0-3-d-landing-page Preview | [Preview](https://v0-3-d-landing-page-git-devin-1771-serdincaltay-5864s-projects.vercel.app) | Calisiyor (PR branch) |
| bjktuzlacimnastik.yisa-s.com | https://bjktuzlacimnastik.yisa-s.com | PR merge sonrasi aktif olacak |

---

## b) Neredeyiz?

### Genel Ilerleme

```
Toplam Ilerleme: ████████████████░░░░ %78
```

| Alan | Ilerleme | Aciklama |
|------|----------|----------|
| Altyapi & DB | ████████████████████ %95 | Tablolar, migration'lar, RLS tamam |
| RBAC Sistemi | ████████████████░░░░ %80 | Scaffold tamam, API route enforcement eksik |
| Tenant Landing Page | ████████████████░░░░ %75 | Hardcoded icerик, dinamik hale getirilmeli |
| Sosyal Medya API | ██████████████░░░░░░ %70 | Route'lar var, auth eksik, test edilmedi |
| ManyChat Webhook | ██████████████░░░░░░ %70 | GET endpoint var, auth eksik |
| Patron Paneli | ████████████████░░░░ %80 | RBAC tamam, roller tanimli |
| Fenerbahce Landing | ████████████████████ %95 | Tamamlandi, merge bekliyor |
| Supabase Trigger Fix | ░░░░░░░░░░░░░░░░░░░░ %0 | 6 tabloda bozuk trigger |

### Calisan / Calismayan Sayfa Tablosu

| Sayfa/Endpoint | Durum | Not |
|----------------|-------|-----|
| app-yisa-s /login | Calisiyor | Vercel deploy aktif |
| app-yisa-s /patron/* | Calisiyor | RBAC PR merge sonrasi DB-based auth |
| tenant-yisa-s /tenant-site | PR'da | Merge sonrasi aktif |
| tenant-yisa-s /api/social/* | PR'da | Merge sonrasi aktif |
| tenant-yisa-s /api/webhooks/manychat | PR'da | Merge sonrasi aktif |
| bjktuzlacimnastik.yisa-s.com | 404 | PR merge + DNS gerekli |
| v0-3-d-landing-page | PR'da | Merge sonrasi aktif |

---

## c) Kalan Isler

### Oncelik 1 - Kritik (Hemen Yapilmali)

| # | Is | Tahmini Sure | Bagimllik |
|---|---|-------------|-----------|
| 1 | PR #38 (tenant-yisa-s) merge | 1 dk | - |
| 2 | PR #11 (app-yisa-s) merge | 1 dk | - |
| 3 | PR #1 (v0-3-d-landing-page) merge | 1 dk | - |
| 4 | Supabase trigger duzeltme (6 tablo) | 15 dk | - |
| 5 | bjktuzlacimnastik tenant_id baglantisi (franchise_subdomains) | 5 dk | #1 |
| 6 | social_media_configs tablosu olustur (Supabase'de yok) | 5 dk | - |

### Oncelik 2 - Onemli (Bu Hafta)

| # | Is | Tahmini Sure | Bagimllik |
|---|---|-------------|-----------|
| 7 | Sosyal medya API route'larina auth eklenmesi | 2 saat | #2 merge |
| 8 | ManyChat webhook auth eklenmesi | 1 saat | #2 merge |
| 9 | Tenant landing page'i dinamik hale getirme (slug bazli) | 3 saat | #1 merge |
| 10 | RBAC'i tum API route'lara uygulama (requireRole) | 4 saat | #2 merge |
| 11 | Davet sistemi (yeni kullanici ekleme) | 4 saat | #2 merge |
| 12 | social_media_configs RLS policy guclendir | 1 saat | #6 |

### Oncelik 3 - Iyilestirme (Gelecek Sprint)

| # | Is | Tahmini Sure | Bagimllik |
|---|---|-------------|-----------|
| 13 | Fenerbahce landing page: Gercek logo entegrasyonu | 1 saat | #3 merge |
| 14 | Demo form fonksiyonelligi (form submit handler) | 2 saat | #1 merge |
| 15 | createClient -> createServerClient (SSR uyumluluk) | 1 saat | #2 merge |
| 16 | BrainTeamChat stale closure bug fix | 30 dk | #1 merge |
| 17 | E2E test suite olusturma | 8 saat | Tum merge'ler |

### Bozuk Trigger'lar - Acil Duzeltme Gerekli

`update_guncelleme_tarihi()` fonksiyonu `NEW.guncelleme_tarihi = NOW()` yapiyor ama 6 tabloda `guncelleme_tarihi` kolonu YOK:

| Tablo | Trigger Adi | Durum |
|-------|-------------|-------|
| athletes | trg_update_athletes | BOZUK - kolon yok |
| attendance | trg_update_attendance | BOZUK - kolon yok |
| demo_requests | trg_update_demo_requests | BOZUK - kolon yok |
| messages | trg_update_messages | BOZUK - kolon yok |
| payments | trg_update_payments | BOZUK - kolon yok |
| staff | trg_update_staff | BOZUK - kolon yok |

**Duzeltme:** Ya bu tablolara `guncelleme_tarihi` kolonu ekle, ya da trigger'lari kaldir.

---

## d) Mevcut Mimari

### Sistem Diyagrami

```mermaid
graph TB
    subgraph "Kullanici Katmani"
        V[Veli] -->|Login| TS
        A[Antrenor] -->|Login| TS
        FS[Franchise Sahibi] -->|Login| TS
        P[Patron - Serdinc Altay] -->|Login| AS
    end

    subgraph "Frontend - Vercel"
        TS[tenant-yisa-s<br/>Next.js 15]
        AS[app-yisa-s<br/>Next.js 15]
        LP[v0-3-d-landing-page<br/>Next.js]
    end

    subgraph "Backend - API Routes"
        TS --> API1[/api/social/*]
        TS --> API2[/api/webhooks/manychat]
        TS --> API3[/api/franchise/*]
        TS --> API4[/api/demo-requests]
        AS --> API5[/api/patron/*]
        AS --> API6[/api/tenants/*]
    end

    subgraph "Middleware Katmani"
        MW1[tenant-yisa-s middleware<br/>Subdomain -> Tenant routing]
        MW2[app-yisa-s middleware<br/>RBAC + Auth]
    end

    subgraph "Supabase - PostgreSQL"
        DB[(bgtuqdkfppcjmtrdsldl)]
        DB --> T1[tenants]
        DB --> T2[user_tenants]
        DB --> T3[franchise_subdomains]
        DB --> T4[demo_requests]
        DB --> T5[franchises]
        DB --> T6[auth.users]
    end

    subgraph "Dis Servisler"
        MC[ManyChat] -->|Webhook| API2
        IG[Instagram API] --> API1
        WA[WhatsApp Business] --> API1
        GB[Google Business] --> API1
    end

    API1 --> DB
    API2 --> DB
    API3 --> DB
    API5 --> DB
    MW1 --> TS
    MW2 --> AS
```

### Repo Yapisi

```
serdincaltay-ai/
|
|-- app-yisa-s/                    # Patron paneli (ana yonetim uygulamasi)
|   |-- Branch: devin/1772096872-roles-social-webhook (PR #11 - OPEN)
|   |-- lib/middleware/role-auth.ts  # RBAC sistemi
|   |-- lib/celf/patron-auth.ts     # Patron auth (DB-based)
|   |-- middleware.ts               # Next.js middleware
|   |-- lib/types/index.ts          # UserRole tipi
|   |-- supabase/migrations/        # 12 migration dosyasi
|   +-- Vercel: app-yisa-s.vercel.app
|
|-- tenant-yisa-s/                 # Franchise tenant uygulamasi
|   |-- Branch: devin/1772096872-bugfix-tenant-page (PR #38 - OPEN)
|   |-- app/tenant-site/page.tsx    # Tenant landing page
|   |-- app/api/social/             # Instagram, WhatsApp, Google Business
|   |-- app/api/webhooks/manychat/  # ManyChat webhook
|   |-- lib/supabase/middleware.ts   # Subdomain routing
|   |-- supabase/migrations/        # 20+ migration dosyasi
|   +-- Vercel: tenant-yisa-s.vercel.app
|
|-- v0-3-d-landing-page/           # Fenerbahce pazarlama sayfasi
|   |-- Branch: devin/1771751715-fenerbahce-landing-page (PR #1 - OPEN)
|   |-- app/page.tsx                # Ana pazarlama sayfasi
|   +-- Vercel: v0-3-d-landing-page.vercel.app
|
|-- yisa-s/                        # Ana repo (issue tracker, docs)
|   +-- Branch: main
|
|-- v0-web-page-content-edit-bjktesis/  # BJK Tesis landing (eski)
|   +-- Branch: main
|
+-- yisa-s-app-uh/                 # 3D landing + CELF API (eski)
    +-- Branch: main
```

### Supabase Tablo Durumu

**Proje:** YiSA-S (`bgtuqdkfppcjmtrdsldl`) - Bolge: eu-central-1

| Kategori | Tablolar | Sayi |
|----------|----------|------|
| Tenant / Franchise | tenants, franchise_subdomains, franchises, franchise_agreements, franchise_applications, franchise_territories, franchise_revenue, franchise_customers, franchise_websites, franchise_basvurulari | 10 |
| Kullanici / Auth | users, user_tenants, user_profiles, kullanicilar, roller, roles, role_permissions | 7 |
| Sporcu / Olcum | athletes, assessments, athlete_health_records, athlete_measurements, evaluations, phv_measurements, baseline_tests, olcum_kayitlari | 8 |
| Yoklama / Ders | attendance, student_attendance, schedules, ders_programi, ders_rezervasyonlari, yoklama | 6 |
| Odeme / Paket | payments, packages, package_payments, package_pricing, seans_packages, student_packages, subscriptions, cash_register | 8 |
| AI / Robot | robots, robot_tasks, robot_health, robot_activity, robot_ai_profiles, robot_chat_logs, robot_recommendations, robot_system_prompts, robot_task_queue, robot_api_permissions | 10 |
| CELF Motor | celf_artifacts, celf_audit_logs, celf_cost_reports, celf_deployments, celf_directorates, celf_epics, celf_events, celf_kasa, celf_logs, celf_provider_registry, celf_tasks | 11 |
| CRM / Iletisim | crm_contacts, crm_activities, crm_lead_stages, conversations, messages, chat_messages, ai_messages, demo_requests | 8 |
| Patron / Yonetim | patron_commands, patron_inbox, patron_private_tasks, patron_sales_prices, approval_queue, approval_rules | 6 |
| Diger | 50+ tablo (staff, expenses, templates, security_*, audit_*, task_*, workflow_*, vb.) | 50+ |
| **TOPLAM** | | **~160 tablo** |

### Auth Kullanicilari

| Email | Rol (user_tenants) | Tenant |
|-------|-------------------|--------|
| serdincaltay@gmail.com | patron | bjk-tuzla (8cc3ea1d) |
| ~~coach@demo.com~~ | - | SILINDI |
| ~~kayit@demo.com~~ | - | SILINDI |
| ~~mudur@demo.com~~ | - | SILINDI |
| ~~owner@demo.com~~ | - | SILINDI |

### Vercel Deployment Durumu

| Proje | Production | PR Preview | Durum |
|-------|-----------|------------|-------|
| tenant-yisa-s | tenant-yisa-s.vercel.app | PR #38 preview aktif | Calisiyor |
| app-yisa-s | app-yisa-s.vercel.app | PR #11 preview aktif | Calisiyor |
| v0-3-d-landing-page | - | PR #1 preview aktif | Calisiyor |

---

## e) Benim Yapmam Gerekenler (Manuel Mudahale)

### Kritik - Hemen Yapilmali

| # | Eylem | Komut / Aciklama | Nerede |
|---|-------|-------------------|--------|
| 1 | **PR #38 Merge** | GitHub'da [PR #38](https://github.com/serdincaltay-ai/tenant-yisa-s/pull/38) ac -> "Merge pull request" tikla | GitHub |
| 2 | **PR #11 Merge** | GitHub'da [PR #11](https://github.com/serdincaltay-ai/app-yisa-s/pull/11) ac -> "Merge pull request" tikla | GitHub |
| 3 | **PR #1 Merge** | GitHub'da [PR #1](https://github.com/serdincaltay-ai/v0-3-d-landing-page/pull/1) ac -> "Merge pull request" tikla | GitHub |
| 4 | **bjktuzlacimnastik tenant_id bagla** | Supabase SQL Editor'da asagidaki SQL'i calistir: | Supabase Dashboard |

```sql
-- bjktuzlacimnastik subdomain'ini tenant'a bagla
UPDATE public.franchise_subdomains
SET tenant_id = '8cc3ea1d-27a0-496e-a0fb-1625be7a9b35'
WHERE subdomain = 'bjktuzlacimnastik';
```

| 5 | **social_media_configs tablosu olustur** | Supabase SQL Editor'da asagidaki SQL'i calistir: | Supabase Dashboard |

```sql
CREATE TABLE IF NOT EXISTS public.social_media_configs (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  tenant_id UUID REFERENCES public.tenants(id),
  platform TEXT NOT NULL CHECK (platform IN ('instagram', 'whatsapp', 'google_business')),
  account_id TEXT,
  access_token TEXT,
  config JSONB DEFAULT '{}',
  active BOOLEAN DEFAULT true,
  created_at TIMESTAMPTZ DEFAULT now(),
  updated_at TIMESTAMPTZ DEFAULT now(),
  UNIQUE(tenant_id, platform)
);

ALTER TABLE public.social_media_configs ENABLE ROW LEVEL SECURITY;

CREATE POLICY "Tenant social media configs"
  ON public.social_media_configs
  USING (tenant_id IN (
    SELECT tenant_id FROM public.user_tenants
    WHERE user_id = auth.uid()
  ))
  WITH CHECK (tenant_id IN (
    SELECT tenant_id FROM public.user_tenants
    WHERE user_id = auth.uid()
  ));
```

| 6 | **Bozuk trigger'lari duzelt** | Supabase SQL Editor'da asagidaki SQL'i calistir: | Supabase Dashboard |

```sql
-- Secenеk A: Bozuk trigger'lari kaldir (onerilir)
DROP TRIGGER IF EXISTS trg_update_athletes ON public.athletes;
DROP TRIGGER IF EXISTS trg_update_attendance ON public.attendance;
DROP TRIGGER IF EXISTS trg_update_demo_requests ON public.demo_requests;
DROP TRIGGER IF EXISTS trg_update_messages ON public.messages;
DROP TRIGGER IF EXISTS trg_update_payments ON public.payments;
DROP TRIGGER IF EXISTS trg_update_staff ON public.staff;

-- VEYA Secenek B: Eksik kolonu ekle (eger guncelleme_tarihi istiyorsan)
-- ALTER TABLE public.athletes ADD COLUMN IF NOT EXISTS guncelleme_tarihi TIMESTAMPTZ DEFAULT now();
-- ALTER TABLE public.attendance ADD COLUMN IF NOT EXISTS guncelleme_tarihi TIMESTAMPTZ DEFAULT now();
-- ALTER TABLE public.demo_requests ADD COLUMN IF NOT EXISTS guncelleme_tarihi TIMESTAMPTZ DEFAULT now();
-- ALTER TABLE public.messages ADD COLUMN IF NOT EXISTS guncelleme_tarihi TIMESTAMPTZ DEFAULT now();
-- ALTER TABLE public.payments ADD COLUMN IF NOT EXISTS guncelleme_tarihi TIMESTAMPTZ DEFAULT now();
-- ALTER TABLE public.staff ADD COLUMN IF NOT EXISTS guncelleme_tarihi TIMESTAMPTZ DEFAULT now();
```

### Onemli - Bu Hafta

| # | Eylem | Aciklama |
|---|-------|----------|
| 7 | Vercel environment variables kontrol | `NEXT_PUBLIC_SUPABASE_URL` ve `NEXT_PUBLIC_SUPABASE_ANON_KEY` degerlerinin dogru oldugunu dogrula |
| 8 | DNS ayarlari | bjktuzlacimnastik.yisa-s.com subdomain'inin Vercel'e yonlendirildigini dogrula |
| 9 | ManyChat webhook URL'ini guncelle | ManyChat dashboard'da webhook URL'ini tenant-yisa-s production URL'ine ayarla |

---

## Cursor IDE Gorev Listesi

Asagidaki gorevleri Cursor IDE'de sirasiyla calistirin:

### Gorev 1 - Sosyal Medya Auth (Oncelik: YUKSEK)
```
Repo:     /home/ubuntu/repos/tenant-yisa-s
Branch:   main (PR #38 merge sonrasi)
Cursor Prompt:
  "app/api/social/ altindaki tum route'lara (instagram, whatsapp, google-business)
   Supabase auth kontrolu ekle. Her route'da kullanicinin auth.uid() ile 
   user_tenants tablosundan tenant_id'sini dogrula. Sadece kendi tenant'ina
   ait social_media_configs kayitlarina erisebilmeli. x-tenant-id header'i
   yerine Supabase session kullan."
```

### Gorev 2 - RBAC API Route Enforcement (Oncelik: YUKSEK)
```
Repo:     /home/ubuntu/repos/app-yisa-s
Branch:   main (PR #11 merge sonrasi)
Cursor Prompt:
  "lib/middleware/role-auth.ts'deki requireRole() ve requireAnyRole()
   fonksiyonlarini tum API route'lara uygula. Her route icin hangi role'un
   erisebilecegini ROLE_ACCESS_MAP'e gore belirle. Ozellikle:
   - /api/patron/* -> requireRole('patron')
   - /api/franchise/* -> requireAnyRole('patron', 'franchise_sahibi')
   - /api/franchise/athletes/* -> requireAnyRole('patron', 'franchise_sahibi', 'antrenor')
   Mevcut API route dosyalarinin basina auth kontrolu ekle."
```

### Gorev 3 - Dinamik Tenant Landing (Oncelik: ORTA)
```
Repo:     /home/ubuntu/repos/tenant-yisa-s
Branch:   main (PR #38 merge sonrasi)
Cursor Prompt:
  "app/tenant-site/page.tsx'i dinamik hale getir. Franchise slug'ini
   x-franchise-slug header'indan al ve Supabase'den franchise bilgilerini
   cek. Hardcoded BJK Tuzla icerigi yerine DB'den gelen verilerle sayfayi
   doldur. Eger franchise bulunamazsa genel bir 'yakinda' sayfasi goster.
   Middleware'de slug header'i zaten ekleniyor."
```

### Gorev 4 - Davet Sistemi (Oncelik: ORTA)
```
Repo:     /home/ubuntu/repos/app-yisa-s
Branch:   main (PR #11 merge sonrasi)
Cursor Prompt:
  "Patron paneline kullanici davet sistemi ekle. Patron, email adresi ve
   rol secerek yeni kullanici davet edebilmeli. Davet sistemi:
   1. /api/patron/invite POST endpoint'i olustur
   2. Supabase auth.admin.inviteUserByEmail() kullan
   3. user_tenants tablosuna rol ve tenant_id ile kayit ekle
   4. /patron/kullanicilar sayfasina davet formu ekle
   Roller: franchise_sahibi, antrenor, veli, admin, kasa"
```

### Gorev 5 - createServerClient Migration (Oncelik: DUSUK)
```
Repo:     /home/ubuntu/repos/app-yisa-s
Branch:   main (PR #11 merge sonrasi)
Cursor Prompt:
  "lib/middleware/role-auth.ts'deki getUserRole() fonksiyonunda
   @supabase/supabase-js createClient yerine @supabase/ssr
   createServerClient kullan. Mevcut cookies pattern SSR icin standart
   degil ve runtime hata verebilir. @supabase/ssr paketi zaten
   package.json'da mevcut."
```

---

## Teknik Notlar

### franchise_subdomains Durumu
```
bjktuzlacimnastik  -> tenant_id: NULL (BAGLANMALI!)
fenerbahceatasehir -> tenant_id: NULL
kartalcimnastik    -> tenant_id: NULL
```

### tenants Durumu
```
8cc3ea1d -> ad: "BJK Tuzla Cimnastik Spor Kulubu", slug: "bjk-tuzla", durum: "aktif"
```

> **Not:** Tenants tablosunda sadece 1 kayit var. Diger franchise'lar icin tenant kayitlari olusturulmali.

### user_tenants Durumu
```
serdincaltay@gmail.com -> role: "patron", tenant_id: 8cc3ea1d (bjk-tuzla)
```

> **Not:** Baska kullanici yok. Davet sistemi ile yeni kullanicilar eklenecek.
