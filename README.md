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

<h1>Прокси сервер MTProto для Telegram</h1>

<p>
🚀 <strong>MTProto Server Example — One-Command Installer</strong>
</p>

Прокси сервер MTProto для Telegram — это серверная конфигурация для подключения Telegram-клиентов через протокол MTProto. В этом репозитории показан практический вариант установки такого сервера на собственном VPS одной командой.

Пример настройки собственного MTProto server для Telegram: установка, конфигурация и подключение клиента к серверу.

Этот репозиторий предназначен для тех, кому нужен практический пример MTProto сервера без лишней инфраструктуры и сложной настройки.

<p>
🚀 <strong>Установка одной командой:</strong>
</p>

<pre><code>sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/tstas69-spec/mtproto-server-example/main/install.sh)"</code></pre>


Готовая инструкция по установке и настройке:

<p>
👉 <a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">
Открыть инструкцию по установке и настройке MTProto server
</a>
</p>

Язык

<p>
🇷🇺 <a href="#russian">Русский</a> |
🇬🇧 <a href="#english">English</a> |
🇨🇳 <a href="#chinese">中文</a> |
🇸🇦 <a href="#arabic">العربية</a> |
🇮🇷 <a href="#persian">فارسی</a>
</p>


<a id="russian"></a>

## Русский
MTProto server для Telegram

<a id="russian"></a>

## Русский

## Прокси сервер MTProto для Telegram

Прокси сервер MTProto для Telegram — это сервер на VPS, через который Telegram-клиент подключается к MTProto proxy. Этот репозиторий содержит готовый рабочий пример с автоматической установкой: скрипт install.sh запускает MTProto-прокси одной командой, устанавливает необходимые компоненты и выводит готовую ссылку для подключения.

👉 <a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">Пошаговая инструкция по установке прокси сервера MTProto для Telegram</a>

🚀 Установка одной командой

Для установки достаточно выполнить на VPS:

sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/tstas69-spec/mtproto-server-example/main/install.sh)"

Скрипт автоматически подготовит сервер и запустит MTProto proxy. Ручная установка Docker и настройка firewall не требуются.

Требования к VPS

Для работы прокси сервера достаточно недорогого VPS:

Ubuntu 20.04 или Ubuntu 22.04
1 CPU core
512 МБ RAM
открытый порт 443
доступ по SSH
root или пользователь с sudo

Для постоянного подключения рекомендуется выбирать VPS с нормальным сетевым соединением и выделенным IPv4-адресом.

🌍 Какой VPS выбрать

Для пользователей из разных стран доступность провайдеров и способы оплаты отличаются. В качестве основной локации для сервера можно использовать Европу.

В подробной инструкции приведён пример VPS-провайдера, подходящего для установки MTProto proxy, а также информация по выбору сервера и доступным вариантам оплаты.

Это особенно удобно, если VPS оплачивается из России, Китая или арабских стран: перед заказом необходимо проверить актуальные способы оплаты конкретного провайдера.

👉 <a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">Инструкция: VPS, установка и настройка MTProto proxy</a>

Что делает install.sh

После запуска скрипт:

обновляет систему;
устанавливает Docker;
устанавливает и настраивает ufw;
открывает порт 443;
запускает MTProto proxy;
использует Docker-образ nineseconds/mtg:2;
настраивает Fake TLS;
генерирует secret;
выводит готовую ссылку для подключения Telegram.

Таким образом, прокси сервер для Телеграмм можно подготовить без ручной последовательной установки нескольких компонентов.

📱 Как подключить MTProto прокси для Телеграмм

После выполнения install.sh сервер выводит ссылку примерно такого вида:

tg://proxy?server=IP&port=443&secret=КЛЮЧ

Эту ссылку можно открыть в Telegram. Клиент получит параметры сервера автоматически.

Для ручного подключения используются:

адрес сервера;
порт 443;
secret.

В Telegram параметры прокси находятся в разделе настроек подключения.

## MTProto прокси для телеграмм подключить

Если требуется именно MTProto прокси для телеграмм подключить, последовательность простая:

арендовать VPS;
установить Ubuntu 20.04 или 22.04;
подключиться к серверу по SSH;
выполнить команду install.sh;
получить готовую ссылку tg://proxy;
открыть ссылку в Telegram.

Подробные шаги, включая выбор VPS и настройку сервера, находятся в инструкции:

👉 <a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">Как установить и подключить MTProto прокси для Telegram</a>

Прокси сервер для Телеграмм: что находится в репозитории

Репозиторий содержит минимальный набор файлов для автоматической установки:

