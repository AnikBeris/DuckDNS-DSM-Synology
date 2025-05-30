**------->** [English](/README_en_EN.md) | [Русский](/README.md) **<-------**

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="./media/logo-dark.png">
    <img alt="Project Logo" src="./media/logo-light.png" width="512" height="auto">
  </picture>
</p>

---

<div align="center">

[![GitHub](https://img.shields.io/badge/GitHub-blue?style=flat&logo=github)](https://github.com/AnikBeris)
[![License](https://img.shields.io/badge/License-purple?style=flat&logo=github)](https://github.com/AnikBeris/n8n-docker/blob/main/LICENSE.md)
[![GitHub Stars](https://img.shields.io/github/stars/your-repo?style=flat&logo=github&label=Звёзды&color=orange)](https://github.com/AnikBeris)

</div>

# Техническое руководство по добывлению [DuckDNS](https://www.duckdns.org) в DSM [Synology](https://www.synology.com/).




> **Отказ от ответственности:** Всё преведенные материалы расчитаны на личное использование.

**Если этот проект оказался полезным для Вас, вы можете оценить его, поставив звёздочку.**:star2:

<p align="left">
  <a href="https://pay.cloudtips.ru/p/7249ba98" target="_blank">
    <img src="./media/buymeacoffe.png" alt="Image">
  </a>
</p>

Пожертвования горячо приветствуются, какими бы маленькими они ни были, и большое спасибо. 😌

| | |
|-------------:|:-------------|
| **Bitcoin (BTC)** |`1Dbwq9EP8YpF3SrLgag2EQwGASMSGLADbh`|
| **Ethereum (ERC20)** | `0x22258ea591966e830199d27dea7c542f31ed5dc5`|
| **Binance Smart Chain (BEP20)** | `0x22258ea591966e830199d27dea7c542f31ed5dc5`|
| **Solana (SOL)** | `yYYXsiVTzsvfvsMnBxfxSZEWTGytjAViE2ojf3hbLeF`|
| **Cloud tips** | [cloudtips](https://pay.cloudtips.ru/p/7249ba98) |
---

<table align="center">
  <tr>
    <td><img src="./media/logo-dsm.png" alt="DSM Logo" width="128"></td>
    <td><img src="./media/logo-DuckDns.png" alt="DuckDNS Logo" width="140"></td>
  </tr>
</table>





# 🚀 Установка [DuckDNS](https://www.duckdns.org)


Этот гайд поможет вам добавить поставщика услуг в виде **DuckDNS** в оболочку **DSM** версии **DSM 7..** и выше

---

# Шаг 1: 📌 Создание домена
---
![//](./media/DuckDNS_Synology_1.png)

- вводим доменное `имя` и нажимаем `add a domain`
![//](./media/DuckDNS_Synology_1-2.png)

---

# Шаг 2: 📌 переходим в [Synology](https://www.synology.com/) и создаём поставщика услуг

![//](./media/DuckDNS_Synology_3.png)

- `панель управления -> Внешний доступ -> DDNS -> Кнопка ДОБАВИТЬ -> Настроить поставщика`

---

![//](./media/DuckDNS_Synology_4.png)

- заполяем поле `Query URL:`:

```bash
http://www.duckdns.org/update?
ip=__MYIP__&domains=__HOSTNAME__&token=__PASSWORD__

```

---

# Шаг 3: 📌 Заполняем поля:

![//](./media/DuckDNS_Synology_5.png)

- для заполнения берём информацияю с сайта [DuckDNS](https://www.duckdns.org)

![//](./media/DuckDNS_Synology_2.png)

- - **`выбираем созданного поставщека услуг`** в *моём случае это `DuckDNS`*
- - **`имя хоста`** это `cсозданный суб домен + домен (.duckdns.org)` в *моём случае `votonokak.duckdns.org`*
- - **`имя пользователя`** это `почта` на которую зарегестрирован акаунт в *моём случае `xxxxxxxx@gmail.com`*
- - **`пароль/ключь`** это `token`
- - **`внешний адрес (IPv4)`** выбираем либо:
- - - **`АВТО`** `->` будет подставлен внешний IP адрес для доступа из сети интернет
- - - **`ЛВС1`** `->` будет подставлен IP адрес первого порта Lan (физичесни подключеного)
- - - **`ЛВС2`** `->` будет подставлен IP адрес второго порта Lan (физичесни подключеного)

# -> **нажимаем тестовое подключение** <-
если всё сделано правильно загорится зелёный текст ![//](./media/DuckDNS_Synology_6.png)
---

---
