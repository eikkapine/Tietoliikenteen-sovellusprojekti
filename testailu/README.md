# Testailu

Kehitysalustan kokeilukoodit. Nämä pidetään omassa haarassaan, jotta keskeneräistä koodia ei päädy main-haaraan.

## kiihtyvyysanturi

Kiihtyvyysanturin lukeminen nRF5340 DK:n AD-muuntimella. Ohjelma tulostaa X-, Y- ja Z-arvot sarjaporttiin sekunnin välein. Pohjana on kurssin valmis esimerkki ([TL_Project_Week2](https://github.com/kajyrkka/TL_Project_Week2), Working_ADC_Solution).

Anturin kytkentä:

| Signaali | Pinni |
|----------|-------|
| X | P0.04 |
| Y | P0.05 |
| Z | P0.06 |

Käännetään VS Coden nRF Connect -laajennuksella, board `nrf5340dk/nrf5340/cpuapp/ns`.

Tila: ei vielä testattu omalla laudalla.
