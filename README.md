# Nevera Realtime Weather

**Nevera Realtime Weather** je premium skripta za FiveM servere koja sinkronizira vrijeme i vremenske uvjete u igri s realnim podacima putem OpenWeatherMap API-ja.

---

## Značajke

- **Sinkronizacija stvarnog vremena** – Dohvaća vremenske podatke za bilo koji grad
- **Dinamička sinkronizacija sata** – Vrijeme u igri prati stvarno
- **Automatski prijelazi** – Glatke promjene između vremenskih uvjeta
- **Vjetar** – Dinamična brzina i smjer prema stvarnim podacima
- **Obavijesti** – Prikaz vremena svakih 10 minuta
- **Resursno učinkovita** – 0.01ms u idle stanju
- **Fallback sustav** – Radi čak i kad je API nedostupan
- **Magla i snijeg** – Potpuna konfiguracija
- **Framework kompatibilnost** – ESX, QBCore, vRP i Standalone
- **Laka konfiguracija** – `config.lua` s detaljnim opcijama

---

## Zahtjevi

- **FiveM server** – Najnovija verzija
- **OpenWeatherMap API ključ** – Može biti besplatan
- Kompatibilnost: **ESX**, **QBCore**, **vRP**, **Standalone**

---

## Instalacija

1. Kupite i preuzmite resurs s Tebex-a
2. Raspakirajte u `resources` mapu vašeg servera
3. Dodajte sljedeće u `server.cfg`:

```cfg
# Nevera Realtime Weather konfiguracija
set my_sync_key "VAŠ_API_KLJUČ"           # Vaš OpenWeatherMap API ključ
set my_sync_timezone "Europe/Zagreb"      # Vaša vremenska zona
set my_sync_city "Split"                  # Grad koji želite sinkronizirati
set nevera_license_key "LICENČNI_KLJUČ"   # Vaš Tebex licenčni ključ
set disable_fog "true"                    # Postavite na "false" za uključivanje magle

ensure nevera-realtime-weather
```

---

## Kako do API ključa

1. Posjeti [openweathermap.org](https://openweathermap.org/)
2. Registriraj se i idi u **API Keys**
3. Generiraj ključ i zalijepi ga u `server.cfg`

---

## Konfiguracija (`config.lua`)

Primjeri opcija:

```lua
Config.OpenWeatherAPIKey = "VAŠ_KLJUČ"
Config.City = "Split"
Config.Timezone = "Europe/Zagreb"
Config.NotificationDuration = 15000
Config.DisplayFormat = "topLeft"
Config.DisableFog = true
Config.UseSnow = true
Config.WeatherUpdateInterval = 600000
Config.EnableWind = true
Config.HighWindThreshold = 10
```

---

## Performanse

- Idle: **0.01ms**
- Ažuriranje: **0.02-0.03ms**
- Minimalna potrošnja memorije

---

## Kompatibilnost

| Framework     | Podržano |
|---------------|----------|
| ESX           | ✅        |
| QBCore        | ✅        |
| vRP           | ✅        |
| Standalone    | ✅        |
| Custom        | ✅        |

---

## Verzije

### v1.1.0 – Svibanj 2025
- Dodano serversko keširanje
- Fallback sustav za API
- Optimizacija performansi
- Bolji sustav vjetra

### v1.0.0 – Inicijalna verzija
- Realno vrijeme i vremenski uvjeti
- Notifikacije
- Podrška za više frameworka

---

## Screenshots

**1. Vremenska sinkronizacija**
![Data Sync](https://i.imgur.com/8S7uUxb.png)

**2. API odgovor**
![Update](https://i.imgur.com/axpJm9s.png)

**3. Resmon performanse**
![Resmon](https://i.imgur.com/0L9ETkn.png)

**4. Prikaz sata i vremena**
![Sat](https://i.imgur.com/CovWD3l.png)

---

## Česta pitanja

**Kako produljiti trajanje obavijesti o vremenu?**

U `config.lua`:

```lua
Config.NotificationDuration = 30000  -- 30 sekundi
```

---

## Podrška

- 📬 Tebex poruka
- 💬 Discord: [discord.gg/DA9FZ4RmpG](https://discord.gg/DA9FZ4RmpG)
- ✉️ Email: nevera.rp@gmail.com

---

## Licenca

Korištenje dopušteno samo za jedan server. Zabranjena je redistribucija i izmjene bez dopuštenja.

© 2025 Nevera. Sva prava pridržana.

---

## LICENSE

```markdown
# Nevera Realtime Weather - Komercijalna licenca

## Ugovor o licenciranju softvera

Pravni ugovor između korisnika i autora Nevera. Instaliranjem pristajete na uvjete. Ako ne, ne koristite softver.

## 1. LICENCA

Licenca vrijedi za **jedan server**. Ne smijete:
- Koristiti na više servera bez dodatnih licenci
- Dijeliti, prodavati, mijenjati, rastavljati ili dekompilirati softver
- Koristiti softver u neovlaštene ili ilegalne svrhe

## 2. VLASNIŠTVO

Softver ostaje intelektualno vlasništvo autora.

## 3. RASKID

Kršenjem uvjeta licenca se automatski raskida.

## 4. JAMSTVO

Softver se pruža **"kakav jest"**, bez ikakvog jamstva.

## 5. ODGOVORNOST

Autor ne odgovara za bilo kakve štete, gubitke ili probleme nastale korištenjem.

## 6. PRAVO

Primjenjuje se zakon Republike Hrvatske.

© 2025 Nevera. Sva prava pridržana.
```
