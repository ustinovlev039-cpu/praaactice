[← Подготовка среды](lab-environment.md)

# Локальные образы для лабораторных работ

Этот перечень составлен по папкам `VirtualBox VMs` и `Downloads` 14 ноября 2026 года. Сопоставление проверено по названиям файлов и требованиям практических заданий из архива «пт.zip»; содержимое гостевых систем не проверялось. Перед повторением работы нужно проверить конфигурацию и состояние каждой ВМ в VirtualBox. Файлы образов не размещены в репозитории.

## Установленные машины: `VirtualBox VMs`

| Лабораторная работа | Папки ВМ | Размер диска каждой ВМ |
| :-- | :-- | --: |
| [Динамическая маршрутизация OSPF](../labs/network/05-ospf/README.md) | `Mikrotik1-ospf`, `Mikrotik2-ospf`, `Mikrotik3-ospf`, `Mikrotik4-ospf` | 54–55 МиБ |
| [DNS](../labs/network/06-dns/README.md) | `Mikrotik1-DNS`, `Mikrotik2-DNS` | 54 МиБ |
| [VLAN](../labs/network/07-vlan/README.md) | `Mikrotik1-VLAN`, `Mikrotik2-VLAN`, `Mikrotik3-VLAN` | 55 МиБ |
| [NAT](../labs/network/08-nat/README.md) | `Mikrotik1-NAT`, `Mikrotik2-NAT` | 54 МиБ |
| [OpenVPN](../labs/network/09-openvpn/README.md) | `Mikrotik-OpenVPN` | 55 МиБ |
| [3proxy](../labs/network/10-3proxy/README.md) | `Mikrotik-proxy` | 54 МиБ |
| [ARP Spoofing](../labs/network/11-arp-spoofing/README.md) | `Mikrotik-ARP` | 55 МиБ |
| [ICMP](../labs/network/13-icmp-discovery/README.md) | `Mikron-ICMP` | 55 МиБ |
| [ICMP](../labs/network/13-icmp-discovery/README.md), [UDP-сканирование](../labs/network/14-udp-scanning/README.md), [TCP-сканирование](../labs/network/15-tcp-scanning/README.md) | `Server_Scan` | 2 959 МиБ |
| [Подбор паролей Telnet](../labs/network/16-telnet-bruteforce/README.md) | `MikroTik_Telnet` | 61 МиБ |
| [Log4Shell](../labs/network/18-log4shell-detection/README.md), [Telnetd bypass](../labs/network/19-telnet-auth-bypass/README.md), [ReactShell](../labs/network/20-reactshell/README.md) | `Mikrotik-2.18-2.20` | 54 МиБ |

Также в папке есть базовые `MikroTik` (54 МиБ), `Network-Debian-Gold 2` (4 674 МиБ) и `Debian-12-Gold_2` (4 073 МиБ). Их точное соответствие отдельным кейсам по имени определить нельзя. У `Debian-12-Gold_2` есть снимок состояния; один базовый диск не восстановит текущую машину без цепочки снимков.

Машины с названиями `Debian-Practice 1`, `Debian-Practice-1_5`, `Debian-cold-monitoring*` и `Guided-Case_1.1_1.3_1.4` относятся по именам к главе Linux, которая не входит в это портфолио.

## Архивы и установочные образы: `Downloads`

Размеры округлены до целых МиБ. OVA — переносимый архив ВМ; ISO — установочный образ, который сам по себе не содержит настроенный учебный стенд.

### Сети

| Работа | Найденный файл | Размер | Назначение |
| :-- | :-- | --: | :-- |
| [2.1–2.10](../labs/network/README.md) | `Network-Debian-Gold.ova` | 1 372 МиБ | Базовая Debian-машина для первых сетевых кейсов; конкретную настройку нужно делать по заданию. |
| [2.3 DHCP](../labs/network/03-dhcp/README.md) | `DebianDHCP.ova`, `MikrotikDHCP.ova` | 1 206 и 42 МиБ | Отдельные машины Debian и MikroTik для DHCP. |
| [2.10 3proxy](../labs/network/10-3proxy/README.md) | `DebianGUI-Proxy.ova` | 3 019 МиБ | Дополнительная Debian-машина с GUI для сценария с прокси. |
| [2.11 ARP Spoofing](../labs/network/11-arp-spoofing/README.md) | `DebianARP.ova` | 1 213 МиБ | Подготовленная машина-жертва Debian. |
| [2.16 Telnet](../labs/network/16-telnet-bruteforce/README.md) | `MikroTik_Telnet.ova` | 43 МиБ | Подготовленный маршрутизатор. |
| [2.18 Log4Shell](../labs/network/18-log4shell-detection/README.md) | `Log4.ova` | 1 692 МиБ | Подготовленная цель для Log4Shell. |
| [2.19 Telnetd bypass](../labs/network/19-telnet-auth-bypass/README.md) | `VictimTelnet.ova` | 1 299 МиБ | Подготовленная цель с Telnet. |
| [2.20 ReactShell](../labs/network/20-reactshell/README.md) | `React2Shell.ova` | 3 395 МиБ | Подготовленная цель React. |
| Несколько сетевых работ | `chr-7.21.4(1).ova` | 42 МиБ | Базовый MikroTik CHR; без привязки к одной работе. |
| [2.17 Password Spraying](../labs/network/17-password-spraying/README.md) | `OPNsense-26.1.2-dvd-amd64.iso` | 2 105 МиБ | Установщик OPNsense, нужный для маршрутизатора и IDS; подготовленный FTP-сервер в `Downloads` не найден. |

