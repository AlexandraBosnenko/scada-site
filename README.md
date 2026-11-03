# Інтерактивна мнемосхема сонячної електростанції (СЕС) 5 кВт

🔗 **Відкрити сайт:** https://valeriiasukhomlyn.github.io/scada-site/

🇬🇧 [English version below](#english-version)

## Що це
Навчальний веб-тренажер. Він показує, як працює невелика сонячна електростанція, на схемі у стилі SCADA/АСУ ТП. Відкривається в браузері за посиланням, нічого встановлювати не потрібно.

На схемі показано:
- 15 фотомодулів по 500 Вт;
- роз’єднувач із запобіжниками QSdc5 та захист від перенапруг (ОПН/ПЗІП) на стороні постійного струму (DC);
- інвертор 5 кВт;
- акумуляторну батарею (АКБ / BESS);
- розподільний щит РЩ-СЕС з автоматом SF1 та ОПН на стороні змінного струму (AC);
- будівлю як споживача та шину заземлення PE.

## Для чого це потрібно студентам
- Зрозуміти, як енергія проходить від сонячних панелей через інвертор до споживача та в батарею.
- Побачити, як стан кожного елемента впливає на всю систему.
- Безпечно експериментувати: нічого не зламається, будь-яку дію можна скасувати.
- Виконувати невеликі дослідження й зберігати результати у текстовий файл.

## Що можна робити на схемі
- Вмикати та вимикати окремі панелі або всі одразу.
- Перемикати сезон (літо / зима) і бачити, як змінюються інсоляція та вироблення.
- Відключати зовнішню мережу, щоб змоделювати аварію (блекаут).
- Замикати й розмикати QSdc5 та автомат SF1, змінювати номінали захисту.
- Налаштовувати інвертор: кількість фаз, тип схеми, потужність.
- Змінювати рівень заряду, тип і режим роботи батареї.
- Змінювати навантаження будівлі (літнє й зимове) та кабель.
- Симулювати удар блискавки й побачити, як спрацьовують ОПН, а потім замінити їх.
- Дивитися живі показники: потужність і напругу, осцилограму AC, графік інсоляції.

## Ролі
| | Користувач (студент) | Адміністратор (викладач) |
|---|---|---|
| Керування схемою | так | так |
| Вивантаження в `.txt` | лише власні дії | дії всіх користувачів |
| Список тих, хто зараз на сайті | ні | так |
| Очищення журналу на екрані | ні | так |

## Як користуватися
1. Відкрийте посилання на сайт.
2. Введіть своє ім’я та натисніть «Увійти». Викладач обирає роль адміністратора та вводить пароль.
3. Натискайте на елементи схеми та змінюйте параметри.
4. Усі ваші дії записуються в журнал внизу сторінки.
5. Натисніть «⬇ Вивантажити дані (.txt)». У файлі буде журнал дій і стан схеми на цей момент. Його можна додати до звіту.

## Важливо знати
- Це навчальна модель, а не точний розрахунок реальної станції. Значення (наприклад, ККД інвертора й вироблення панелей) спрощені.
- Ваше ім’я та дії зберігаються в спільному журналі, який бачить викладач.
- У полі імені не вказуйте особисті дані, окрім потрібних для навчання.

## Технічно
Сайт — одна HTML-сторінка (HTML, CSS, JavaScript), розміщена на GitHub Pages. Спільний журнал і список користувачів онлайн зберігаються в Firebase Realtime Database.

Файли:
- `index.html` — сайт;
- `config.js` — пароль адміністратора (SHA-256) і адреса бази Firebase.

---

# English version

## Interactive Solar Power Plant (SPP) 5 kW SCADA Mimic Diagram

🔗 **Open the site:** https://valeriiasukhomlyn.github.io/scada-site/

### What it is
A web-based educational simulator. It shows how a small solar power plant works, using a SCADA/industrial-automation style diagram. It opens in any browser through a link, with nothing to install.

The diagram shows 15 PV panels (500 W each), the QSdc5 fuse-disconnector and DC-side surge protection, a 5 kW inverter, a battery energy storage unit (BESS), the AC switchboard with breaker SF1 and AC-side surge protection, a building as the load, and the PE grounding bus.

### What it is for (students)
- Understand how energy flows from solar panels through the inverter to the load and the battery.
- See how the state of each component affects the whole system.
- Experiment safely: nothing can break, and every action can be undone.
- Run small research tasks and save the results to a text file.

### What you can do
- Switch panels on and off, change the season (summer / winter), and disconnect the external grid to simulate a blackout.
- Open and close QSdc5 and SF1, and change protection ratings.
- Configure the inverter, the battery (charge, type, mode), the building load and the cable.
- Simulate a lightning strike and watch the surge protectors operate.
- Watch live readings: power, voltage, the AC oscilloscope and the irradiance chart.

### User roles
| | User (student) | Administrator (teacher) |
|---|---|---|
| Control the diagram | yes | yes |
| Export to `.txt` | own actions only | actions of all users |
| See who is currently on the site | no | yes |
| Clear the on-screen log | no | yes |

### How to use it
1. Open the site link.
2. Enter your name and log in. The teacher selects the administrator role and enters the password.
3. Click any element on the diagram and change its parameters. All actions are recorded in the event log.
4. Click "Export data (.txt)". The file contains your action log and the state of the diagram, and can be attached to a report.

### Please note
- This is an educational model, not an exact calculation of a real plant. Values are simplified.
- Your name and actions are saved in a shared log that the teacher can see. Do not enter personal data in the name field beyond what your course needs.

### Technical notes
A single HTML page (HTML, CSS, JavaScript) hosted on GitHub Pages. The shared log and online-user list are stored in Firebase Realtime Database. The interface is in Ukrainian.