mtproto-server-example/
├── install.sh
└── README.md

Главный файл — install.sh. Он превращает чистый VPS с Ubuntu в работающий MTProto proxy без необходимости вручную устанавливать Docker, создавать firewall-правила и настраивать контейнер.

Что такое MTProto proxy

MTProto proxy — серверный компонент, который принимает соединение Telegram-клиента и передаёт его дальше через инфраструктуру Telegram.

В данном проекте используется готовая реализация mtg, запускаемая в Docker-контейнере.

Схема работы:

Telegram
   │
   │  MTProto
   ▼
VPS
   │
   ▼
MTProto Proxy
   │
   ▼
Telegram infrastructure

Проект рассчитан прежде всего на простой сценарий: один VPS → одна установка → готовая ссылка для Telegram.

Почему установка сделана через скрипт

При ручной настройке приходится отдельно устанавливать Docker, открывать порт, запускать контейнер и получать параметры подключения.

install.sh объединяет эти действия в одну команду.

Это делает репозиторий одновременно примером MTProto сервера и готовым шаблоном для быстрого развёртывания собственного MTProto proxy.

Быстрый старт

Минимальный сценарий выглядит так:

sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/tstas69-spec/mtproto-server-example/main/install.sh)"

После выполнения команды дождитесь завершения установки и сохраните выведенную ссылку tg://proxy.

Затем откройте её на устройстве с Telegram и подтвердите подключение.

📖 Полная инструкция

В README приведён рабочий пример установки, но отдельная инструкция содержит дополнительные сведения о VPS, выборе конфигурации, установке и подключении.

👉 <a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">Открыть полную инструкцию по MTProto server и Telegram proxy</a>

Основные запросы

Проект ориентирован на практические задачи, связанные с:

прокси сервер MTProto для Telegram;
прокси сервер для Телеграмм;
MTProto прокси для телеграмм подключить;
MTProto server;
MTProto proxy;
MTProto server example;
Telegram proxy server;
установка MTProto proxy;
подключение MTProto в Telegram.

<a id="english"></a>

## English

MTProto Server Example

<a id="english"></a>

## English

This repository is a working **MTProto server example**. The `install.sh` script deploys the proxy on your VPS with a single command, without manual Docker or firewall configuration.

### Requirements

- VPS running **Ubuntu 20.04 or 22.04**
- Minimum: **1 CPU core, 512 MB RAM**
- Port **443** available
- **SSH** access (root or sudo)
- A VPS location in **Europe** is recommended
- VPS providers may offer different payment methods. The step-by-step guide includes an example provider and additional information about VPS setup and payment options.

### 🚀 One-command installation

```bash
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/tstas69-spec/mtproto-server-example/main/install.sh)"
```
What the script does:

updates the system;
installs Docker and firewall (ufw);
opens port 443;
starts MTProto proxy on port 443;
uses nineseconds/mtg:2 with Fake TLS;
generates a secret key;
outputs a ready-to-use Telegram proxy link.
📖 Connect the proxy

After installation, the script provides a link similar to:

tg://proxy?server=IP&port=443&secret=SECRET

This repository provides a practical MTProto server example for Telegram.

It can be used as a starting point for deploying and configuring your own MTProto server on a VPS.

👉 MTProto server installation and configuration guide
<a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">
Step-by-step MTProto server installation and configuration guide
</a>

What is MTProto server?

MTProto is the protocol used by Telegram clients for communication with Telegram infrastructure.

An MTProto server can be configured as an independent server component with its own connection parameters and access settings.

This repository focuses on the practical side of MTProto server configuration rather than protocol theory.

MTProto server setup

A typical setup looks like:

Telegram client
       |
       v
   MTProto
    server
       |
       v
 Telegram infrastructure

The exact installation steps depend on the selected implementation and server environment.

For a complete step-by-step setup:

👉 MTProto server guide
<a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">
Step-by-step MTProto server installation and configuration guide
</a>

MTProto proxy

MTProto proxy is commonly used as a server-side component for Telegram connections.

Typical configuration parameters include:

server address;
port;
secret;
client connection parameters.

See the installation guide for the complete configuration:

👉 MTProto server documentation
<a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">
Step-by-step MTProto server installation and configuration guide
</a>

Keywords

MTProto server, MTProto server example, MTProto proxy, Telegram MTProto server, MTProto proxy server, Telegram proxy server.

<a id="chinese"></a>

## 中文

MTProto Server 示例

<a id="chinese"></a>

## 中文

本项目是一个可实际使用的 **MTProto server 示例**。`install.sh` 脚本可以通过一条命令在 VPS 上完成代理部署，无需手动配置 Docker 和防火墙。

