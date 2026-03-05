# Ano

[English](#english) | [Русский](#русский)

---

## English

Ano is a lightweight, modern AI Chat Client built specifically for **iPhone OS 3.0** and legacy iOS devices. Developed by **AnotherLabs**, Ano breathes new life into classic hardware by connecting it to state-of-the-art AI models.

📣 **Join our Telegram Channel:** [@theopenriver](https://t.me/theopenriver)

### Features

- **Legacy Compatibility:** Runs flawlessly on iPhone OS 3.0+ (compiled for `armv6`).
- **Mistral AI Integration:** Powered by Mistral AI, acting as a smart, conversational assistant.
- **Chat History & Sessions:** Automatically saves your conversations locally so you never lose your chat history. Includes a convenient sidebar to switch between past sessions.
- **Dynamic Theming:** Full support for both **Light** and **Dark** themes, seamlessly integrated.
- **Localization:** Bilingual support for **English** and **Russian**.
- **Candy Chat Bubbles:** A beautiful, retro-modern UI with gradient chat bubbles tailored for the classic iPhone display.
- **Keyboard & UI Polish:** Smart keyboard dismissal, typing indicators ("AI is typing..."), and smooth animations.

### Architecture

Ano consists of two main components:
1. **The iOS Client (Objective-C):** A native UI built using traditional `UIKit` elements (`UITableView`, `UIButton`, CoreGraphics) optimized for memory and performance on older devices.
2. **The Backend Bridge (Python):** A lightweight Flask server that handles communication with the Mistral API and circumvents legacy SSL/TLS negotiation issues on old iOS versions.

### Prerequisites & Building

To build the iOS client, you will need a configured **Theos** environment with an `armv6` compatible toolchain and an early iOS SDK (e.g., iOS 3.0 - 5.1).

#### Building the iOS App

```bash
# Clone the repository
# Navigate to the project directory
cd Ano

# Compile and package the application
make package

# Install to a jailbroken device (requires SSH)
make package install
```

#### Running the Backend

Ano comes with a built-in API proxy by default. It works out of the box, so you don't need to configure or run anything manually!

*(If you wish to host your own backend, the Python server script is still available in the repository.)*

### Installing the .deb Package

If you already have the precompiled `.deb` package, you can install it on your jailbroken iOS device using one of the following methods:

**Method 1: Using iFile / Filza**
1. Transfer the `.deb` file to your device (via SSH, email, or cloud storage).
2. Open **iFile** or **Filza File Manager**.
3. Tap on the `.deb` file and select **Installer**.
4. Respring your device.

**Method 2: Using SSH (Command Line)**
1. Copy the `.deb` file to your device via SCP or SFTP.
2. SSH into your device.
3. Run the following command (replace `package_name.deb` with the actual filename):
   ```bash
   dpkg -i package_name.deb
   killall SpringBoard
   ```

### Support the Author

If you'd like to support the development and help cover hosting costs for the built-in API, you can donate via **TON**:
`UQD0nTUnlEDtCkYomVdL9oq7TpC-Fa6EEufEi-jH35-ljmd-`

---

## Русский

Ano — это легковесный, современный ИИ-клиент, созданный специально для **iPhone OS 3.0** и старых iOS-устройств. Разработанный **AnotherLabs**, Ano вдыхает новую жизнь в классическое железо, подключая его к передовым нейросетям.

📣 **Наш Telegram-канал:** [@theopenriver](https://t.me/theopenriver)

### Возможности

- **Поддержка ретро-устройств:** Идеально работает на iPhone OS 3.0+ (скомпилировано под архитектуру `armv6`).
- **Интеграция Mistral AI:** В качестве умного помощника используется Mistral AI.
- **История чатов и сессии:** Автоматическое локальное сохранение переписок. Удобный сайдбар для переключения между прошлыми диалогами.
- **Динамические темы:** Полная поддержка плавного переключения между **Светлой** и **Тёмной** темами.
- **Локализация:** Поддержка **английского** и **русского** языков.
- **Candy-бабблы чата:** Красивый ретро-модерновый интерфейс с градиентными пузырями сообщений, адаптированный под классические дисплеи iPhone.
- **Продуманный UX:** Умное скрытие клавиатуры, индикатор набора текста ("AI печатает...") и плавные анимации.

### Архитектура

Ano состоит из двух главных компонентов:
1. **iOS-клиент (Objective-C):** Нативный интерфейс, построенный на классических элементах `UIKit` (`UITableView`, `UIButton`, CoreGraphics), оптимизированный для эффективного использования оперативной памяти старых устройств.
2. **Бэкенд-мост (Python):** Лёгкий Flask-сервер, который общается с Mistral API и обходит проблемы со старыми сертификатами SSL/TLS на ретро-устройствах.

### Требования и сборка

Для сборки iOS-клиента потребуется настроенное окружение **Theos** с поддержкой `armv6` и классическим iOS SDK (например, iOS 3.0 - 5.1).

#### Сборка iOS-приложения

```bash
# Клонируйте репозиторий
# Перейдите в папку проекта
cd Ano

# Скомпилируйте и соберите пакет
make package

# Установите на устройство с джейлбрейком (требуется SSH)
make package install
```

#### Запуск бэкенда

В приложении уже встроен API-бэкенд по умолчанию. Оно работает "из коробки", так что вам ничего не нужно настраивать или запускать вручную!

*(Если вы хотите поднять свой собственный сервер, Python-скрипт по-прежнему доступен в репозитории.)*

### Установка .deb пакета

Если у вас уже есть скомпилированный `.deb` пакет, вы можете установить его на своё устройство с джейлбрейком одним из следующих способов:

**Способ 1: Через iFile / Filza**
1. Перенесите `.deb` файл на устройство (через SSH, почту или облако).
2. Откройте **iFile** или **Filza File Manager**.
3. Нажмите на `.deb` файл и выберите **Установщик (Installer)**.
4. Сделайте Respring (перезапуск рабочего стола).

**Способ 2: Через SSH (Командная строка)**
1. Скопируйте `.deb` файл на устройство через SCP или SFTP.
2. Подключитесь к устройству по SSH.
3. Выполните следующую команду (замените `package_name.deb` на имя вашего файла):
   ```bash
   dpkg -i package_name.deb
   killall SpringBoard
   ```

### Поддержать автора

Если вам нравится проект и вы хотите помочь с оплатой серверов для встроенного API, вы можете поддержать разработку:
- **Перевод на карту:** `2204 3211 5560 9365`
- **Boosty:** [boosty.to/anotherlabs](https://boosty.to/anotherlabs)

### Лицензия

Разработано **AnotherLabs** (Версия 1.0).
