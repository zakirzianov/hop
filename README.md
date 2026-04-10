# Hop
Hop for AWG \ VLESS
# 🌊 Hop Traffic Manager

**Скрипт для переадресации трафика (NAT) и ускорения сети на Linux.**

Cоздание "мостов" к VPN (AmneziaWG, WireGuard) и Proxy (VLESS, XRay).


---

##  Возможности

* ** High Speed Core:** Работает через **Iptables (Kernel NAT)**. Никаких лишних процессов, скорость ограничена только каналом сервера.
* ** BBR Turbo:** Автоматически включает алгоритм **Google BBR** для максимального ускорения TCP соединений.
* ** Мультипротокольность:**
    * Поддержка **UDP** (AmneziaWG, WireGuard).
    * Поддержка **TCP** (VLESS, VMess, Reality).
* ** Мульти-туннелирование:** Создавайте 2, 5, 10 соединений на разных портах одновременно.
* ** Умная настройка:**
    * Автоматическое открытие портов в UFW.
    * Отключение `rp_filter` (важно для VPN).
    * Сохранение правил после перезагрузки (`netfilter-persistent`).
* ** Удобное меню:** Просмотр списка правил, удаление по одному, полный сброс.

---

##  Быстрая установка

Подключитесь к вашему VPS (Ubuntu/Debian) и выполните одну команду:

```bash
wget -O install.sh https://raw.githubusercontent.com/anten-ka/kaskad/main/install.sh && chmod +x install.sh && ./install.sh
