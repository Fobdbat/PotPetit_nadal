# Tió de Nadal! · El joc d'El Pot Petit

Joc musical de navegador per a infants, al ritme de la cançó **«Tió de Nadal»** d'El Pot Petit.

**Juga:** https://tio-pot-petit.pages.dev/ (nom de projecte proposat a Cloudflare Pages)

## Com es juga
- Abans de començar, l'infant tria quin dels dos cantants recull els regals. L'altre canta amb la Melmelada Band.
- El Tió bota al ritme de la música i caga torrons, regals i caganers per 3 carrils.
- Es recullen amb la cistella. Les arengades pudents resten un punt: per esquivar-les, canvia de carril o toca **la banda** per amagar-t'hi.
- Toca l'**estació** d'un carril per moure't.
- Cada 25 regals es desbloqueja un vers tradicional del Tió (n'hi ha 4). Surt uns segons sense aturar el joc, i al final de la partida es poden llegir tots.
- La lletra de la cançó surt a la píndola de sota el Tió, al ritme de la veu.
- Una cançó, una partida: el joc s'acaba quan s'acaba la cançó. A la pantalla final hi ha un enllaç a la cançó a YouTube.
- Teclat (pissarra digital): fletxes ← →, números 1–3, espai o ↓ per anar amb la banda, P per fer pausa.

## Fitxers
| Fitxer | Què és |
|---|---|
| `index.html` | El joc sencer (gràfics, lògica i so) |
| `tio-de-nadal-pot-petit.mp3` | La cançó |
| `portada.png` | Imatge de vista prèvia quan es comparteix l'enllaç (1200×630) |

## Sincronia amb la cançó
126 BPM (temps 0 a 0,288 s). Introducció tranquil·la (temps 0–35), secció A (36–88), tornades amb patrons de 16 temps, aturades de la música als temps 136 i 220 (onada d'arengades: cal amagar-se a la banda) i pluja de regals final (270–279). Els valors són a l'inici del codi (`BEAT0`, `BEAT`, `FIRST_LAND`, `LAST_LAND`, `END_BEAT`).

La lletra surt en pantalla vers a vers, sincronitzada amb la veu (`LYRIC_LINES`: `[temps inici, temps final, text]`, en temps de 126 BPM). Per corregir un vers que entri tard o d'hora, canvia'n els dos números (1 temps = 0,476 s).

## Estadístiques
GoatCounter (tiopotpetit.goatcounter.com, site propi) compta les visites i aquests esdeveniments (prefix `tio-pot-petit/`):
- `partida-iniciada`, `partida-acabada` i `vers-1` … `vers-4` (quants infants arriben a cada vers).
- `cantant-ell` / `cantant-ella`: quin cantant trien per jugar.
- `clic-youtube`: clics a l'enllaç de la cançó a YouTube (pantalla final; s'obre en una pestanya nova).
- `partida-1`, `partida-2`, `partida-3`… : cada partida envia el seu número. **`partida-1` = gent que ha jugat**; **la suma de tots els `partida-N` = partides totals**. El comptador és només en memòria (no es guarda res al dispositiu).

## Mode de prova
`index.html?test&t=20` comença al segon 20, sense so. Afegeix `&auto` perquè jugui sol, o `&who=1` per jugar amb la cantant.

---
Cançó: «Tió de Nadal» © El Pot Petit · Joc: Europe Multimedia Service
