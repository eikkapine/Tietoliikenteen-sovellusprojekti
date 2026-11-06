# ble_kiihtyvyysanturi

Viikon 2 tehtävä 1.1.3: kiihtyvyysanturin ADC-ohjelma ja BLE-ohjelma yhdistettynä.

Pohjana:
- Nordic Academy, Bluetooth Low Energy Fundamentals, Lesson 4 Exercise 2 (`my_lbs.c`, `my_lbs.h`)
- [TL_Project_Week2](https://github.com/kajyrkka/TL_Project_Week2), Working_ADC_Solution (`adc.c`, `adc.h`)

## Toiminta

- Laite mainostaa nimellä `MY_LBS2` (Nordicin harjoituksen oletusnimi).
- Kun notifikaatiot on tilattu (nRF Connect -sovellus), laite lähettää puolen sekunnin välein yhden mittauksen.
- Nappi 2 vaihtaa suuntaa 0 -> 1 -> 2 -> 3 -> 4 -> 5 -> 0.
- Nappi 3 tekee 100 mittausta valitusta suunnasta ja lähettää ne (10 ms välein).

Suunnat: 0 = X alas, 1 = X ylös, 2 = Y alas, 3 = Y ylös, 4 = Z alas, 5 = Z ylös.

Yksi mittaus lähetetään neljänä notifikaationa Karin ohjeen mukaan (`my_lbs_send_sensor_notify()` neljä kertaa): suunta, x, y, z. Jokainen arvo on uint32 (little endian). X, Y ja Z ovat millivoltteja.
Arvot tulevat LBS-palvelun MYSENSOR-ominaisuuteen (UUID `00001526-1212-efde-1523-785feabcd123`).

## Kytkentä

| Signaali | Pinni |
|----------|-------|
| X | P0.04 |
| Y | P0.05 |
| Z | P0.06 |

ADC:n kanavat on määritelty tiedostossa `nrf5340dk_nrf5340_cpuapp.overlay` (Karin overlay-tiedosto).

## Kääntäminen

nRF Connect SDK v3.0.2, board `nrf5340dk/nrf5340/cpuapp`.

Tila: testattu omalla laudalla. Data tulee nRF Connect -sovellukseen ja tietokoneelle, napit 2 ja 3 toimivat.
