# ScriptMaster Pro - Complete Projectdocumentatie

## 📋 Overzicht

ScriptMaster Pro is een AI-powered schrijfplatform voor scenarioschrijvers, geïnspireerd door de Actor's Tool. Het combineert **analyse** van bestaande scripts met **actieve schrijfhulp** tijdens het creatieve proces.

**Doel:** Een schrijver helpen van idee → afgewerkt script, met AI-ondersteuning en de wijsheid van 100 meesterlijke schrijvers.

**Tech Stack:**
- Single HTML file (zoals Actor's Tool)
- Vanilla JavaScript
- localStorage voor persistence
- Cloudflare Worker proxy: `actingtool.ferencsomogyi.workers.dev/v1/messages`
- Claude API (claude-sonnet-4-20250514)
- PDF.js voor PDF parsing
- Mammoth.js voor DOCX parsing

**Live URL:** `https://ferrisomogyi.github.io/scriptmaster-pro/`

---

## 🏗️ App Structuur - 7 Hoofdsecties

### 1. Scripts (Analyse)
**Status:** ✅ Gebouwd
- Bulk upload (.txt, .fountain, .pdf, .docx)
- Automatische parsing van scenes, karakters, locaties
- Scene viewer
- Script statistieken

### 2. Schrijf Assistent (Creatie) ⭐ HOOFDFUNCTIE
**Status:** ✅ Volledig gebouwd met 5 subtabs

**Subtabs:**
1. **Beat Planner** - 6 schrijfmethodes met progress tracking
2. **Scene Builder** - Complete scenes genereren
3. **Dialoog Generator** - 3 versies per dialoog
4. **Conflict Escalator** - 5 escalatieniveaus
5. **Plot Twist** - Verrassende wendingen genereren

**Kernfeature:** 🎓 **100 Meesters Dropdown** - beschikbaar in ALLE tools
- Selecteer een meester-schrijver
- AI schrijft in hun stijl en past hun technieken toe
- Gegroepeerd per categorie (Structuur, Karakter, Dialoog, TV, Comedy, Horror, Sci-Fi, Internationaal)

### 3. Karakters (Analyse)
**Status:** ✅ Gebouwd
- Automatisch geëxtraheerd uit scripts
- Dialoog count per karakter
- In welke scripts/scenes ze voorkomen

### 4. Locaties (Analyse)
**Status:** ✅ Gebouwd
- Alle INT./EXT. locaties
- Scene links per locatie

### 5. Storyframe (Analyse/Creatie)
**Status:** ✅ Gebouwd
- Lange lijn → 10 weken breakdown
- 5-acten structuur
- 6 genres (Drama, YA, RomCom, Thriller, Family, Social)
- AI-generated beats per week
- **🎓 Meester dropdown** voor stijlkeuze

### 6. Continuïteit (Analyse)
**Status:** ✅ Gebouwd
- Cross-script consistentie check
- Naamvariaties detectie
- Locatie inconsistenties

### 7. AI Chat
**Status:** ✅ Gebouwd
- Chat met Claude over je scripts
- Context-aware (kent je scripts, karakters, locaties)

---

## 🎓 100 Meesters Database

### Hoe het werkt
In elke tool (Beat Planner, Scene Builder, Dialoog Generator, etc.) zie je een **"Schrijf in de stijl van"** dropdown. Selecteer een meester en de AI past hun unieke stijl en technieken toe.

### Categorieën

| Categorie | Voorbeelden | Focus |
|-----------|-------------|-------|
| **Structuur & Plot** | Robert McKee, Blake Snyder, Christopher Nolan | Verhaalstructuur, twists |
| **Karakter & Arc** | Aaron Sorkin, Phoebe Waller-Bridge, Greta Gerwig | Karakter ontwikkeling |
| **Dialoog** | Quentin Tarantino, Woody Allen, Nora Ephron | Dialoog schrijven |
| **TV Series** | Vince Gilligan, David Chase, Shonda Rhimes | Serie formats |
| **Comedy** | Judd Apatow, Tina Fey, Edgar Wright | Komische timing |
| **Horror & Thriller** | Jordan Peele, Ari Aster, Alfred Hitchcock | Spanning opbouwen |
| **Sci-Fi & Fantasy** | Denis Villeneuve, George Lucas, Ursula K. Le Guin | Wereldbouw |
| **Internationaal** | Bong Joon-ho, Pedro Almodóvar, Park Chan-wook | Internationale stijlen |

### Voorbeeld gebruik
```
Scene Builder + Aaron Sorkin → Walk-and-talk scenes met snelle dialoog
Conflict Escalator + Ari Aster → Langzame dread, familie-trauma escalatie
Plot Twist + Christopher Nolan → Tijds-twists, non-lineaire onthullingen
```

---

## 🛠️ Features Per Tool

### Beat Planner
- **6 methodes:** Save the Cat, Story Circle, 3-Act, Hero's Journey, Sequence, Mini-Movie
- **Progress bar:** Visueel hoeveel beats zijn ingevuld
- **AI Suggesties:** 3 opties per beat (Conventioneel, Verrassend, Gedurfd)
- **Meester Tips:** Random tips van relevante schrijvers
- **Export:** Download beats als TXT of JSON

### Scene Builder
- **Volledig formulier:** INT/EXT, locatie, tijd, karakters, doel, conflict, toon
- **AI generatie:** Complete scene in screenplay format
- **Export:** Download als .fountain bestand
- **Copy:** Kopieer naar clipboard

### Dialoog Generator
- **Input:** Spreker, luisteraar, doel, subtext, toon
- **Output:** 3 versies - Subtiel, Direct, Gedurfd
- **Per versie:** Beschrijving + dialoog

### Conflict Escalator
- **Input:** Beschrijf je basisconflict
- **Output:** 5 escalatieniveaus (1-5)
- **Visueel:** Kleurcodering van groen (mild) naar rood (explosief)
- **Per niveau:** Naam, beschrijving, scene voorbeeld

### Plot Twist Generator
- **5 categorieën:** Karakter, Perspectief, Tijd, Relatie, Realiteit
- **Per twist:** Titel, setup, reveal, impact, filmvoorbeeld
- **Filter:** Zoek per categorie of genereer mix

---

## 🌐 Taalinstelling

**Alle AI output is in het Nederlands:**
- Suggesties, scenes, dialogen, twists - alles Nederlands
- UI elementen zijn Nederlands
- Meester quotes blijven in originele taal (Engels) voor authenticiteit

---

## 📁 Bestanden in Repository

```
scriptmaster-pro/
├── index.html              # Hoofd applicatie (~4200 regels)
├── manifest.json           # PWA manifest voor app-installatie
├── sw.js                   # Service worker voor offline gebruik
└── SCRIPTMASTER_PRO_DOCUMENTATION.md  # Dit document
```

---

## 🚀 Installatie & Gebruik

### Als Website
Ga naar: `https://ferrisomogyi.github.io/scriptmaster-pro/`

### Als App (PWA)
1. Open de URL in Chrome (mobiel of desktop)
2. Klik op "Installeren" of "Toevoegen aan startscherm"
3. De app werkt nu als standalone applicatie

### API Key instellen
1. Klik op ⚙️ Settings (rechtsboven)
2. Vul je Claude API key in (begint met `sk-ant-...`)
3. Proxy URL staat al goed: `https://actingtool.ferencsomogyi.workers.dev/v1/messages`

---

## ✅ Voltooide Features (januari 2026)

- [x] 7 hoofdsecties volledig functioneel
- [x] Beat Planner met 6 schrijfmethodes
- [x] Scene Builder met screenplay output
- [x] Dialoog Generator met 3 versies
- [x] Conflict Escalator met 5 niveaus
- [x] Plot Twist Generator met 5 categorieën
- [x] 100 Meesters Database geïntegreerd in alle tools
- [x] Nederlandse AI output
- [x] Export functionaliteit (TXT, JSON, Fountain)
- [x] PWA ondersteuning (installeerbaar als app)
- [x] Responsive design voor mobiel

---

## 🔮 Mogelijke Toekomstige Uitbreidingen

1. [ ] Character Arc Builder - volg karakter ontwikkeling per beat
2. [ ] Theme Tracker - houd thema's bij door het script
3. [ ] Outline to Script - genereer volledige scripts uit beats
4. [ ] Collaboration features - delen met andere schrijvers
5. [ ] Version history - track wijzigingen over tijd
6. [ ] Import bestaande scripts voor analyse
7. [ ] Meer schrijfmethodes toevoegen
8. [ ] Karakter-specifieke dialoog stijlen

---

## 📝 Voor Volgende Chat Sessies

Bij het starten van een nieuwe chat:
1. Upload dit document
2. Zeg: "Ik wil verder werken aan ScriptMaster Pro"
3. Claude kan direct verder bouwen met volledige context

**Huidige Status:** ✅ Volledig functioneel en live

---

*Laatst bijgewerkt: 12 januari 2026*
*Versie: 2.1 - Meesters Dropdown Integratie*
