<!-- 
  ============================================================
  MTProto Server Example — One-Command Installer
  ============================================================
-->

<p align="center">
  <img src="https://img.shields.io/github/stars/tstas69-spec/mtproto-server-example?style=for-the-badge&color=yellow" alt="Stars">
  <img src="https://img.shields.io/badge/Docker-ready-blue?style=for-the-badge" alt="Docker">
  <img src="https://img.shields.io/badge/Ubuntu-20.04%20%7C%2022.04-orange?style=for-the-badge" alt="Ubuntu">
  <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License">
</p>

<h1 align="center">🚀 MTProto Server — Example & One-Command Installer</h1>

<p align="center">
  <strong>Working example of an MTProto server for Telegram. Deploy your own proxy in one command.</strong><br>
  <strong>Пример MTProto сервера для Telegram. Установка прокси за одну команду.</strong>
</p>

<br>

<p align="center">
  <b>🌐 Выберите язык / Choose language / 选择语言 / اختر اللغة</b><br><br>
  <a href="#ru"><img src="https://flagcdn.com/ru.svg" width="30" alt="Русский"> Русский</a> •
  <a href="#en"><img src="https://flagcdn.com/gb.svg" width="30" alt="English"> English</a> •
  <a href="#zh"><img src="https://flagcdn.com/cn.svg" width="30" alt="中文"> 中文</a> •
  <a href="#ar"><img src="https://flagcdn.com/sa.svg" width="30" alt="العربية"> العربية</a>
  <a href="#fa"><img src="https://flagcdn.com/ir.svg" width="30" alt="فارسی"> فارسی</a>
</p>

<br>

<h2 align="center">⚡ One Command to Install an MTProto Server</h2>

<p align="center">
  <code>sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/tstas69-spec/mtproto-server-example/main/install.sh)"</code>
</p>

<p align="center">
  <a href="https://tstas69-spec.github.io/">
    <img src="https://img.shields.io/badge/📖_Full_Guide_with_Screenshots-Click_Here-success?style=for-the-badge" alt="Full Guide">
  </a>
</p>

<hr>

<a id="ru"></a>
## 🇷🇺 Русский

**MTProto** — официальный протокол Telegram, который используется для обхода блокировок мессенджера. Он маскирует трафик под обычный HTTPS, поэтому провайдеру сложнее его отличить от рядового веб-серфинга — в отличие от классического VPN, который проще детектировать.

Этот репозиторий — рабочий **пример MTProto сервера**: скрипт `install.sh` поднимает прокси на вашем VPS одной командой, без ручной настройки Docker и firewall.

### Требования
- VPS с **Ubuntu 20.04 или 22.04**
- Минимум: 1 ядро, 512 МБ RAM
- Открытый порт 443
- Доступ по SSH (root или sudo)

### 🚀 Установка одной командой

```bash
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/tstas69-spec/mtproto-server-example/main/install.sh)"
```

**Что делает скрипт:**
- Обновляет систему
- Устанавливает Docker и firewall (ufw)
- Открывает порт 443
- Запускает MTProto-прокси на порту 443 (образ `nineseconds/mtg:2`, Fake TLS)
- Генерирует секретный ключ и готовую ссылку для Telegram

### 📖 Как подключить прокси
После установки вы получите ссылку вида:

```
tg://proxy?server=IP&port=443&secret=КЛЮЧ
```

Скопируйте её и вставьте в Telegram: **Настройки → Данные и память → Настройка прокси**.

### 🔗 Пошаговая инструкция с картинками
Если вы новичок и хотите увидеть весь процесс с нуля — как арендовать VPS, подключиться по SSH и настроить сервер — там расписан каждый шаг со скриншотами:

