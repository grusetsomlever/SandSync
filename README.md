# 📊 SandSync Mod - Kommandoguide

Välkommen till SandSync-wikin! Alla kommandon börjar med `/sandsync`. Modden har fullt stöd för **Tab-Completion**, vilket innebär att du kan trycka på `Tab`-tangenten för att automatiskt fylla i kommandona.

### 🔑 Kom igång
För att kunna spara och ladda ner stats måste du koppla din identitet till en hemlig PIN-kod. Detta krypterar din data så att ingen annan kan skriva över dina framsteg!

* **`/sandsync pin <din_pinkod>`**
  * **Beskrivning:** Sparar din hemliga pinkod. Du behöver bara göra detta en gång. När koden är satt gör modden automatiskt en "force sync" för att spara dina nuvarande stats till molnet. *Notera: Du kan inte byta PIN-kod när den väl är satt!*
  * **Exempel:** `/sandsync pin MinHemligaKod123`

---

### 📝 Vilka stats kan jag spåra?
Du kan spåra all anpassad statistik ("Custom Statistics") som Minecraft mäter i bakgrunden! För att hitta namnet på en specifik stat kan du kika på **[Minecraft Wiki - Statistics](https://minecraft.wiki/w/Statistics#List_of_custom_statistic_names)** under rubriken *"List of custom statistic names"*.

**Viktigt:** Du behöver **inte** skriva `minecraft:` framför namnet. 
* Om wikin säger `minecraft:animals_bred`, skriver du bara `animals_bred`.
* Om wikin säger `minecraft:play_time`, skriver du bara `play_time`.
* Om wikin säger `minecraft:damage_dealt`, skriver du bara `damage_dealt`.

Dessa namn använder du sedan när du söker efter topplistor eller ändrar din HUD!

---

### 🔄 Synkning & Uppdatering
Modden synkar automatiskt i bakgrunden (baserat på din `syncinterval`), men du kan när som helst tvinga fram en uppdatering manuellt.

* **`/sandsync sync`**
  * **Beskrivning:** Tvingar modden att hämta dina allra senaste stats från servern och ladda upp dem till molnet.
* **`/sandsync fetch`**
  * **Beskrivning:** Tvingar modden att ladda ner den senaste topplistan från molnet så att din HUD och sökningar är helt uppdaterade.

---

### 💬 Databas & Sökning (Chatt)
Vill du kolla vem som leder i en viss kategori utan att ändra din HUD? Använd dessa chatt-kommandon!

* **`/sandsync top <stat_name>`**
  * **Beskrivning:** Visar topp 5-spelarna för en specifik stat direkt i din chatt.
  * **Exempel:** `/sandsync top animals_bred`
* **`/sandsync search <spelarnamn>`**
  * **Beskrivning:** Sök på en specifik spelare för att se en snabb sammanfattning av deras stats (t.ex. speltid och dödsfall).
  * **Exempel:** `/sandsync search Notch`

---

### ⚙️ Inställningar (Settings)
Här kan du skräddarsy exakt hur SandSync ska se ut och bete sig på din skärm. Alla inställningar sparas automatiskt i din config-fil.

**HUD & Utseende:**
* **`/sandsync settings hud <show | hide>`**
  * **Beskrivning:** Visar eller döljer topplistan (HUD) på skärmen helt och hållet.
* **`/sandsync settings leaderboard stat <stat_name>`**
  * **Beskrivning:** Väljer vilken statistik som ska visas på skärmen.
  * **Exempel:** `/sandsync settings leaderboard stat deaths`
* **`/sandsync settings leaderboard background <show | hide>`**
  * **Beskrivning:** Slår av eller på den mörka rutan bakom texten på topplistan.
* **`/sandsync settings leaderboard opacity <1-100>`**
  * **Beskrivning:** Ändrar hur genomskinlig bakgrunden ska vara. `100` är helt svart, `20` är väldigt transparent.
  * **Exempel:** `/sandsync settings leaderboard opacity 50`

**Format & Beteende:**
* **`/sandsync settings tickformat <auto | minutes | hours | days>`**
  * **Beskrivning:** Bestämmer hur tidsbaserad statistik (som speltid) ska formateras. `Auto` skalar dynamiskt upp tiden (t.ex. från minuter till timmar när numret blir tillräckligt stort).
* **`/sandsync settings syncinterval <5-60>`**
  * **Beskrivning:** Bestämmer hur ofta (i minuter) modden automatiskt ska ladda upp dina stats till molnet. Standard är oftast 5 minuter.
  * **Exempel:** `/sandsync settings syncinterval 10`
* **`/sandsync settings messages <show | hide>`**
  * **Beskrivning:** Döljer eller visar meddelandena i chatten när modden gör en automatisk synkning i bakgrunden. Perfekt att dölja om du vill ha en ren chatt!

---

> **💡 Tips:** Eftersom SandSync krypterar serveradressen är alla topplistor helt unika för den server du spelar på. Modden går in i "viloläge" om du spelar Singleplayer, för att spara prestanda och inte ladda upp offline-data i onödan.
