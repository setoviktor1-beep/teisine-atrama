# PATCH_PLAN_v1: Technical SEO Hardening

## 1. Problema: Canonical Tags (Duplicate Content Prevention)

- **Statusas:** Nėra.
- **Rizika:** Kadangi naudojame parametrinius URL kalboms (ateityje) arba tiesiog dėl saugumo, reikia nurodyti pagrindinį puslapį.
- **Fix:** Pridėti `<link rel="canonical" href="https://teisinėatrama.lt/" />`.

## 2. Problema: Favicon

- **Statusas:** Nėra.
- **Rizika:** Prastai atrodo paieškos rezultatuose (Google rodo ikonas) ir naršyklės tab'e.
- **Fix:** Pridėti favicon nuorodas (net jei failo dar nėra, reikia placeholder).

## 3. Problema: Heading Hierarchy (H1-H6)

- **Statusas:** Geras, bet reikia patikrinti ar nėra tuščių headingų.
- **Fix:** H1 yra. H2 yra. Struktūra atrodo tvarkinga.

## 4. Problema: Altributai Paveikslėliams

- **Statusas:** `profile-photo.jpg` turi alt tagą `Laura Seržintienė`, bet Hero fonas yra CSS.
- **Fix:** CSS background images nėra indeksuojami kaip paveikslėliai. Tai gerai dekoracijai. Profilio nuotraukos alt tagą galima praplėsti: `Laura Seržintienė - Antstolio padėjėja, Teisininkė`.

## 5. Problema: Multi-language SEO (Hreflang)

- **Statusas:** Viskas yra viename HTML faile ir keičiama per JS.
- **Kritinė Rizika:** Google robotai gali nematyti EN/PL/RU turinio, nes jis "paslėptas" JavaScript'e.
- **Sprendimas (Complex):** Idealiu atveju reiktų atskirų HTML failų (`/en/index.html`, `/pl/index.html`).
- **Sprendimas (Quick Fix):** Kol kas paliekame JS, bet pridedame `meta` keywords visomis kalbomis į pagrindinį failą, kad bent indeksuotųsi bendrai.

## 6. Veiksmai (Execution)

1. Pridėti `canonical`.
2. Atnaujinti `img alt`.
3. Pridėti `meta keywords` (nors Google jų nelabai žiūri, kitiems botams tinka).
4. Sutvarkyti `meta description` ilgį (optimalus 150-160 simbolių). Dabartinis: ~85. Galima išplėsti.
