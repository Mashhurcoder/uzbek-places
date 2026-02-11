
<img width="200" height="400" alt="image" src="https://github.com/user-attachments/assets/8d7e0758-a5ea-453b-8f30-8b60d3951d25" />
<img width="200" height="400" alt="image" src="https://github.com/user-attachments/assets/08f43c44-532e-4121-9ecc-f9972a67fbae" />
<img width="200" height="400" alt="image" src="https://github.com/user-attachments/assets/f2950f79-e249-433e-90c3-d0f6581f99b6" />


# 📍 Uzbek Places App - Flutter (MVVM Architecture)

Ushbu ilova O'zbekistonning diqqatga sazovor joylarini o'rganish uchun mo'ljallangan bo'lib, eng zamonaviy arxitektura tamoyillari asosida qurilgan. Loyihada kodning tozaligi (Clean Code) va kengayuvchanligi (Scalability) uchun **MVVM** patternidan foydalanilgan.

## 🏗 Arxitektura: MVVM + BLoC

Loyihaning asosi **MVVM (Model-View-ViewModel)** patterniga qurilgan bo'lib, u quyidagi qismlardan iborat:

* **Model:** Ma'lumotlar tuzilmasi va SQLite bazasi bilan ishlash (`sqflite`).
* **View:** Foydalanuvchi interfeysi (UI), faqat BLoC holatlarini (states) kuzatadi.
* **ViewModel (BLoC):** Biznes mantiq qismi. View'dan kelgan hodisalarni (events) qabul qiladi va Model orqali ma'lumotlarni yangilab, UI'ga yangi holatni qaytaradi.



---

## ✨ Texnik Imkoniyatlar

* **🚀 BLoC State Management:** Ilovaning har bir qismi (Kategoriyalar, Sevimlilar, Qidiruv) alohida BLoC oqimlari orqali boshqariladi.
* **💾 SQLite Integration:** Foydalanuvchi tanlagan maskanlar lokal bazada saqlanadi, bu esa oflayn rejimda ham foydalanish imkonini beradi.
* **🎨 Dynamic UI:** * **Splash Screen:** Kirish qismida harflarning kattalashib-kichrayishi (Scaling Animation).
    * **Sliver Widgets:** `SliverAppBar` va `SliverList` orqali silliq va interaktiv skroll effektlari.
    * **Custom Design:** Material 3 va Dark/Light rejimiga mos ranglar palitrasi.
* **📂 Data Handling:** `popularDestinations` va `allDestinations` massivlari orqali ma'lumotlarni dinamik filtrlash.

---

## 🛠 Ishlatilgan Kutubxonalar (Dependencies)

```yaml

dependencies:
  flutter:
    sdk: flutter
  flutter_bloc: ^8.1.0  # State management uchun
  sqflite: ^2.3.0       # Lokal baza uchun
  path: ^1.8.3          # Fayl yo'llari uchun
  flutter_spinkit: ^5.2.0 # Yuklanish animatsiyalari uchun
  lib/
 ├── core/              # Ranglar, mavzular va doimiy o'zgaruvchilar
 ├── data/
 │    ├── models/       # DestinationModel class
 │    └── database/     # SQLite DatabaseHelper
 ├── logic/             # BLoC (Events, States, Blocs)
 └── presentation/      # UI qismi
      ├── screens/      # Splash, Home, Detail sahifalari
      └── widgets/      # Qayta ishlatiluvchi UI komponentlar