`Network-Debian-Gold(2).ova` — точная копия `Network-Debian-Gold.ova` (совпадает SHA-256), поэтому второй раз в таблице не учитывается. Для [2.12 Rogue DHCP](../labs/network/12-rogue-dhcp/README.md) исходный кейс требует отдельную подготовленную машину-жертву и MikroTik; файлов с однозначным соответствием этому кейсу не найдено.

### Windows

| Работы | Найденный файл | Размер | Назначение |
| :-- | :-- | --: | :-- |
| [3.1–3.9](../labs/windows/README.md) | `windows 11.ova` | 17 188 МиБ | Базовая Windows 11 для работ со службами, драйверами, пользователями, автозапуском, реестром, NFS, RDP/WinRM, локальными политиками и журналированием. |
| [3.10 AD DS](../labs/windows/10-active-directory/README.md), [3.13 GPO](../labs/windows/13-gpo/README.md) | `windows 11.ova`, `ServerWindows.ova` | 17 188 и 6 836 МиБ | Клиент и сервер домена; 3.13 продолжает стенд 3.10. |
| [3.11 IIS](../labs/windows/11-iis/README.md), [3.12 AD CS](../labs/windows/12-ad-cs/README.md) | `ServerWindows.ova` | 6 836 МиБ | Базовый Windows Server. |

### Web / OWASP

| Работа | Найденный файл | Размер |
| :-- | :-- | --: |
| [4.2 XSS](../labs/web/02-xss/README.md) | `Guided Case_4.2 - эксплуатация XSS.ova` | 1 110 МиБ |
| [4.3 SQL Injection](../labs/web/03-sql-injection/README.md) | `Guided_Case_4.3.ova` | 1 078 МиБ |
| [4.4 IDOR](../labs/web/04-idor/README.md) | `Guided Case_4.4.ova` | 1 054 МиБ |
| [4.5 LFI](../labs/web/05-lfi/README.md) | `Guided_Case_4.5.ova` | 1 064 МиБ |
| [4.6 Directory Traversal](../labs/web/06-directory-traversal/README.md) | `Guided Case_4.6 - эксплуатация Directory Traversal.ova` | 1 016 МиБ |
| [4.7 Command Injection](../labs/web/07-command-injection/README.md) | `Guided_Case_4.7.ova` | 972 МиБ |
| [4.8 Code Injection](../labs/web/08-code-injection/README.md) | `Guided_Case_4.8.ova` | 1 175 МиБ |
| [4.9 XXE](../labs/web/09-xxe/README.md) | `Guided_Case_4.9.ova` | 1 158 МиБ |
| [4.10 SSTI](../labs/web/10-ssti/README.md) | `Guided Case_4.10 - эксплуатация SSTI.ova` | 1 041 МиБ |
| [4.11 Race Condition](../labs/web/11-race-condition/README.md) | `Guided Case_4.11 - эксплуатация Race Condition.ova` | 1 058 МиБ |

Для [4.12 DefectDojo](../labs/web/12-defectdojo/README.md), [4.13 SAST](../labs/web/13-sast/README.md) и [4.14 SafeLine](../labs/web/14-waf-safeline/README.md) исходные задания используют клон базовой Debian 12: локальная `Debian-12-Gold_2` есть в `VirtualBox VMs`, а `debian-12.11.0-amd64-netinst.iso` (670 МиБ) — установщик для создания новой машины. Для [4.1 Burp Suite](../labs/web/01-burp-http/README.md) исходное задание использует Docker-образ Directus; отдельного OVA в `Downloads` нет.

`Debian-Practice-json-xml.ova` относится по названию к теории JSON/XML, а не к одному из практических веб-кейсов. В каталоге Kali Linux в `Downloads` есть файл `.vbox`, но нет диска, поэтому он не считается готовым образом ВМ.
