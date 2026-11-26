# OMSE VR Remote

Telecomanda VR i-JMB K-207Z controleaza gimbalul DJI Osmo Mobile SE in fundal,
cat timp aplicatia Camera e deschisa pe tot ecranul.

## Cum obtii APK-ul (fara Android Studio)

1. Fa-ti cont pe github.com (gratuit) si creeaza un repository nou (New repository), public sau privat.
2. In repository: "uploading an existing file" -> trage TOT continutul acestui folder (dezarhivat).
   ATENTIE: folderul `.github` e ascuns pe unele sisteme. Daca nu apare dupa upload,
   creeaza-l manual: Add file -> Create new file -> nume `.github/workflows/build.yml`
   si lipeste continutul fisierului build.yml din arhiva.
3. Commit changes. Mergi la tab-ul "Actions": porneste automat "Build APK" (3-5 minute).
4. Cand apare bifa verde, deschide build-ul -> jos la "Artifacts" -> descarca `OMSE-VR-Remote-apk`.
   E un .zip cu `app-release.apk` inauntru.
5. Pune APK-ul pe telefon si instaleaza-l (permite "Instalare din surse necunoscute").

## Utilizare

1. Imperecheaza telecomanda K-207Z cu telefonul din setarile Bluetooth (ca la orice gamepad).
   Gimbalul NU se imperecheaza din setari - il conecteaza aplicatia.
2. Deschide aplicatia -> accepta permisiunile Bluetooth.
3. Butonul 2 -> Accesibilitate -> OMSE VR Remote -> Activeaza.
   (Pe Android 13+ daca e gri: Setari -> Aplicatii -> OMSE VR Remote -> meniu ⋮ -> "Permite setari restrictionate", apoi incearca iar.)
4. Butonul 1 -> se conecteaza la gimbal (porneste gimbalul inainte; inchide aplicatia DJI Mimo daca e conectata).
5. Misca joystick-ul: in "Ultima tasta VR" trebuie sa apara ceva gen DPAD_LEFT. Apoi deschide Camera.

## Mapare taste

| Telecomanda            | Actiune             |
|------------------------|---------------------|
| Joystick / D-Pad / WASD| Misca gimbalul      |
| A / OK / Enter         | Recenter            |
| B / X / Y              | Mod lent / normal   |

Daca "Ultima tasta VR" nu se schimba cand misti joystick-ul, telecomanda e intr-un mod
care trimite axe de joystick/mouse in loc de taste. Schimba modul de pe telecomanda
(combinatie de pornire cu @+A / @+B / @+C, depinde de varianta) pana apar taste DPAD.