### 系统要求

- **Ubuntu 20.04 或 22.04**
- 最低配置：**1 个 CPU 核心、512 MB RAM**
- 开放 **443 端口**
- 具有 **SSH** 访问权限（root 或 sudo）
- 推荐选择位于**欧洲**的 VPS
- 不同 VPS 服务商支持的付款方式不同。完整指南中提供了服务商示例以及 VPS 选择和付款说明。

### 🚀 一键安装

```bash
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/tstas69-spec/mtproto-server-example/main/install.sh)"
```
安装脚本会完成：

更新系统；
安装 Docker 和防火墙 ufw；
开放 443 端口；
在 443 端口启动 MTProto proxy；
使用 nineseconds/mtg:2 和 Fake TLS；
自动生成 secret；
输出 Telegram 可使用的连接链接。
📖 如何连接

安装完成后会得到类似下面的链接：

tg://proxy?server=IP&port=443&secret=SECRET

复制链接并在 Telegram 中打开。

本项目提供一个用于 Telegram 的 MTProto server 示例，可以作为部署和配置 MTProto 服务器的基础参考。

👉 MTProto server 安装与配置指南
<a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">
MTProto Server 安装与配置分步指南
</a>

什么是 MTProto Server？

MTProto 是 Telegram 使用的通信协议。

MTProto server 可以部署在自己的 VPS 上，并根据需要配置服务器地址、端口、secret 等连接参数。

本项目主要用于展示 MTProto server 的基本结构和配置方式。

MTProto Server 配置

基本结构：

Telegram 客户端
       |
       v
  MTProto Server
       |
       v
Telegram infrastructure

完整的安装和配置步骤：

👉 MTProto server 指南
<a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">
MTProto Server 安装与配置分步指南
</a>

MTProto Proxy

MTProto proxy 是 Telegram 生态中常见的服务器组件。

配置通常涉及：

服务器地址；
端口；
secret；
客户端连接参数。

更多安装资料：

👉 MTProto server installation guide
<a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">
MTProto Server 安装与配置分步指南
</a>

相关关键词

MTProto server、MTProto server example、MTProto proxy、Telegram MTProto server、Telegram proxy server。

<a id="arabic"></a>

## العربية

العربية
مثال MTProto Server

<a id="arabic"></a>



هذا المستودع هو **مثال عملي لخادم MTProto**. يقوم السكربت `install.sh` بإعداد الخادم على VPS باستخدام أمر واحد، من دون الحاجة إلى إعداد Docker أو جدار الحماية يدوياً.

### متطلبات النظام

- **Ubuntu 20.04 أو 22.04**
- الحد الأدنى: **نواة CPU واحدة و512 MB من RAM**
- فتح المنفذ **443**
- الوصول عبر **SSH** باستخدام root أو sudo
- يُنصح باختيار VPS في **أوروبا**
- تختلف طرق الدفع حسب مزود VPS. يتضمن الدليل الكامل مثالاً على مزود مناسب ومعلومات حول إعداد الخادم وخيارات الدفع.

### 🚀 التثبيت بأمر واحد

```bash
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/tstas69-spec/mtproto-server-example/main/install.sh)"
```
يقوم السكربت بما يلي:

تحديث النظام؛
تثبيت Docker وufw؛
فتح المنفذ 443؛
تشغيل MTProto proxy على المنفذ 443؛
استخدام nineseconds/mtg:2 مع Fake TLS؛
إنشاء secret تلقائياً؛
إنشاء رابط جاهز للاتصال عبر Telegram.
📖 كيفية الاتصال

بعد التثبيت سيظهر رابط مشابه لهذا:

tg://proxy?server=IP&port=443&secret=SECRET

انسخ الرابط وافتحه في Telegram.

هذا المستودع يحتوي على مثال عملي لإعداد MTProto server لاستخدامه مع Telegram.

يمكن استخدام المشروع كنقطة بداية لفهم بنية خادم MTProto وإعداده على VPS.

👉 دليل تثبيت وإعداد MTProto server
<a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">
دليل خطوة بخطوة لتثبيت وإعداد MTProto server
</a>
ما هو MTProto Server؟

MTProto هو بروتوكول الاتصال المستخدم في Telegram.

يمكن إعداد MTProto server بشكل مستقل مع تحديد إعدادات الاتصال الخاصة به.

يتضمن الإعداد عادةً:

عنوان الخادم؛
المنفذ؛
secret؛
إعدادات اتصال العميل.
إعداد MTProto Server

البنية الأساسية:

