# nevera-realtime-weather-hr
Nevera Realtime Weather v1.1
# Nevera Realtime Weather

**Nevera Realtime Weather** je premium skripta za FiveM servere koja sinkronizira vrijeme i vremenske uvjete u igri s realnim podacima putem OpenWeatherMap API-ja.

## Značajke

- **Sinkronizacija stvarnog vremena**: Dohvaća realne vremenske podatke za bilo koji grad
- **Dinamička sinkronizacija sata**: Sinkronizira vrijeme u igri sa stvarnim vremenom
- **Automatski prijelazi vremenskih uvjeta**: Glatki prijelazi između vremenskih uvjeta
- **Napredni sustav vjetra**: Dinamička brzina i smjer vjetra prema stvarnim podacima
- **Sustav obavijesti**: Elegantne obavijesti o promjenama vremena
- **Resursno učinkovita**: Optimizirani kod s minimalnim korištenjem resursa (0.01ms u idle stanju)
- **Serversko keširanje**: Smanjuje API pozive i pruža fallback tijekom nedostupnosti servisa
- **Kontrola magle**: Opcija za onemogućavanje magle u regijama gdje je rijetka
- **Kompatibilna s više frameworka**: Radi s ESX, QBCore, vRP ili kao Standalone
- **Prilagodljiva**: Jednostavna konfiguracija putem config.lua datoteke

