# ScriptMaster Pro - Complete Projectdocumentatie

## 📋 Overzicht

ScriptMaster Pro is een AI-powered schrijfplatform voor scenarioschrijvers, geïnspireerd door de Actor's Tool. Het combineert **analyse** van bestaande scripts met **actieve schrijfhulp** tijdens het creatieve proces.

**Doel:** Een schrijver helpen van idee → afgewerkt script, met AI-ondersteuning en de wijsheid van de beste schrijvers ter wereld.

**Tech Stack:**
- Single HTML file (zoals Actor's Tool)
- Vanilla JavaScript
- localStorage voor persistence
- Cloudflare Worker proxy: `actingtool.ferencsomogyi.workers.dev`
- Claude API (claude-sonnet-4-20250514)
- PDF.js voor PDF parsing
- Mammoth.js voor DOCX parsing

**GitHub Deploy:**
- Repository: `scriptmaster-pro`
- URL: `ferrisomogyi.github.io/scriptmaster-pro`

---

## 🏗️ App Structuur - 8 Secties

### 1. Scripts (Analyse)
**Status:** ✅ Gebouwd
- Bulk upload (.txt, .fountain, .pdf, .docx)
- Automatische parsing van scenes, karakters, locaties
- Scene viewer
- Script statistieken

### 2. Karakters (Analyse)
**Status:** ✅ Gebouwd
- Automatisch geëxtraheerd uit scripts
- Dialoog count per karakter
- In welke scripts/scenes ze voorkomen

### 3. Locaties (Analyse)
**Status:** ✅ Gebouwd
- Alle INT./EXT. locaties
- Scene links per locatie

### 4. Storyframe (Analyse/Creatie)
**Status:** ✅ Gebouwd
- Lange lijn → 10 weken breakdown
- 5-acten structuur
- 6 genres (Drama, YA, RomCom, Thriller, Family, Social)
- AI-generated beats per week

### 5. Continuïteit (Analyse)
**Status:** ✅ Gebouwd
- Cross-script consistentie check
- Naamvariaties detectie
- Locatie inconsistenties

### 6. AI Assistent (Chat)
**Status:** ✅ Gebouwd
- Chat met Claude over je scripts
- Context-aware (kent je scripts, karakters, locaties)

### 7. Meester Wijsheid (Referentie)
**Status:** ✅ Basis gebouwd, moet uitgebreid naar 100 schrijvers
- Tips van legendarische schrijvers
- Categorieën: Structuur, Karakter, Dialoog, Thema

### 8. Schrijf Assistent (NIEUW - Te bouwen)
**Status:** ✅ VOLLEDIG GEBOUWD
- Beat Planner met 6 methodes (Save the Cat, Story Circle, 3-Act, Hero's Journey, Sequence, Mini-Movie)
- Scene Builder - genereer volledige scenes
- Dialogue Generator - 3 versies van dezelfde dialoog
- Conflict Escalator - 5 escalatieniveaus
- Plot Twist Generator - 5 categorieën twists
- 100 Meester Schrijvers Database met detail modal
- Export functionaliteit (TXT, JSON, Fountain)
- Progress indicator per methode
- Copy-to-clipboard functionaliteit

---

## 📚 SECTIE 8: SCHRIJF ASSISTENT - Gedetailleerd Ontwerp

### 8.1 Schrijfmethodes (6 methodes)

#### A. Save the Cat (Blake Snyder) - 15 Beats
```
1. Opening Image (p.1) - Tone, mood, "before" snapshot
2. Theme Stated (p.5) - Thema subtiel genoemd
3. Set-up (p.1-10) - Held's wereld, "Six Things That Need Fixing"
4. Catalyst (p.12) - Inciting incident
5. Debate (p.12-25) - Held twijfelt
6. Break into Two (p.25) - Held neemt beslissing, Act 2 begint
7. B Story (p.30) - Subplot, vaak liefdesverhaal
8. Fun and Games (p.30-55) - "Promise of the premise"
9. Midpoint (p.55) - False victory of false defeat
10. Bad Guys Close In (p.55-75) - Stakes verhogen
11. All Is Lost (p.75) - Laagste punt, "whiff of death"
12. Dark Night of the Soul (p.75-85) - Held in wanhoop
13. Break into Three (p.85) - A en B story komen samen
14. Finale (p.85-110) - Held past geleerde lessen toe
15. Final Image (p.110) - "After" snapshot, transformatie compleet
```

#### B. Dan Harmon Story Circle - 8 Stappen
```
1. YOU - Karakter in comfort zone
2. NEED - Iets ontbreekt, verlangen
3. GO - Betreedt onbekend terrein
4. SEARCH - Past zich aan, zoekt
5. FIND - Vindt wat ze zochten
6. TAKE - Betaalt de prijs
7. RETURN - Keert terug naar bekende wereld
8. CHANGE - Is veranderd door de reis
```

#### C. Syd Field 3-Act Paradigm
```
Act 1: Setup (p.1-30)
- Exposition
- Inciting Incident (p.10-15)
- Plot Point 1 (p.25-27)

Act 2: Confrontation (p.30-90)
- Rising Action
- Midpoint (p.55-60)
- Plot Point 2 (p.85-90)

Act 3: Resolution (p.90-120)
- Climax
- Resolution
```

#### D. Hero's Journey (Campbell/Vogler) - 12 Stappen
```
ACT 1 - DEPARTURE
1. Ordinary World
2. Call to Adventure
3. Refusal of the Call
4. Meeting the Mentor
5. Crossing the Threshold

ACT 2 - INITIATION
6. Tests, Allies, Enemies
7. Approach to the Inmost Cave
8. Ordeal
9. Reward (Seizing the Sword)

ACT 3 - RETURN
10. The Road Back
11. Resurrection
12. Return with the Elixir
```

#### E. Sequence Method - 8 Sequenties
```
Seq 1 (p.1-15): Status Quo & Inciting Incident
Seq 2 (p.15-30): Predicament & Lock In
Seq 3 (p.30-45): First Obstacle & Raising Stakes
Seq 4 (p.45-60): First Culmination/Midpoint
Seq 5 (p.60-75): Subplot & Rising Action
Seq 6 (p.75-90): Main Culmination/Low Point
Seq 7 (p.90-105): New Tension & Twist
Seq 8 (p.105-120): Resolution
```

#### F. Mini-Movie Method (Chris Soth)
```
Mini-Movie 1 (p.1-25): Complete mini-verhaal, held reageert
Mini-Movie 2 (p.25-50): Held begint te vechten
Mini-Movie 3 (p.50-75): Held lijkt te winnen, dan grote tegenslag
Mini-Movie 4 (p.75-100): Held overwint obstakels, climax
```

---

### 8.2 Top 100 Schrijvers Database

#### CATEGORIE: STRUCTUUR & PLOT

| # | Schrijver | Bekende Werken | Kerntechniek | Tip |
|---|-----------|----------------|--------------|-----|
| 1 | **Robert McKee** | Story (boek) | Scene als "story event" | "Elke scene moet de waarde van het leven veranderen" |
| 2 | **Syd Field** | Screenplay | 3-Act Paradigm | "Structure is the spine of the story" |
| 3 | **Blake Snyder** | Save the Cat | 15 Beat Sheet | "Give me the same thing, only different" |
| 4 | **Christopher Nolan** | Memento, Inception, Tenet | Non-lineaire structuur | "Play with time to create meaning" |
| 5 | **Quentin Tarantino** | Pulp Fiction, Kill Bill | Chaptered structure, non-lineair | "Start in the middle of action" |
| 6 | **Charlie Kaufman** | Eternal Sunshine, Being John Malkovich | Meta-structuur | "Structure should reflect the theme" |
| 7 | **Christopher McQuarrie** | Usual Suspects, MI series | Twist endings | "Plant seeds early, harvest late" |
| 8 | **David Fincher** | Fight Club, Gone Girl | Unreliable narrator | "Make the audience complicit" |
| 9 | **Denis Villeneuve** | Arrival, Blade Runner 2049 | Slow burn revelation | "Patience in storytelling pays off" |
| 10 | **Guillermo del Toro** | Pan's Labyrinth, Shape of Water | Parallel storylines | "Fairy tale structure for adult themes" |

#### CATEGORIE: KARAKTER & ARC

| # | Schrijver | Bekende Werken | Kerntechniek | Tip |
|---|-----------|----------------|--------------|-----|
| 11 | **Aaron Sorkin** | The Social Network, West Wing | Walk-and-talk, rapid dialogue | "Characters are what they DO, not what they say" |
| 12 | **Phoebe Waller-Bridge** | Fleabag, Killing Eve | Breaking fourth wall, flawed heroes | "Give characters contradictions" |
| 13 | **Greta Gerwig** | Lady Bird, Little Women | Small moments reveal character | "The specific is universal" |
| 14 | **Jordan Peele** | Get Out, Us | Subverted expectations | "Genre as social commentary" |
| 15 | **Bong Joon-ho** | Parasite, Memories of Murder | Class dynamics | "Environment shapes character" |
| 16 | **Taika Waititi** | Jojo Rabbit, Thor Ragnarok | Comedy + tragedy | "Find the funny in the dark" |
| 17 | **Emerald Fennell** | Promising Young Woman | Revenge with purpose | "Subvert the victim narrative" |
| 18 | **Barry Jenkins** | Moonlight, If Beale Street | Intimate character study | "Silence speaks volumes" |
| 19 | **Celine Sciamma** | Portrait of a Lady on Fire | The gaze, unspoken emotion | "Show, don't tell - especially love" |
| 20 | **Sofia Coppola** | Lost in Translation, Virgin Suicides | Mood over plot | "Atmosphere is character" |

#### CATEGORIE: DIALOOG

| # | Schrijver | Bekende Werken | Kerntechniek | Tip |
|---|-----------|----------------|--------------|-----|
| 21 | **David Mamet** | Glengarry Glen Ross, The Untouchables | Sparse, rhythmic dialogue | "People rarely say what they mean" |
| 22 | **Diablo Cody** | Juno, Jennifer's Body | Distinctive voice | "Every character needs their own vocabulary" |
| 23 | **Nora Ephron** | When Harry Met Sally, Sleepless | Natural banter | "Dialogue should be composed like music" |
| 24 | **Armando Iannucci** | Veep, In the Loop | Insult comedy, overlapping | "Comedy timing lives in pauses" |
| 25 | **Joel & Ethan Coen** | Fargo, No Country | Regional dialect | "Dialogue reveals geography and class" |
| 26 | **Woody Allen** | Annie Hall, Manhattan | Neurotic, intellectual | "Let characters talk themselves into corners" |
| 27 | **Richard Linklater** | Before Sunrise trilogy | Philosophical conversation | "Real conversations meander" |
| 28 | **Amy Sherman-Palladino** | Gilmore Girls, Mrs. Maisel | Rapid-fire, reference-heavy | "Density creates character" |
| 29 | **Tony Gilroy** | Michael Clayton, Bourne series | Corporate speak, subtext | "What's NOT said matters most" |
| 30 | **Taylor Sheridan** | Sicario, Yellowstone | Laconic, Western | "Fewer words, more weight" |

#### CATEGORIE: GENRE MASTERY

| # | Schrijver | Bekende Werken | Genre | Kerntechniek |
|---|-----------|----------------|-------|--------------|
| 31 | **James Cameron** | Terminator, Aliens, Titanic | Action/Sci-Fi | "Stakes + spectacle + heart" |
| 32 | **Steven Spielberg** | Jaws, E.T., Schindler's List | Multiple genres | "The Spielberg face - wonder" |
| 33 | **Ridley Scott** | Blade Runner, Gladiator | Sci-Fi/Epic | "World-building through detail" |
| 34 | **Alfred Hitchcock** | Psycho, Vertigo | Thriller | "Suspense vs surprise" |
| 35 | **Stanley Kubrick** | The Shining, 2001 | Psychological | "Precise visual storytelling" |
| 36 | **Martin Scorsese** | Goodfellas, Taxi Driver | Crime/Character | "Voice-over as confession" |
| 37 | **David Lynch** | Mulholland Drive, Twin Peaks | Surreal | "Embrace the unexplainable" |
| 38 | **Wes Anderson** | Grand Budapest, Moonrise Kingdom | Comedy/Whimsy | "Symmetry and control" |
| 39 | **Paul Thomas Anderson** | There Will Be Blood, Boogie Nights | Drama | "Long takes, character immersion" |
| 40 | **Darren Aronofsky** | Black Swan, Requiem | Psychological | "Physical transformation = inner turmoil" |

#### CATEGORIE: TV/SERIES SCHRIJVEN

| # | Schrijver | Bekende Werken | Kerntechniek | Tip |
|---|-----------|----------------|--------------|-----|
| 41 | **Vince Gilligan** | Breaking Bad, Better Call Saul | Slow burn transformation | "Mr. Chips to Scarface" |
| 42 | **David Chase** | The Sopranos | Antihero complexity | "Sympathy for the devil" |
| 43 | **David Simon** | The Wire | Systemic storytelling | "Institutions as characters" |
| 44 | **Shonda Rhimes** | Grey's Anatomy, Scandal | Cliffhangers, diversity | "End every act with a question" |
| 45 | **Dan Harmon** | Community, Rick and Morty | Story Circle | "The embryo of story" |
| 46 | **Damon Lindelof** | Lost, The Leftovers, Watchmen | Mystery boxes | "Questions are more engaging than answers" |
| 47 | **Jesse Armstrong** | Succession | Dark comedy, power dynamics | "Make them awful but watchable" |
| 48 | **Mike White** | The White Lotus | Social satire | "Privilege exposed" |
| 49 | **Noah Hawley** | Fargo (TV), Legion | Tonal shifts | "Genre-bending within episodes" |
| 50 | **Craig Mazin** | Chernobyl, The Last of Us | Research + emotion | "Truth is dramatic enough" |

#### CATEGORIE: COMEDY

| # | Schrijver | Bekende Werken | Kerntechniek | Tip |
|---|-----------|----------------|--------------|-----|
| 51 | **Billy Wilder** | Some Like It Hot, The Apartment | Setup/payoff | "If you have a problem in Act 3, the solution is in Act 1" |
| 52 | **Mel Brooks** | Blazing Saddles, Young Frankenstein | Parody | "Tragedy + time = comedy" |
| 53 | **Judd Apatow** | 40-Year-Old Virgin, Knocked Up | Improv-friendly | "Let actors find the funny" |
| 54 | **Tina Fey** | 30 Rock, Mean Girls | Joke density | "More jokes per page" |
| 55 | **Edgar Wright** | Shaun of the Dead, Hot Fuzz | Visual comedy, callbacks | "Every frame is a setup or payoff" |
| 56 | **Lord & Miller** | 21 Jump Street, LEGO Movie | Meta-comedy | "Acknowledge the absurdity" |
| 57 | **Mike Judge** | Office Space, Silicon Valley | Workplace absurdity | "Mundane horror is comedy" |
| 58 | **Kristen Wiig** | Bridesmaids | Cringe comedy | "Embarrassment is universal" |
| 59 | **Jordan Peele** (comedy) | Key & Peele | Sketch-to-feature | "Social commentary through laughs" |
| 60 | **Seth Rogen & Evan Goldberg** | Superbad, This Is The End | Friendship comedy | "Authentic male friendship" |

#### CATEGORIE: DRAMA & EMOTIE

| # | Schrijver | Bekende Werken | Kerntechniek | Tip |
|---|-----------|----------------|--------------|-----|
| 61 | **Eric Roth** | Forrest Gump, A Star Is Born | Sweeping emotion | "Find the humanity in epic" |
| 62 | **Kenneth Lonergan** | Manchester by the Sea | Grief realism | "Not everyone gets healed" |
| 63 | **Mike Leigh** | Secrets & Lies | Improvised realism | "Character comes from rehearsal" |
| 64 | **Pedro Almodóvar** | Talk to Her, All About My Mother | Melodrama elevated | "Embrace big emotions" |
| 65 | **Wong Kar-wai** | In the Mood for Love | Yearning, missed connections | "What could have been" |
| 66 | **Terrence Malick** | Tree of Life, Badlands | Poetic voice-over | "Inner life narrated" |
| 67 | **Paolo Sorrentino** | The Great Beauty | Decadence and meaning | "Beauty masks emptiness" |
| 68 | **Yorgos Lanthimos** | The Favourite, Poor Things | Absurdist drama | "Alienation as technique" |
| 69 | **Lee Chang-dong** | Burning, Poetry | Ambiguity | "Let audiences complete the story" |
| 70 | **Hirokazu Kore-eda** | Shoplifters, After Life | Quiet family drama | "Found family, chosen bonds" |

#### CATEGORIE: HORROR & THRILLER

| # | Schrijver | Bekende Werken | Kerntechniek | Tip |
|---|-----------|----------------|--------------|-----|
| 71 | **Ari Aster** | Hereditary, Midsommar | Dread, grief-horror | "Family trauma is the real monster" |
| 72 | **Mike Flanagan** | Haunting of Hill House, Midnight Mass | Character-driven horror | "Ghosts are metaphors" |
| 73 | **Robert Eggers** | The Witch, The Lighthouse | Period authenticity | "Research creates atmosphere" |
| 74 | **James Wan** | Saw, Conjuring, Insidious | Set-piece horror | "Build to the scare" |
| 75 | **Leigh Whannell** | Upgrade, Invisible Man | High concept | "One idea, fully explored" |
| 76 | **Ti West** | X, Pearl | Retro horror | "Genre pastiche with depth" |
| 77 | **David Cronenberg** | The Fly, Videodrome | Body horror | "The flesh is the canvas" |
| 78 | **John Carpenter** | Halloween, The Thing | Minimalist suspense | "Less is more scary" |
| 79 | **William Peter Blatty** | The Exorcist | Faith vs evil | "Believe in your mythology" |
| 80 | **Wes Craven** | Nightmare on Elm Street, Scream | Meta-horror | "Know the rules to break them" |

#### CATEGORIE: SCI-FI & FANTASY

| # | Schrijver | Bekende Werken | Kerntechniek | Tip |
|---|-----------|----------------|--------------|-----|
| 81 | **George Lucas** | Star Wars | Mythology in space | "Joseph Campbell in a galaxy far away" |
| 82 | **Peter Jackson & Fran Walsh** | LOTR trilogy | Adaptation, scale | "Respect the source, serve the film" |
| 83 | **Joss Whedon** | Buffy, Firefly, Avengers | Ensemble, quips | "Every character gets their moment" |
| 84 | **The Wachowskis** | The Matrix | Philosophical action | "Ideas can be visualized" |
| 85 | **Alex Garland** | Ex Machina, Annihilation | Cerebral sci-fi | "Science fiction as philosophy" |
| 86 | **Shane Carruth** | Primer, Upstream Color | Hard sci-fi | "Don't explain everything" |
| 87 | **Ted Chiang** | Arrival (Story of Your Life) | Linguistic sci-fi | "Language shapes reality" |
| 88 | **Hayao Miyazaki** | Spirited Away, Princess Mononoke | Environmental fantasy | "Nature as character" |
| 89 | **Terry Gilliam** | Brazil, 12 Monkeys | Dystopian satire | "Bureaucracy is the enemy" |
| 90 | **Neill Blomkamp** | District 9, Elysium | Allegory sci-fi | "Sci-fi as social mirror" |

#### CATEGORIE: INTERNATIONALE MEESTERS

| # | Schrijver | Land | Bekende Werken | Kerntechniek |
|---|-----------|------|----------------|--------------|
| 91 | **Akira Kurosawa** | Japan | Seven Samurai, Rashomon | Multiple perspectives |
| 92 | **Ingmar Bergman** | Sweden | Persona, Seventh Seal | Existential dialogue |
| 93 | **Federico Fellini** | Italy | 8½, La Dolce Vita | Dream logic |
| 94 | **François Truffaut** | France | 400 Blows | Autobiographical |
| 95 | **Andrei Tarkovsky** | Russia | Stalker, Solaris | Poetic imagery |
| 96 | **Park Chan-wook** | Korea | Oldboy, Handmaiden | Revenge aesthetics |
| 97 | **Asghar Farhadi** | Iran | A Separation | Moral complexity |
| 98 | **Alfonso Cuarón** | Mexico | Roma, Children of Men | Long takes, immersion |
| 99 | **Alejandro González Iñárritu** | Mexico | Birdman, Babel | Interconnected stories |
| 100 | **Florian Henckel von Donnersmarck** | Germany | Lives of Others | Surveillance drama |

---

### 8.3 Schrijf Assistent Features (Te Bouwen)

#### Feature 1: Beat Planner
**Functie:** Kies een schrijfmethode, vul per beat je ideeën in, AI helpt met suggesties.

**UI Flow:**
1. Selecteer methode (Save the Cat, Story Circle, etc.)
2. Zie visuele representatie van alle beats
3. Klik op een beat om te bewerken
4. Vul je idee in of klik "AI Suggestie"
5. AI geeft 3 opties:
   - 🟢 **Conventioneel** - Wat het publiek verwacht
   - 🟡 **Verrassend** - Onverwachte twist
   - 🔴 **Gedurfd** - Risicovol maar memorabel
6. Selecteer, pas aan, ga naar volgende beat

**AI Prompt Template:**
```
Je bent een expert scenarioschrijver die helpt met [METHODE].

CONTEXT:
- Genre: [GENRE]
- Logline: [LOGLINE]
- Vorige beats: [VORIGE_BEATS]

HUIDIGE BEAT: [BEAT_NAAM]
Beschrijving: [BEAT_BESCHRIJVING]

Geef 3 suggesties voor deze beat:
1. CONVENTIONEEL: Een solide, verwachte invulling
2. VERRASSEND: Een onverwachte maar logische twist
3. GEDURFD: Een riskante keuze die kan uitbetalen

Per suggestie:
- Korte beschrijving (2-3 zinnen)
- Waarom het werkt
- Voorbeeld uit bekende film
```

#### Feature 2: Scene Builder
**Functie:** Bouw scenes met AI-hulp voor conflict, doel, en dialoog.

**Per Scene Invullen:**
- Locatie (INT/EXT)
- Tijd (DAG/NACHT)
- Karakters aanwezig
- POV karakter
- Scene doel (wat moet bereikt worden)
- Conflict (wat staat in de weg)
- Emotionele beat (hoe moet publiek zich voelen)

**AI Genereert:**
- Opening actie (hoe begint de scene)
- Key dialogue moment
- Scene-ending hook
- Subtext suggesties

#### Feature 3: Meester Integratie
**Functie:** Laat AI schrijven "in de stijl van" een meester.

**Voorbeeld:**
> "Schrijf deze confrontatie-scene in de stijl van Aaron Sorkin"
> → Rapid-fire dialoog, walk-and-talk, characters zijn slim

> "Hoe zou Tarantino dit restaurant gesprek aanpakken?"
> → Pop culture referenties, spanning onder oppervlak, onverwachte uitbarsting

**UI:**
- Dropdown met 100 schrijvers
- Filter op categorie (Structuur, Dialoog, Genre, etc.)
- Klik op schrijver → zie hun technieken + tips
- "Pas toe op mijn scene" button

#### Feature 4: Conflict Escalator
**Functie:** AI helpt om conflict stap voor stap te verhogen.

**Input:** Huidige conflictniveau
**Output:** 5 escalatie-suggesties van mild → explosief

#### Feature 5: Dialogue Generator
**Functie:** Gegeven context, genereer dialoog variaties.

**Input:**
- Wie spreekt
- Tot wie
- Wat willen ze bereiken
- Wat is het obstakel
- Toon (subtiel, direct, agressief)

**Output:** 3 versies van de dialoog

#### Feature 6: Plot Twist Generator
**Functie:** AI suggereert twists die passen bij je verhaal.

**Categorieën:**
- Character revelation (hij was de moordenaar!)
- Perspective shift (unreliable narrator)
- Time twist (we zijn in de toekomst/verleden)
- Relationship twist (ze zijn familie)
- Reality twist (het was een droom/simulatie)

---

### 8.4 UI Design Schrijf Assistent

```
┌─────────────────────────────────────────────────────────────┐
│ SCHRIJF ASSISTENT                                           │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  [Methode: ▼ Save the Cat    ]  [Genre: ▼ Thriller  ]      │
│                                                             │
│  ┌─────────────────────────────────────────────────────┐   │
│  │            BEAT PLANNER (Save the Cat)              │   │
│  │                                                     │   │
│  │  [1. Opening Image  ] ✅ Ingevuld                   │   │
│  │  [2. Theme Stated   ] ✅ Ingevuld                   │   │
│  │  [3. Set-up         ] 🔄 Bezig                      │   │
│  │  [4. Catalyst       ] ⬜ Leeg                       │   │
│  │  [5. Debate         ] ⬜ Leeg                       │   │
│  │  ...                                                │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  ┌─────────────────────────────────────────────────────┐   │
│  │ BEAT 3: SET-UP                                      │   │
│  │                                                     │   │
│  │ Beschrijving: De held's wereld, "Six Things That    │   │
│  │ Need Fixing", alle belangrijke karakters intro      │   │
│  │                                                     │   │
│  │ Jouw idee:                                          │   │
│  │ ┌───────────────────────────────────────────────┐   │   │
│  │ │ Sarah is een workaholic advocaat die haar     │   │   │
│  │ │ familie verwaarloost. Haar dochter...         │   │   │
│  │ └───────────────────────────────────────────────┘   │   │
│  │                                                     │   │
│  │ [🤖 AI Suggestie]  [💡 Meester Tip]                │   │
│  │                                                     │   │
│  │ ┌─ AI SUGGESTIES ─────────────────────────────────┐ │   │
│  │ │ 🟢 CONVENTIONEEL                                │ │   │
│  │ │ Sarah wint een grote zaak maar mist het        │ │   │
│  │ │ schooltoneelstuk van haar dochter...           │ │   │
│  │ │ [Selecteer]                                     │ │   │
│  │ │                                                 │ │   │
│  │ │ 🟡 VERRASSEND                                   │ │   │
│  │ │ Sarah is al gescheiden en krijgt bericht       │ │   │
│  │ │ dat haar ex hertrouwt - met haar beste...      │ │   │
│  │ │ [Selecteer]                                     │ │   │
│  │ │                                                 │ │   │
│  │ │ 🔴 GEDURFD                                      │ │   │
│  │ │ Sarah is succesvol maar leeft dubbelleven      │ │   │
│  │ │ - 's nachts is ze online gokverslaafd...       │ │   │
│  │ │ [Selecteer]                                     │ │   │
│  │ └─────────────────────────────────────────────────┘ │   │
│  │                                                     │   │
│  │ ┌─ MEESTER TIP ───────────────────────────────────┐ │   │
│  │ │ 💬 Blake Snyder:                                │ │   │
│  │ │ "In de Set-up moet je de 'Six Things That      │ │   │
│  │ │ Need Fixing' tonen - dit zijn de dingen die    │ │   │
│  │ │ mis zijn in het leven van je held."            │ │   │
│  │ │                                                 │ │   │
│  │ │ 🎬 Voorbeeld: The Proposal                      │ │   │
│  │ │ Margaret (Sandra Bullock) is gevreesd op       │ │   │
│  │ │ kantoor, heeft geen sociaal leven, en is       │ │   │
│  │ │ op het punt gedeporteerd te worden.            │ │   │
│  │ └─────────────────────────────────────────────────┘ │   │
│  └─────────────────────────────────────────────────────┘   │
│                                                             │
│  [← Vorige Beat]                    [Volgende Beat →]       │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

## 🔧 Technische Implementatie

### State Structure (uit te breiden)
```javascript
const state = {
    // Bestaande state...
    
    // Nieuwe Schrijf Assistent state
    writer: {
        method: 'savethecat', // savethecat, storycircle, 3act, herosjourney, sequence, minimovie
        genre: 'thriller',
        logline: '',
        beats: {}, // Per methode, per beat: { content, suggestions, selectedSuggestion }
        currentBeat: 0,
        project: {
            title: '',
            characters: [],
            locations: [],
            themes: []
        }
    },
    
    // Meesters database (hardcoded)
    masters: [...] // 100 schrijvers met hun data
};
```

### API Calls
- Zelfde Cloudflare Worker als Acting Tool
- Model: claude-sonnet-4-20250514
- Rate limiting: 2.5 seconde delay tussen calls

---

## 📁 Bestanden

### Huidige Bestanden
1. `scriptmaster-pro.html` - Hoofd applicatie (1880 regels)
2. `manifest.json` - PWA manifest
3. `sw.js` - Service worker

### Te Maken
1. Uitbreiding van `scriptmaster-pro.html` met Schrijf Assistent sectie
2. Dit documentatiebestand voor continuïteit

---

## 🚀 Volgende Stappen

### ✅ VOLTOOID (11 januari 2026)
1. [x] Nieuwe tab "Schrijf Assistent" met 6 subtabs
2. [x] Beat Planner met 6 methodes + progress indicator
3. [x] AI integratie voor suggesties (3 opties: conventioneel, verrassend, gedurfd)
4. [x] 100 schrijvers database met filtering + detail modal
5. [x] "Pas stijl toe" integratie met Chat
6. [x] Scene Builder met volledige scene generatie
7. [x] Dialogue Generator met 3 versies
8. [x] Conflict Escalator met 5 niveaus
9. [x] Plot Twist Generator met 5 categorieën
10. [x] Export functionaliteit (TXT, JSON, Fountain)
11. [x] Copy-to-clipboard functionaliteit
12. [x] UI verbeteringen en polish

### Mogelijke Toekomstige Uitbreidingen
1. [ ] Character Arc Builder - volg karakter ontwikkeling per beat
2. [ ] Theme Tracker - houd thema's bij door het script
3. [ ] Outline to Script - genereer volledige scripts uit beats
4. [ ] Collaboration features - delen met andere schrijvers
5. [ ] Version history - track wijzigingen over tijd
6. [ ] Import bestaande scripts voor analyse

---

## 📝 Notities voor Volgende Chat

Bij het starten van een nieuwe chat:

1. Upload dit document
2. Zeg: "Ik wil verder werken aan ScriptMaster Pro, hier is de documentatie"
3. Claude leest het document en kan direct verder bouwen

**Huidige Status:** 
- ✅ ALLE 8 secties zijn gebouwd en volledig functioneel
- ✅ Schrijf Assistent met 6 tools volledig geïmplementeerd
- ✅ 100 schrijvers database volledig gevuld
- ✅ Export functionaliteit werkend

**Cloudflare Worker:** `actingtool.ferencsomogyi.workers.dev` (al werkend)
**GitHub Repo:** `scriptmaster-pro` (nog aan te maken)
**URL na deploy:** `ferrisomogyi.github.io/scriptmaster-pro`

### Huidige Bestanden
1. `scriptmaster-pro.html` - Hoofd applicatie (~4100 regels)
2. `manifest.json` - PWA manifest
3. `sw.js` - Service worker

---

*Laatst bijgewerkt: 11 januari 2026*
*Versie: 2.0 - Volledige Schrijf Assistent*
