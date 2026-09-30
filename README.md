# LKS-92 → LKS-2020 DGN — izlaidumi un atjauninājumi

Šeit tiek publicētas programmas **LKS-92 to LKS-2020** (DGN pārrēķins MicroStation /
PowerSurvey V8i vidē ar LĢIA NTv2 virsmu) gatavās versijas. Pirmkods šeit nav.

© 2026 Aldis Pizāns. Visas tiesības aizsargātas. Skat. [LICENSE](LICENSE).

## Lejupielāde

**Releases → Latest → `LKS-92_uz_LKS-2020_v<versija>.zip`.** Izpakojiet un palaidiet
`LKS-92_to_LKS-2020.exe`; pamācība (PDF) ir ZIP iekšā.

Programmai **nepieciešama licence** — bez tās tā nepārrēķina. Licenci izsniedz autors:
aldis@surveying.lv.

## Automātiskā atjauninājumu pārbaude

Programma (no versijas 1.7.0) reizi diennaktī fonā pārbauda šo vietu. Ja ir jaunāka
versija, logā parādās rinda „ATJAUNINĀJUMS …” un poga „Lejupielādēt atjauninājumu”.
Bez interneta pārbaude klusi izlaižama un darbu neaizkavē.

Katram izlaidumam ir trīs faili:

| Fails | Nozīme |
|---|---|
| `LKS-92_uz_LKS-2020_v<versija>.zip` | programma |
| `manifest.json` | versija, ZIP adrese, izmērs, SHA-256 |
| `manifest.json.sig` | autora Ed25519 paraksts manifestam |

Programma lejupielādēto ZIP pieņem tikai tad, ja manifesta paraksts ir derīgs (autora
atslēga ir iebūvēta programmā), ZIP izmērs un SHA-256 sakrīt ar manifestu un ZIP ir
vesels. Tāpēc šī vieta pati par sevi nav jāuzskata par uzticamu: izmainītu vai svešu
failu programma noraida.

Programma sevi **nenomaina**: pārbaudītais ZIP tiek saglabāts programmas mapē
`Atjauninajumi\`. Aizveriet programmu, izpakojiet ZIP un aizstājiet programmas failus;
`Config`, `Seed` un `grids` mapes, ja tajās ir jūsu izmaiņas, saglabājiet.

## Autoram

Izlaidumus šeit izveido privātā repozitorija darbplūsma „Windows programma” (izlaidums
`v<versija>`) — tā pati būve, testi un paraksts; ar roku nekas nav jāaugšupielādē.
Nepieciešams noslēpums `ATJAUNINAJUMI_TOKEN` privātajā repozitorijā (skat. tā README).

* Tagam jāsakrīt ar versiju (`v1.7.0`); izlaidumu neatzīmēt kā *pre-release* — adrese
  `releases/latest/download/manifest.json` ņem tikai pēdējo pilno izlaidumu.
* Atsaukt versiju: izdzēsiet izlaidumu — `latest` atgriežas pie iepriekšējā. Klienti,
  kas jau ieraudzījuši jaunāku manifestu, vecāku par to nepieņem (aizsardzība pret
  atkārtotu veca manifesta piespēlēšanu), tāpēc labojumu izlaidiet kā jaunu versiju.