### View Images
1. **Data synchronization**:
   ![Prva slika](https://i.imgur.com/8S7uUxb.png)

2. **Data update**:
   ![Ažuriranje podataka](https://i.imgur.com/axpJm9s.png)

3. **Resmon value in game**:
   ![Resmon](https://i.imgur.com/0L9ETkn.png)

4. **Clock display in the upper left corner every 10 minutes, with a duration of 15 seconds**: 
   ![Prikaz sata](https://i.imgur.com/CovWD3l.png)

### Zahtjevi

- **FiveM Server**: Najnovija verzija
- **OpenWeatherMap API ključ**: Besplatna verzija savršeno funkcionira
- **Framework**: Kompatibilna s ESX, QBCore, vRP ili kao Standalone

### **Instalacija**

1. **Kupite i preuzmite** resurs s Tebex-a
2. **Raspakirajte datoteke** u mapu resursa vašeg servera
3. **Konfigurirajte `server.cfg`** sa sljedećim postavkama:

```cfg
## **Nevera Realtime Weather konfiguracija**
set my_sync_key "VAŠ_API_KLJUČ"           # Vaš OpenWeatherMap API ključ
set my_sync_timezone "Europe/Zagreb"      # Vaša vremenska zona
set my_sync_city "Split"                  # Vaš grad
set nevera_license_key "LICENČNI_KLJUČ"   # Vaš Tebex licenčni ključ
set disable_fog "true"                    # Postavite na "false" za uključivanje magle

### **Pokretanje resursa**
ensure nevera-realtime-weather
Kako dobiti API ključ

### **Posjetite OpenWeatherMap**
Napravite besplatni račun
Idite u API keys sekciju u vašem profilu
Generirajte novi API ključ
Koristite taj ključ u vašem server.cfg

### **Korištenje**
Resurs automatski počinje raditi nakon instalacije. On će:

Dohvaćati vremenske podatke svakih 10 minuta
Prikazivati vremenske obavijesti 15 sekundi nakon svakog ažuriranja
Sinkronizirati vrijeme u igri sa stvarnim vremenom
Prilagođavati vremenske uvjete prema stvarnim podacima

### **Opcije konfiguracije**
Sve opcije možete pronaći i mijenjati u config.lua datoteci:
OpcijaOpisZadanoConfig.OpenWeatherAPIKeyVaš OpenWeatherMap API ključPotrebno postavitiConfig.CityGrad za koji se dohvaćaju vremenski podaci"Split"Config.TimezoneVremenska zona za sinkronizaciju"Europe/Zagreb"Config.NotificationDurationTrajanje obavijesti u ms15000Config.DisplayFormatPozicija obavijesti"topLeft"Config.DisableFogOnemogućavanje magletrueConfig.UseSnowOmogućavanje snijegatrueConfig.WeatherUpdateIntervalInterval ažuriranja u ms600000Config.EnableWindOmogućavanje vjetratrueConfig.HighWindThresholdPrag za jaki vjetar (m/s)10
Performanse
Ovaj resurs je visoko optimiziran:

Potrošnja u idle stanju: 0.01ms
Tijekom ažuriranja vremena: 0.02-0.03ms (kratki skok)
Korištenje memorije: Minimalno

### Kompatibilnost
Nevera Realtime Weather je dizajnirana da radi sa svim mogućim FiveM serverima:
FrameworkKompatibilnostESX✅ PotpunaQBCore✅ PotpunavRP✅ PotpunaStandalone✅ PotpunaPrilagođeni✅ Potpuna
Bez obzira koji framework koristite ili planirate koristiti u budućnosti,
Nevera Realtime Weather će raditi besprijekorno, bez potrebe za dodatnim podešavanjima!
Povijest verzija
v1.1.0 (Svibanj 2025)

Velike optimizacije performansi
Dodano serversko keširanje odgovora
Poboljšana logika sinkronizacije vremena
Dodan fallback mehanizam tijekom nedostupnosti API-ja
Poboljšan sustav vjetra
Ispravljeni razni rubni slučajevi

v1.0.0 (Inicijalno izdanje)

Sinkronizacija vremenskih uvjeta u stvarnom vremenu
Sinkronizacija vremena
Podrška za više frameworka

### **Česta pitanja**

**Kako mogu produžiti trajanje prikaza obavijesti o vremenu?**
U datoteci `config.lua` možete promijeniti postavku `Config.NotificationDuration` na željeni broj milisekundi. 
Na primjer, za prikaz koji traje 30 sekundi:
```lua
Config.NotificationDuration = 30000  -- 30 sekundi (30000 ms)

### **Podrška**
Za podršku, kontaktirajte nas putem:

**Tebex poruka**
**Discord**: discord.gg/DA9FZ4RmpG
**Email**: nevera.rp@gmail.com

### Licenca
Ovo je komercijalni softver. Neovlašteno distribuiranje je zabranjeno.
© 2025 Nevera, Sva prava pridržana.

### 6. **LICENSE**
```markdown
# Nevera Realtime Weather - Komercijalna licenca

### Ugovor o licenciranju softvera

Ovaj Ugovor o licenciranju softvera ("Ugovor") je pravni ugovor između vas (bilo pojedinca ili pravne osobe) i Nevere ("Autor") za softverski proizvod identificiran iznad, koji uključuje računalni softver i pripadajuće medije i dokumentaciju ("Softver").

Instaliranjem, kopiranjem ili korištenjem Softvera na bilo koji način, pristajete biti vezani uvjetima ovog Ugovora. Ako ne pristajete na uvjete ovog Ugovora, nemojte instalirati ili koristiti Softver.

### 1. **DODJELA LICENCE**

### 1.1 **Licenca za jedan server**
Ova licenca vam daje pravo instaliranja i korištenja Softvera na jednoj instanci FiveM servera.

### 1.2 **Ograničenja**
**NE smijete**:
- Koristiti Softver na više od jedne instance FiveM servera bez kupnje dodatnih licenci
- Distribuirati, dijeliti, iznajmljivati, prodavati ili podlicencirati Softver
- Modificirati, dekompilirati, obrnuto inženjerstvo, rastaviti ili stvarati izvedena djela temeljena na Softveru
- Uklanjati bilo kakve oznake vlasništva ili oznake sa Softvera
- Koristiti Softver za ilegalne ili neovlaštene svrhe

### 2. **INTELEKTUALNO VLASNIŠTVO I VLASNIŠTVO**

Softver je zaštićen zakonima o autorskim pravima i međunarodnim ugovorima o autorskim pravima, kao i drugim zakonima i ugovorima o intelektualnom vlasništvu. Softver je licenciran, a ne prodan. Autor zadržava sva prava, naslov i interes za i u Softveru, uključujući sva prava intelektualnog vlasništva.

### 3. **TRAJANJE I RASKID**

Ovaj Ugovor je na snazi dok se ne raskine. Autor može raskinuti ovaj Ugovor ako ne ispunite bilo koji uvjet ili odredbu ovog Ugovora. Nakon raskida, morate uništiti sve kopije Softvera i sve njegove komponente.

### 4. **BEZ JAMSTVA**

Autor izričito odriče bilo kakvo jamstvo za Softver. Softver se pruža "KAKAV JEST" bez ikakvog izričitog ili impliciranog jamstva bilo koje vrste, uključujući, ali ne ograničavajući se na bilo kakva jamstva za mogućnost prodaje, nekršenje ili prikladnost za određenu svrhu.

### 5. OGRANIČENJE ODGOVORNOSTI

Autor ni u kojem slučaju neće biti odgovoran za bilo kakvu štetu (uključujući, bez ograničenja, izgubljenu dobit, prekid poslovanja ili izgubljene informacije) koja proizlazi iz korištenja ili nemogućnosti korištenja Softvera, čak i ako je Autor bio obaviješten o mogućnosti takve štete.

### 6. OPĆE ODREDBE

Ovaj Ugovor predstavlja cjeloviti sporazum između vas i Autora i zamjenjuje sve prethodne izjave, predstavljanja ili sporazume, bilo usmene ili pisane.

### 7. MJERODAVNO PRAVO

Ovaj Ugovor će biti uređen zakonima Republike Hrvatske.

Autorska prava © 2025 Nevera. Sva prava pridržana.