👉 **[Полная инструкция →](https://tstas69-spec.github.io/)**

<a id="en"></a>
## 🇬🇧 English

**MTProto** is Telegram's own protocol for bypassing network restrictions. It disguises traffic as regular HTTPS, which makes it harder for a provider to detect than a classic VPN.

This repository is a working **MTProto server example**: `install.sh` spins up a proxy on your VPS in one command, no manual Docker or firewall setup needed.

### Requirements
- VPS with **Ubuntu 20.04 or 22.04**
- Minimum: 1 core, 512 MB RAM
- Open port 443
- SSH access (root or sudo)

### 🚀 One-Command Installation

```bash
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/tstas69-spec/mtproto-server-example/main/install.sh)"
```

**What the script does:**
- Updates the system
- Installs Docker and a firewall (ufw)
- Opens port 443
- Starts an MTProto proxy on port 443 (`nineseconds/mtg:2` image, Fake TLS)
- Generates a secret key and a ready-to-use Telegram link

### 📖 Connecting the proxy
After installation you'll get a link like:

```
tg://proxy?server=IP&port=443&secret=KEY
```

Copy it and paste into Telegram: **Settings → Data and Storage → Proxy Settings**.

### 🔗 Full step-by-step guide
New to this? The full guide covers everything from scratch — renting a VPS, connecting via SSH, and setting it all up, with screenshots for every step:

👉 **[Full guide →](https://tstas69-spec.github.io/mtproto-en.html)**

<a id="zh"></a>
## 🇨🇳 中文

**MTProto** 是 Telegram 官方用于绕过网络限制的协议。它将流量伪装成普通 HTTPS 流量，因此比传统 VPN 更难被运营商识别。

本仓库提供一个可用的 **MTProto 服务器示例**：`install.sh` 一条命令即可在您的 VPS 上启动代理，无需手动配置 Docker 和防火墙。

### 系统要求
- VPS，系统为 **Ubuntu 20.04 或 22.04**
- 最低配置：1 核 CPU，512 MB 内存
- 开放端口 443
- SSH 访问权限（root 或 sudo）

### 🚀 一键安装

```bash
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/tstas69-spec/mtproto-server-example/main/install.sh)"
```

**脚本执行的操作：**
- 更新系统
- 安装 Docker 和防火墙（ufw）
- 开放端口 443
- 在 443 端口启动 MTProto 代理（`nineseconds/mtg:2` 镜像，Fake TLS 伪装）
- 生成密钥并输出可直接使用的 Telegram 链接

### 📖 如何连接代理
安装完成后，您会得到类似的链接：

```
tg://proxy?server=IP&port=443&secret=密钥
```

复制并粘贴到 Telegram：**设置 → 数据和存储 → 代理设置**。

### 🔗 完整分步教程
新手用户可查看带截图的完整教程 — 从租用 VPS、通过 SSH 连接到最终配置，每一步都有说明：

👉 **[查看完整教程 →](https://tstas69-spec.github.io/mtproto-zh.html)**

<a id="ar"></a>
## 🇸🇦 العربية

**MTProto** هو بروتوكول Telegram الرسمي لتجاوز القيود المفروضة على الشبكة. يُخفي هذا البروتوكول حركة البيانات على أنها HTTPS عادية، مما يجعل اكتشافه أصعب مقارنة بشبكات VPN التقليدية.

هذا المستودع هو مثال عملي لـ **خادم MTProto**: يقوم ملف `install.sh` بتشغيل الوكيل على خادمك (VPS) بأمر واحد فقط، دون الحاجة لإعداد Docker أو جدار الحماية يدويًا.

### المتطلبات
- خادم VPS بنظام **Ubuntu 20.04 أو 22.04**
- الحد الأدنى: نواة واحدة، 512 ميجابايت رام
- منفذ مفتوح 443
- وصول SSH (root أو sudo)

### 🚀 التثبيت بأمر واحد

```bash
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/tstas69-spec/mtproto-server-example/main/install.sh)"
```

**ما يقوم به السكربت:**
- تحديث النظام
- تثبيت Docker وجدار الحماية (ufw)
- فتح المنفذ 443
- تشغيل وكيل MTProto على المنفذ 443 (صورة `nineseconds/mtg:2`، تمويه Fake TLS)
- إنشاء مفتاح سري ورابط جاهز لتطبيق Telegram

### 📖 كيفية توصيل الوكيل
بعد التثبيت ستحصل على رابط مثل:

```
tg://proxy?server=IP&port=443&secret=المفتاح
```

انسخه والصقه في Telegram: **الإعدادات → البيانات والتخزين → إعدادات الوكيل**.

### 🔗 الدليل الكامل خطوة بخطوة
دليل كامل بالشرح والصور من الصفر — استئجار الخادم، الاتصال عبر SSH، والإعداد الكامل:

👉 **[الدليل الكامل →](https://tstas69-spec.github.io/mtproto-ar.html)**

<a id="fa"></a>
## 🇮🇷 فارسی

**MTProto** پروتکل رسمی تلگرام برای عبور از فیلترینگ و محدودیت‌های شبکه است. این پروتکل ترافیک را شبیه HTTPS معمولی می‌کند، به همین دلیل تشخیص آن برای اپراتور نسبت به یک VPN معمولی سخت‌تر است.

این مخزن یک نمونه‌ی کارِ **سرور MTProto** و راه‌اندازی **پروکسی تلگرام** است: اسکریپت `install.sh` با یک دستور، پروکسی را روی VPS شما راه‌اندازی می‌کند — بدون نیاز به تنظیم دستی Docker یا فایروال.

### پیش‌نیازها
- VPS با **اوبونتو ۲۰.۰۴ یا ۲۲.۰۴**
- حداقل: ۱ هسته پردازنده، ۵۱۲ مگابایت رم
- پورت ۴۴۳ باز باشد
- دسترسی SSH (root یا sudo)

### 🚀 نصب پروکسی تلگرام با یک دستور

```bash
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/tstas69-spec/mtproto-server-example/main/install.sh)"
```

**این اسکریپت چه کاری انجام می‌دهد:**
- سیستم را به‌روزرسانی می‌کند
- Docker و فایروال (ufw) را نصب می‌کند
- پورت ۴۴۳ را باز می‌کند
- یک **پروکسی MTProto** روی پورت ۴۴۳ اجرا می‌کند (ایمیج `nineseconds/mtg:2`، با Fake TLS)
- یک کلید مخفی و لینک آماده برای تلگرام تولید می‌کند

### 📖 نحوه اتصال پروکسی تلگرام
بعد از نصب، لینکی شبیه این دریافت می‌کنید:

```
tg://proxy?server=IP&port=443&secret=KEY
```

آن را کپی کرده و در تلگرام وارد کنید: **تنظیمات ← داده و حافظه ← تنظیمات پروکسی**.

### 🔗 راهنمای کامل قدم‌به‌قدم
اگر تازه‌کار هستید، راهنمای کامل با تصاویر — از اجاره VPS تا اتصال SSH و پیکربندی نهایی — هر مرحله را توضیح می‌دهد:

👉 **[راهنمای کامل ←](https://tstas69-spec.github.io/mtproto-ir.html)**
<hr>

<p align="center">
  <b>⭐ Поставьте звезду, если репозиторий помог! / Star this repo if it helped! / 如果这个仓库有帮助，请给它一个星！ / ضع نجمة إذا أعجبك المستودع! / اگر این مخزن به شما کمک کرد، ستاره بدهید!</b>
</p>
<p align="center">
  <a href="https://tstas69-spec.github.io/">
    <img src="https://img.shields.io/badge/📖_Full_Guide-tstas69--spec.github.io-blue?style=for-the-badge" alt="Full Guide">
  </a>
</p>



