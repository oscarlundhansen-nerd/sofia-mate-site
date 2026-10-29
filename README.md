# Sofia Maté — sajten

Hela sajten består av `index.html` och mappen `images/`. Det finns ingen byggprocess.

## Lägga till en bild
1. Lägg bilden i `images/`. Använd jpg, ca 2000 px på långsidan, gärna redan beskuren till 4:5.
2. Öppna `index.html`, sök efter `const LIBRARY` och lägg en rad **överst** i listan:
   ```js
   {type:"editorial", title:"Publication: Photographer", src:"images/filnamn.jpg"},
   ```
   `type` är `"editorial"` eller `"commercial"`. Nyast överst.
3. Dra in hela mappen i Netlify, under fliken Deploys i projektet. Sajten är live direkt.

Rader utan `src` visar en tonad platshållare. Ta bort dem när de riktiga bilderna ligger inne.

## Första gången: lägga upp och koppla domänen
1. Logga in på netlify.com och välj Add new project → Deploy manually. Dra in mappen.
2. Under Domain management → Add a domain anger du Sofias domän.
3. Logga in på one.com och gå till DNS-inställningarna för domänen. Byt Cargos poster mot:
   - `@`: A-post → `75.2.60.5`
   - `www`: CNAME → projektets adress hos Netlify, till exempel `namn.netlify.app`
4. Rör inte MX-posterna, de styr mejlen.
5. Ändringen kan ta upp till ett dygn att slå igenom. Netlify ordnar HTTPS automatiskt när domänen pekar rätt.
6. När sajten är live via domänen kan du säga upp Cargo.
