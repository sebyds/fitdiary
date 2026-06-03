<div align="center">

# 🫀 FitDiary

### Dieta & Allenamento — *Diet & Workout*

Diario personale di salute e fitness, completamente offline e privato.
*A fully offline, private health & fitness journal.*

[🇮🇹 Italiano](#-italiano) · [🇬🇧 English](#-english) · [Privacy IT](PRIVACY.it.md) · [Privacy EN](PRIVACY.en.md)

</div>

---

## 🇮🇹 Italiano

**FitDiary** è un diario tutto-in-uno per dieta e allenamento: traccia le calorie,
registra i workout, crea menù con lista della spesa automatica, segui i progressi
con le foto, monitora l'idratazione e (per chi lo desidera) il ciclo mestruale.
Tutto in un'unica app, semplice, in italiano e **completamente offline**.

### ✨ Funzioni

- **🍽️ Tracciamento alimentare** — pasti, orari e note; database di oltre 200
  alimenti italiani con calcolo automatico di calorie e macronutrienti; alimenti
  personalizzati.
- **📖 Menù e lista della spesa** — menù settimanali o mensili; la lista della
  spesa si genera automaticamente sommando gli ingredienti e raggruppandoli per
  categoria.
- **💪 Allenamenti e schede** — sessioni con esercizi, serie, ripetizioni, pesi e
  durata; schede personalizzate con libreria di esercizi illustrati.
- **📸 Progressi fotografici** — foto periodiche con confronto fianco a fianco.
- **🌸 Ciclo mestruale** — calendario con previsioni, finestra fertile,
  ovulazione e registrazione di flusso, umore e sintomi.
- **💧 Promemoria acqua** — obiettivo 2L con notifica "ricordati di bere".
- **📊 Dashboard giornaliera** — calorie, macro, allenamento, andamento
  settimanale, ciclo e idratazione a colpo d'occhio.
- **📲 Widget** per la schermata home con calorie e acqua del giorno.

### 🔒 Privacy

Nessun account, nessuna registrazione, nessuna connessione a internet. Tutti i
dati restano sul dispositivo. Vedi l'[Informativa sulla Privacy](PRIVACY.it.md).

### 🏗️ Architettura

L'interfaccia è una web-app **React** compilata in un singolo bundle e
incapsulata in una **WebView** nativa Android. La persistenza usa il layer nativo
(`SharedPreferences`) tramite un bridge JavaScript; notifiche in background via
`WorkManager`.

### 🚀 Build

> Requisiti: Android Studio (Hedgehog o più recente), JDK 17.

```bash
# 1. Clona la repository
git clone https://github.com/<utente>/fitdiary.git

# 2. Apri la cartella del progetto in Android Studio (File → Open)
#    seleziona la cartella che contiene settings.gradle

# 3. Attendi il Gradle Sync, poi:
#    - Run ▶ per installare su dispositivo/emulatore
#    - Build → Build APK(s) per l'APK
#    - Build → Generate Signed Bundle / APK per il .aab del Play Store
```

| Proprietà | Valore |
|-----------|--------|
| applicationId | `com.diariosalute.app` |
| minSdk | 24 (Android 7.0) |
| targetSdk | 34 (Android 14) |
| Linguaggio UI | Italiano |

### 📁 Struttura

```
app/
├─ src/main/
│  ├─ AndroidManifest.xml
│  ├─ java/com/diariosalute/app/
│  │  ├─ MainActivity.java        # host WebView + bridge + permessi
│  │  ├─ WaterReminderWorker.java # notifica acqua in background
│  │  └─ SummaryWidget.java       # widget schermata home
│  ├─ assets/web/                 # app React compilata (index.html + bundle.js)
│  └─ res/                        # icone, temi, layout widget, backup rules
```

### 📄 Licenza

[Scegli una licenza, es. MIT] — vedi il file `LICENSE`.

---

## 🇬🇧 English

**FitDiary** is an all-in-one diet & workout journal: track calories, log
workouts, build menus with an automatic shopping list, follow your progress with
photos, monitor hydration, and (optionally) your menstrual cycle. One app,
simple, and **fully offline**.

### ✨ Features

- **🍽️ Food tracking** — meals, times and notes; 200+ Italian foods with
  automatic calorie & macro calculation; custom foods.
- **📖 Menus & shopping list** — weekly or monthly menus; the shopping list is
  generated automatically by summing ingredients and grouping them by category.
- **💪 Workouts & plans** — sessions with exercises, sets, reps, weights and
  duration; custom plans with an illustrated exercise library.
- **📸 Progress photos** — periodic photos with side-by-side comparison.
- **🌸 Menstrual cycle** — calendar with predictions, fertile window, ovulation,
  and logging of flow, mood and symptoms.
- **💧 Water reminder** — 2L goal with a "drink water" notification.
- **📊 Daily dashboard** — calories, macros, workout, weekly trend, cycle and
  hydration at a glance.
- **📲 Home-screen widget** for today's calories and water.

### 🔒 Privacy

No account, no sign-up, no internet connection. All data stays on the device.
See the [Privacy Policy](PRIVACY.en.md).

### 🏗️ Architecture

The UI is a **React** web app compiled into a single bundle and wrapped in a
native Android **WebView**. Persistence uses the native layer
(`SharedPreferences`) through a JavaScript bridge; background notifications via
`WorkManager`.

### 🚀 Build

> Requirements: Android Studio (Hedgehog or newer), JDK 17.

```bash
# 1. Clone the repository
git clone https://github.com/<user>/fitdiary.git

# 2. Open the project folder in Android Studio (File → Open),
#    select the folder containing settings.gradle

# 3. After Gradle Sync:
#    - Run ▶ to install on a device/emulator
#    - Build → Build APK(s) for the APK
#    - Build → Generate Signed Bundle / APK for the Play Store .aab
```

### 📄 License

[Choose a license, e.g. MIT] — see the `LICENSE` file.

---

<div align="center">
<sub>FitDiary collects no data. Your health stays yours. · FitDiary non raccoglie dati. La tua salute resta una cosa tua.</sub>
</div>
