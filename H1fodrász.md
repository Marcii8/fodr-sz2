# H1 – Projektterv  
**IdőMester – Fodrász Szalon Időpontfoglaló rendszer**

## 0. Projektleírás  
Az IdőMester egy webes időpontfoglaló rendszer fodrászszalonok számára.  
A vendégek online választhatnak szolgáltatást (pl. hajvágás, festés, melír), stylistot és elérhető időpontot az üzlet nyitvatartása alapján.  
A rendszer ütközésmentes foglalást biztosít, visszaigazolást ad, és áttekinthető naptárnézetet kínál a szalon adminisztrációjához.

---

## 1. Csapattagok és szerepek  
A projektet **egyszemélyben** végzem, így a szerepkörök is hozzám tartoznak.

| Név | Szerepkör | Felelősség |
|------|----------|-----------|
| Kóró Marcell József | Fejlesztő, Tesztelő, Dokumentáció felelős | Backend fejlesztés Pythonban, admin és vendég felület prototípus, tesztek, dokumentáció |

**Kommunikáció és nyomon követés:**  
- GitHub Issues és Project Board  
- Heti státuszjegyzet rövid összegzéssel  
- Saját kódreview önellenőrzés formájában

---

## 2. Fejlesztési terv – Mérföldkövek és várható eredmények  

| Mérföldkő | Leszállítandó | Határidő |
|-----------|-------------|---------|
| **H1** | Projektterv (jelen dokumentum) | 6. hét |
| **H2** | Vízió dokumentum + frissített projektterv + munkanapló | 6. hét |
| **H3** | SRS, Szótár, Felhasználói kézikönyv (1. verzió) | 6. hét |
| **H4** | Analízis modell + Adatmodell + Architektúra | 9. hét |
| **H5** | MVP prototípus (foglalás/lemondás, ütközéskezelés) + Tesztterv | 12. hét |

> **Megjegyzés:** A szolgáltatások, stylistok és nyitvatartás konfigurálhatóak lesznek JSON/SQLite alapon.

---

## 3. Programozási nyelvek és fejlesztő eszközök

### Programozási nyelv
- **Python** – REST API backend és minimál felhasználói felület

### IDE-k és fejlesztői eszközök
- Visual Studio Code / PyCharm Community  
- Git + GitHub (Issues, Projects, Actions CI)

### Frameworkök és technológiák
- **FastAPI** vagy Flask (végleges döntés H2/H3 fázisban)
- SQLite (később PostgreSQL-re emelhető)
- **pytest** – egység és integrációs tesztek
- Docker – fejlesztői és demó környezethez

---

## 4. Tervezett módszerek és technikák

### Fejlesztési módszertan
- Iteratív fejlesztés (heti mini-sprintek)
- **MVP fókusz**: először foglalás → majd admin funkciók

### Tesztelési módszerek
- Egységtesztek: időütközés, foglalási logika
- Integrációs tesztek: API működés (foglalás/lemondás)
- Manuális elfogadási teszt – tipikus felhasználói folyamatokra (1 vendég, 1 stylist)

### Telepítés
- Docker image / GitHub Pages dokumentációs nézet
- GitHub Actions – automatikus tesztfuttatás (későbbi fázisban)

---

## 5. Dokumentumok és ütemezés

| Dokumentum | Felelős | Határidő |
|-----------|--------|---------|
| Vízió dokumentum | Kóró Marcell József | 6. hét |
| SRS + Szótár | Kóró Marcell József | 6. hét |
| Analízis modell | Kóró Marcell József | 9. hét |
| Felhasználói dokumentáció | Kóró Marcell József | 12. hét |
| Tesztterv | Kóró Marcell József | 12. hét |
| Prototípus kód | Kóró Marcell József | 12. hét |

---

## 6. Tesztelési terv (előnézet)
- **Egységteszt cél**: Legalább 70% lefedettség kritikus logikai modulokra
- **Integrációs teszt**: Foglalás, időütközés-kezelés, lemondás
- **Manuális teszt**: Böngészőből „vendég foglal” + „admin jóváhagy / lemond”

---

## 7. Bemutatási és leszállítási terv
- **Bemutató fázis:** élő demó – szolgáltatás kiválasztása → stylist választás → időpont → foglalás rögzítése
- **Leszállítás:** GitHub repo + (opcionálisan) Docker image és README telepítési leírással

---

## 8. Források
- **Python docs** – docs.python.org  
- **FastAPI / Flask dokumentációk**  
- **GitHub Actions / CI pipeline példák**  
- *Robert C. Martin: Clean Code*
