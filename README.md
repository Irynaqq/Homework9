Refactoring “Simple Site” with SCSS

Проєкт виконано в рамках задачі з рефакторингу існуючого CSS-коду на розширений стиль SCSS.
Мета — підвищити ефективність, читабельність та підтримуваність стилів, застосувавши модульну структуру, змінні, міксіни та медіа-міксіни.

🎯 Основні завдання рефакторингу
✔ 1. Перехід з CSS на SCSS

Усі стилі перенесено у SCSS-файли з подальшою компіляцією у css/style.css.

✔ 2. Декомпозиція коду

Проєкт поділено на логічні модулі:

  scss/
  utils/        – змінні, міксіни, медіа-міксіни
  base/         – базові стилі (reset, typography)
  layout/       – контейнер, шапка, футер
  components/   – компоненти (hero, navbar, experience, video, section)
  main.scss     – точка входу (@use)

✔ 3. Використання SCSS-змінних

У файлі _variables.scss винесено:

кольори

типографіку

відступи (gap)

ширини контейнерів

line-height та font-weight

✔ 4. Використання міксінів

Файл _mixins.scss містить:

flex-center

button-primary

visually-hidden

✔ 5. Медіа-міксіни

Файл _media.scss:

@mixin mobile

@mixin tablet

@mixin desktop

✔ 6. Вкладеність селекторів

Стилі переписано з використанням вкладеності для підвищення читабельності.
🚀 Компіляція SCSS → CSS
sass scss/main.scss css/style.css --watch
Після цього усі зміни у SCSS автоматично потрапляють у css/style.css.