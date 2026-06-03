# 🐾 Tamagochi

Laipni lūdzam **Tamagochi** — pārlūkprogrammas virtuālā mājdzīvnieka un klikšķeru spēlē! Tavs uzdevums ir rūpēties par savu kaķi, uzturēt tā statistiku labā līmenī un pelnīt monētas, lai attīstītu un uzlabotu aprūpes lietas, kļūstot par īstu mājdzīvnieku magnātu.

---

## 🎮 Spēles noteikumi un mērķis

Galvenais spēles mērķis ir **uzturēt mājdzīvnieku dzīvu**, vienlaikus **krājot monētas** un pērkot labākos uzlabojumus.

* **Trīs labklājības joslas:** Kaķim ir trīs galvenie rādītāji: **Prieks (Happiness)**, **Enerģija (Energy)** un **Izsalkums (Hunger)**. Spēles sākumā tie visi ir 100%.
* **Monētu pelnīšana:** Katru reizi, kad ar savu klikšķi uzpildi kādu no rādītāju joslām līdz taisni 100%, tu saņem monētu izmaksu (payout).
* **Dinamiskais domu burbulis:** Ja kāda no joslām nokrītas **zem 40%**, virs mājdzīvnieka parādīsies peldošs mākonītis, kurā iekšā animēti tiks rādīts tieši tas GIF attēls, kuru pusi viņš šobrīd visvairāk vēlas (ēdienu, miegu vai mantas).
* **Zaudēšanas nosacījums (Nāve):** Ja nepieskatīsi dzīvnieku un visas trīs joslas vienlaicīgi sasniegs 0%, spēle būs zaudēta. Kaķa attēls automātiski pārvērtīsies par kapa pieminekli (RIP), darbības tiks iesaldētas un spēle apstāsies.

---

## ⚙️ Spēles loģika un mehānikas

### 1. Pasīvais joslu kritums (Drenāža)
Pat tad, ja tu neklikšķini pogas, Tamagochi rādītāji laika gaitā dabiski samazinās. Katrai joslai ir pielāgots savs krituma ātrums komfortablai spēlēšanai:

| Rādītājs | Cik bieži samazinās? | Cik daudz nokrīt? |
| :--- | :--- | :--- |
| **🧸 Prieks** | Ik pēc 5 sekundēm | -5% |
| **🛏️ Enerģija** | Ik pēc 8 sekundēm | -5% |
| **🍲 Izsalkums** | Ik pēc 10 sekundēm | -5% |

### 2. Spama aizsardzība (Cooldown)
Lai spēlētājs nevarētu vienkārši bezgalīgi un pārlieku ātri klikšķināt pogas, rotaļlietām un gultai ir iestrādāta klikšķu bremze:
* Izdarot **3 ātrus klikšķus** pēc kārtas uz Rotaļlietas vai Gultas ikonas, poga uz brīdi nodziest un ieslēdzas **5 sekunžu dīkstāve (cooldown)**. Šajā laikā pogu nospiest nevar.

### 3. Sākuma ekonomika
* **Darbību cenas:** Spēlēties un Gulēt ir pilnīgi bez maksas. Tomēr ēdiens ir jāpērk! Sākumā katra barošana (Food) maksā tikai **1 monētu**.
* **Sākuma kapitāls:** Spēle vienmēr sākas ar 10 monētām tavā makā.

---

## 🛒 Uzlabojumu veikals (Shop Upgrades)

Sakrātās monētas var tērēt apakšējā veikalā, lai palielinātu Tamagochi aprūpes efektivitāti. Katrs nopirktais uzlabojums sniedz divus būtiskus bonusus:
1.  **+5% klikšķa jauda:** Attiecīgā progresjosla piepildīsies daudz ātrāk un ar mazāku klikšķu skaitu.
2.  **+2 monētas pie katras izmaksas:** Katru reizi, kad josla sasniedz 100%, tu saņemsi par 2 monētām vairāk nekā iepriekš (piemēram: Lvl 1 dod +1 monētu, Lvl 2 dod +3 monētas, Lvl 3 dod +5 monētas utt.). Tas veido galveno spēles peļņas pieaugumu.

> ⚠️ **Svarīgi par Ēdiena uzlabošanu:** Katru reizi, kad tu uzlabo ēdienu, palielinās tā sniegtā jauda un izmaksas peļņa, taču arī paša ēdiena cena (barošanas izmaksas darbību panelī) pieaug par **+1 monētu**.
> 
> **Uzlabojumu cenas:** Katru reizi, kad nopērc kādu veikala uzlabojumu, tā cena nākamajam līmenim **dubultojas** (5, 10, 20, 40 monētas utt.).

---

## 🛠️ Tehniskais izpildījums
Projekts ir izstrādāts, izmantojot tīras un vieglas tīmekļa tehnoloģijas:
* **HTML5** – spēles struktūrai, elementu izvietojumam un konteineriem.
* **CSS3** – dizainam, peldošā mākoņa animācijām (`@keyframes float`) un vizuālajiem cooldown efektiem.
* **Vanilla JavaScript** – spēles laika cilpām (`setInterval`), loģikas aprēķiniem un mājdzīvnieka stāvokļa kontrolelei.