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

Tila: testattu omalla laudalla. Pinnit P0.04, P0.05 ja P0.06 testattu kytkemällä ne VDD:hen (n. 2980 mV) ja GND:hen (0 mV). Anturilla vaakatasossa Z on suurin.

## ble_kiihtyvyysanturi

Kiihtyvyysanturin data BLE:n yli (viikko 2). Nappi 2 vaihtaa suuntaa, nappi 3 tekee 100 mittausta. Tarkemmin kansion README:ssä.

Tila: testattu omalla laudalla. Data tulee nRF Connect -sovellukseen ja tietokoneelle, napit 2 ja 3 toimivat.
