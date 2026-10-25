# LEDINEK coach – Android

Intervalni timer (Get ready / Workout / Rest). Zaslon ostane prižgan, dokler je aplikacija odprta (FLAG_KEEP_SCREEN_ON), sistemske vrstice so skrite.

## Gradnja APK (Android Studio)
1. Odpri Android Studio → **Open** → izberi mapo `LedinekCoach`.
2. Počakaj, da se Gradle sinhronizira (prvič nekaj minut, potrebuje internet).
3. Meni **Build → Build App Bundle(s) / APK(s) → Build APK(s)**.
4. APK najdeš v `app/build/outputs/apk/debug/app-debug.apk` (povezava »locate« se pojavi v spodnjem desnem kotu).

## Namestitev na telefon
- Pošlji `app-debug.apk` (WhatsApp, e-pošta, Drive).
- Na telefonu ga odpri in dovoli »Namesti neznane aplikacije« za aplikacijo, iz katere ga odpiraš.

## Spremembe
- Videz in logika: `app/src/main/assets/index.html`
- Ime aplikacije: `app/src/main/AndroidManifest.xml` (android:label)
- Ikona: `app/src/main/res/drawable/ic_launcher_fg.xml` (ali v Android Studiu: desni klik `res` → New → Image Asset in izberi logo LEDINEK)

Opomba: pisave se naložijo z interneta; brez povezave aplikacija uporabi sistemsko pisavo, timer deluje normalno.

## Gradnja brez računalnika (GitHub)
Ob vsakem pushu na `main` GitHub Actions zgradi APK in ga objavi pod **Releases → latest** kot `LEDINEK-coach.apk`. Povezava za prenos:
`https://github.com/<uporabnik>/<repo>/releases/latest/download/LEDINEK-coach.apk`
