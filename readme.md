# Ez egy Markdown file
Itt jó dolgokat lehet csinálni int például
|táblázatok|valami ilyesmi|
|---|---|
|headerek|azt már használtam|
|---|---|
|kéne egy jegyzetet írnom|de a nincs kedvem|

itt van 3 ok hogy miért nincs kedvem:
- Háradt vagyok
  - De nagyon
- Éhes vagyok már
  - De kalyakra
- Szimplán nincs kedvem



### Mr. AI:

# 🎨 CSS utasítások részletes összefoglalása

## 📁 `index.css`

### Általános elrendezés (`article`, `.cikk`)
- **Rácsalapú elrendezés**: Az `article` és `.cikk` elemek `grid` megjelenítést használnak, amely lehetővé teszi a tartalom rugalmas, többoszlopos elrendezését.
- **Automatikus oszlopszám**: A `repeat(auto-fit, minmax(...))` szerkezet automatikusan annyi oszlopot hoz létre, amennyi elfér, minimum 250px szélességgel.
- **Oszlop- és sorközök**: Az elemek között 20px távolság van vízszintesen és függőlegesen.
- **Cikk struktúra**: A `.cikk` három sorból áll: fejléc, tartalom, lábléc, ahol a középső rész rugalmasan kitölti a rendelkezésre álló helyet.

### Navigációs sáv (`nav`, `ul`, `li`, `a`)
- **Háttérszín**: A `nav` sötétszürke (`dimgray`) hátteret kap.
- **Lista elrendezése**: A `ul` elem is `grid` elrendezést használ, a menüpontokat automatikusan oszlopokba rendezi, középre igazítva.
- **Listaelemek (`li`)**: Középre igazított szöveg, sötétszürke háttérrel.
- **Linkek (`a`)**: Fehér színűek, aláhúzás nélkül.
- **Hover effekt**: Ha az egérrel egy menüpontra visszük a kurzort, annak háttérszíne barnára változik.

### Elem sorrend (`#n1`–`#n5`)
- **Rácsban való sorrendezés**: Az `order` tulajdonság segítségével meghatározható, hogy az egyes elemek milyen sorrendben jelenjenek meg a rácsban, függetlenül a HTML-ben elfoglalt helyüktől.

---

## 📁 `oldal1.css`

### Tartalomirány (`direction`)
- **Jobbról balra (`rtl`)**: Az `article` elem szövegirányát jobbról balra állítja, ami például arab vagy héber nyelvű tartalomhoz hasznos.
- **Balról jobbra (`ltr`)**: A `.cikk` osztály visszaállítja a szövegirányt balról jobbra, így a cikkek tartalma a megszokott módon jelenik meg.

### Igazítás
- **Középre rendezés**: Az `article` tartalma vízszintesen és függőlegesen is középre kerül, így esztétikusabb és szimmetrikusabb megjelenést biztosít.

### Kommentelt `order` szabályok
- **Inaktív sorrendezés**: Az `order` tulajdonságokat kikommentelték, így azok jelenleg nem befolyásolják az elemek megjelenési sorrendjét, de később könnyen aktiválhatók.

---

## 📁 `oldal2.css`

### Grid területek (`main`, `grid-template-areas`)
- **Oldalszerkezet kialakítása**: A `main` elem egy előre definiált rácsot használ, amely külön területekre osztja az oldalt: fejléc (`header`), menü (`menu`), tartalom (`artical`), oldalsáv (`aside`), lábléc (`footer`).
- **Terület hozzárendelés**: Az egyes HTML elemek a `grid-area` segítségével kerülnek a megfelelő helyre a rácsban.

### Tartalom elrendezés (`article`, `.cikk`)
- **Rácsos `article`**: Hasonlóan az előző fájlokhoz, itt is automatikusan illeszkedő oszlopokat használ, de kiegészül azzal, hogy az `article` a `grid-area: artical` területre kerül.
- **Szöveg igazítása**: Az `align-items: first baseline` beállítás biztosítja, hogy a tartalom az első szövegsor alapvonalához igazodjon, ami esztétikusabb szövegigazítást eredményez.
- **Cikkek (`.cikk`)**: Három soros rácsot használ, és a magassága 100%-ra van állítva, így kitölti a rendelkezésre álló helyet.
- **Elem sorrend (`.cikk div`)**: A `div` elemek `order: -1` beállítással előre kerülnek a megjelenési sorrendben, még akkor is, ha a HTML-ben később szerepelnek.

