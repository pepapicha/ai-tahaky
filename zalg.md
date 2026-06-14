# Souhrnné hodnocení – PeeWee Rover Light (2025/2026)

## Pořadí

| Pořadí | Skupina | Body / 990 | Procenta | Hodnocení (jedna věta) |
|:------:|:-------:|:----------:|:--------:|------------------------|
| 1. | **M** | 727 | 73,4 % | Nejvyspělejší plynulé řízení a dekompozice; chybí kód breakdance, k vysvětlení složitost. |
| 2. | **C** | 674 | 68,1 % | Nejlepší packovaný protokol a joystickové řízení; AI poctivě přiznáno. |
| 3. | **H** | 648 | 65,5 % | Packovaný datagram a skvělá dokumentace; chybí breakdance, AI. |
| 4. | **B** | 609 | 61,5 % | Nejlepší breakdance (hudba, figury); kazí logická chyba v ověření a tank řízení. |
| 5. | **S** | 534 | 53,9 % | Proporcionální řízení; zbytkový `main.py`, 8 LED, chybí breakdance. |
| 6. | **E** | 499 | 50,4 % | Pěkný breakdance-automat; není to MakeCode projekt (volné soubory). |
| 7. | **K** | 493 | 49,8 % | Univerzální párování a `enum`; tank řízení, **rušení soupeřů** (etika). |
| 8. | **J** | 475 | 48,0 % | Náznak trimu a LED indikace; vyšší latence, breakdance jen video. |
| 9. | **A** | 466 | 47,1 % | Povedený dekomponovaný breakdance; slabá kvalita kódu a tank řízení přes stringy. |
| 10. | **T** | 452 | 45,7 % | Krásné parametrické figury, ale **celý breakdance zakomentován**. |
| 11. | **P** | 447 | 45,2 % | Čistý, jednoduchý; tank přes stringy, „tajný“ klíč, chybí breakdance. |
| 12. | **D** | 423 | 42,7 % | Striktní `===`; žádné LED, rozdělený datagram, chybná kompenzace. |
| 13. | **G** | 411 | 41,5 % | Hezky dekomponovaný breakdance; chyby API (hodnoty mimo rozsah, `wheelBreak` bez závorek). |

## Souhrnné poznámky napříč skupinami

- **Break Dance odevzdaný jako spustitelný kód:** A, B, E, G (a C/T s výhradami). **Chybí v repozitáři** u H, J, K, M (pouze video/dokumentace) a u T je **zakomentovaný**.
- **Plynulé „analogové" řízení:** nejlépe M, C, S, H. Většina ostatních používá tank/stupňové ovládání.
- **Packovaný datagram:** výborně C a H (vše v jednom), M naopak posílá 3 hodnoty zvlášť; D/T datagram tříští.
- **Ochrana komunikace sériovým číslem:** korektně M a C; H/J/K/P/S spoléhají na „obscurity" nebo nic. (Pozn.: B sériové číslo ověřuje, ale kvůli chybě priority operátorů je ochrana neúčinná.)
- **Časté chyby:** hodnoty `wheelSpeed` mimo rozsah −100..100 (G), příkaz `wheelBreak` bez závorek = no-op (G), volné `==` místo `===` (A, C, E, G).
