# H2 – Követelmény-analízis  
*IdőMester – Fodrász Szalon Időpontfoglaló*

---

## 1. Leadandó összefoglaló  
A H2 mérföldkő három fő dokumentumból áll:
- **Vízió dokumentum** – célok, probléma, felhasználói körök, kockázatok és szótár  
- **Projektterv kivonat** – mérföldkövek, erőforrások és ütemezés  
- **Munkanapló** – az egyéni munka követése

---

## 2. Vízió dokumentum

### 2.1 Címlap  
- **Projekt neve:** IdőMester — Fodrász Szalon Időpontfoglaló  
- **Verzió:** v0.9 (H2-tervezet)  
- **Dátum:** 2025.10.

### 2.2 Bevezetés  
Az IdőMester célja egy online foglalási rendszer létrehozása fodrászszalonok számára.  
A rendszer támogatja:
- Szolgáltatás választását
- Stylist kiválasztását
- Ütközésmentes időpontfoglalást
- Adminisztrátori foglaláskezelést

### 2.3 Probléma megfogalmazása  
| Probléma | Következmény |
|----------|-------------|
| Telefonos vagy chat alapú időpont-egyeztetés | Duplikált vagy elfelejtett foglalások, pontatlanság |
| Nincs átlátható foglalási naptár | Stylistok túlterhelése vagy üres időblokkok |
| Manuális időpont-bejegyzés | Hibalehetőségek, nem skálázható folyamat |

### 2.4 A termék helye a piacon  
A célcsoport: **kisebb, független fodrászszalonok**, akiknek túl bonyolult vagy drága a nagy rendszerek használata.  
**Megkülönböztető előnyök:**
- Egyszerű, célratörő rendszer (nem túlkomplikált)
- Webalapú, telepítés nélkül használható
- Kevés erőforrással is működik

### 2.5 Felhasználói környezet  
| Szereplő | Leírás |
|----------|-------|
| Vendég | Kiválasztja a szolgáltatást és időpontot |
| Stylist | Foglalásokat látja, naptárnézetet használ |
| Admin | Foglalásokat felülírhat, naptárt kezel |

Használat eszközökről: **mobil + böngésző**, nincs natív app követelmény.

### 2.6 A termék előnyei  
- **Vendég:** gyors foglalás 0–24  
- **Szalon:** kevesebb telefonhívás, átlátható napi terhelés  
- **Stylist:** szervezett munkabeosztás

### 2.7 Feltételezések és függőségek  
- Internetkapcsolat rendelkezésre áll  
- A szalon biztosít nyitvatartási adatokat  
- Adatbázis elérhető a futtatás során  

### 2.8 Fő funkciók

| Kategória | Funkció | Leírás |
|-----------|--------|-------|
| **Kötelező** | Foglalás létrehozása | Vendég választ szolgáltatást, stylistot és időpontot |
| **Kötelező** | Naptárnézet | Stylist/Admin böngészi a foglalásokat |
| **Kötelező** | Lemondás / módosítás | Vendég vagy admin végrehajthatja |
| **Ajánlott** | Automatikus email visszaigazolás | Foglalás után visszajelzés |
| **Jó, ha van** | Foglalások exportja (CSV/ICS) | Admin le tudja tölteni az adatokat |

### 2.9 Minőségi követelmények (NFR)

| Típus | Elvárás |
|------|--------|
| Teljesítmény | API válasz ≤ 300ms fejlesztői környezetben |
| Biztonság | Jelszavak biztonságos tárolása, jogosultságkezelés |
| Használhatóság | Mobilbarát felület, egyértelmű UI |
| Karbantarthatóság | Kódszerkezet moduláris legyen, dokumentált funkciók |

### 2.10 Kockázatok

| Kockázat | Valószínűség | Hatás | Kezelés |
|---------|-------------|-------|--------|
| Ütközéskezelési hiba | Közepes | Magas | Egységtesztek, logikai ellenőrzés |
| Naptárazás időzónával | Alacsony | Közepes | UTC tárolás, lokális megjelenítés |
| Adatvédelem hiánya | Közepes | Magas | Jogosultság-szintek, titkosított tárolás |
| Fejlesztési scope növekedése | Közepes | Közepes | MVP priorizálás, backlog kontroll |

### 2.11 Szótár / fogalomtár

| Fogalom | Jelentés |
|--------|---------|
| **Szolgáltatás** | Fodrász tevékenység fix időtartammal |
| **Stylist** | A szolgáltatást végző szakember |
| **Időablak** | Foglalható idősáv a nyitvatartáson belül |
| **Foglalás** | Vendég által rögzített időpont szolgáltatással |
| **Naptárnézet** | Napi/heti megjelenítés admin/stylist számára |

---

## 3. Projektterv (H2 kivonat)

### 3.1 Csapattagok és szerepek  
**Egyéni projekt** – minden szerepet egy fő lát el

### 3.2 Mérföldkövek  

| Mérföldkő | Leszállítandó | Határidő |
|-----------|-------------|---------|
| H1 | Projektterv | 6. hét |
| H2 | Vízió + Projektterv + Munkanapló | 6. hét |
| H3 | SRS + Szótár | 6. hét |
| H4 | Analízis modell + Tervezés | 9. hét |
| H5 | MVP + Tesztterv | 12. hét |

### 3.3 Eszközök  
- **Python** backend  
- **FastAPI/Flask**
- **SQLite**
- **GitHub** verziókövetés + projektkezelés
- **pytest** automata teszteléshez

### 3.4 Tesztelés  
- Egységtesztek: ≥70% domain logika  
- Integrációs tesztek: API végpontok  
- Manuális UAT: tipikus foglalási folyamat

### 3.5 Bemutatás és leszállítás  
- **Demó:** Foglalási folyamat élőben bemutatva  
- **Átadás:** GitHub repó + opcionális Docker image  

---

## 4. Munkanapló (sablon)

| Dátum | Tag | Feladat | Idő (óra) |
|------|-----|--------|-----------|
| 2025-10-16 | Kóró Marcell József | Vízió vázlat + funkciólista | 2 |
| 2025-10-17 | Kóró Marcell József | Probléma megfogalmazása + piaci pozíció | 1.5 |
| 2025-10-18 | Kóró Marcell József | Szótár + NFR kidolgozása | 1.5 |

---

## Zárás
A H2 mérföldkő lezárásával a projekt céljai és követelményei egyértelműen definiálva vannak. A következő fázis a **részletes funkcionalitás leírása és SRS készítés (H3)**.

