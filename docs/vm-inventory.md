[← Подготовка среды](lab-environment.md)

# Локальные виртуальные машины для сетевых кейсов

Этот перечень составлен по папке `VirtualBox VMs` 14 ноября 2026 года. Связь с кейсами определена по именам машин; перед повторением работы нужно проверить конфигурацию и состояние каждой ВМ в VirtualBox. Диски не размещены в репозитории.

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