Telegram client
       |
       v
   MTProto server
       |
       v
Telegram infrastructure

للحصول على خطوات التثبيت والإعداد بالتفصيل:

👉 دليل MTProto server
<a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">
دليل خطوة بخطوة لتثبيت وإعداد MTProto server
</a>

MTProto Proxy

يُستخدم مصطلح MTProto proxy لوصف خادم وسيط يعتمد على بروتوكول MTProto لاتصالات Telegram.

يمكن العثور على خطوات الإعداد الكاملة هنا:

👉 MTProto server installation guide

<a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">
دليل خطوة بخطوة لتثبيت وإعداد MTProto server
</a>

كلمات مفتاحية

MTProto server، MTProto server example، MTProto proxy، Telegram MTProto server، Telegram proxy server.
<a id="persian"></a>

## فارسی

این مخزن یک **نمونه عملی MTProto server** است. اسکریپت `install.sh` سرور را با یک دستور روی VPS راه‌اندازی می‌کند و نیازی به تنظیم دستی Docker یا فایروال نیست.

### نیازمندی‌های سیستم

- **Ubuntu 20.04 یا 22.04**
- حداقل: **۱ هسته CPU و ۵۱۲ مگابایت RAM**
- پورت **443** باز باشد
- دسترسی **SSH** با root یا sudo
- استفاده از VPS در **اروپا** پیشنهاد می‌شود
- روش‌های پرداخت به ارائه‌دهنده VPS بستگی دارد. در راهنمای کامل، نمونه‌ای از ارائه‌دهنده VPS و اطلاعات مربوط به انتخاب سرور و پرداخت ارائه شده است.

### 🚀 نصب با یک دستور

```bash
sudo bash -c "$(curl -fsSL https://raw.githubusercontent.com/tstas69-spec/mtproto-server-example/main/install.sh)"
```
اسکریپت این کارها را انجام می‌دهد:

سیستم را به‌روزرسانی می‌کند؛
Docker و فایروال ufw را نصب می‌کند؛
پورت 443 را باز می‌کند؛
MTProto proxy را روی پورت 443 اجرا می‌کند؛
از nineseconds/mtg:2 با Fake TLS استفاده می‌کند؛
secret را ایجاد می‌کند؛
لینک آماده اتصال به Telegram را نمایش می‌دهد.
📖 نحوه اتصال

پس از نصب، لینکی مشابه نمونه زیر دریافت می‌کنید:

tg://proxy?server=IP&port=443&secret=SECRET

لینک را کپی کرده و در Telegram باز کنید.

فارسی
نمونه MTProto Server

این مخزن یک نمونه عملی برای راه‌اندازی و پیکربندی MTProto server برای Telegram ارائه می‌کند.

می‌توان از این پروژه به عنوان نقطه شروع برای راه‌اندازی یک سرور MTProto روی VPS استفاده کرد.

👉 راهنمای نصب و تنظیم MTProto server
<a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">
راهنمای گام‌به‌گام نصب و تنظیم MTProto server
</a>

MTProto Server چیست؟

MTProto پروتکل ارتباطی مورد استفاده Telegram است.

MTProto server را می‌توان روی یک VPS مستقل نصب و با پارامترهای مورد نیاز پیکربندی کرد.

تنظیمات معمول شامل موارد زیر است:

آدرس سرور؛
پورت؛
secret؛
پارامترهای اتصال کلاینت.
راه‌اندازی MTProto Server

ساختار کلی:

Telegram client
       |
       v
   MTProto server
       |
       v
Telegram infrastructure

راهنمای کامل نصب و تنظیم:

👉 MTProto server — راهنمای مرحله‌به‌مرحله

<a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">
راهنمای گام‌به‌گام نصب و تنظیم MTProto server
</a>

MTProto Proxy

MTProto proxy یکی از روش‌های متداول برای ایجاد اتصال Telegram بر اساس پروتکل MTProto است.

برای مشاهده مراحل نصب و تنظیم سرور:

👉 راهنمای MTProto server
<a href="https://tstas69-spec.github.io/" target="_blank" rel="noopener noreferrer">
راهنمای گام‌به‌گام نصب و تنظیم MTProto server
</a>
کلمات کلیدی

MTProto server، MTProto server example، MTProto proxy، Telegram MTProto server، Telegram proxy server.

Documentation

The repository is intentionally kept simple. The main installation and configuration instructions are maintained separately:

👉 https://tstas69-spec.github.io/

If you are looking for:

MTProto server example
MTProto server setup
MTProto proxy configuration
Telegram MTProto server
Telegram proxy server
MTProto server installation

start with the documentation above.
