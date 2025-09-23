ethernet-programming
====================
- https://github.com/qemu/qemu/blob/master/hw/net/rtl8139.c
- https://github.com/espressif/esp-idf/blob/master/components/esp_eth/src/phy/esp_eth_phy_rtl8201.c
- https://github.com/espressif/esp-idf/blob/master/components/esp_eth/src/phy/esp_eth_phy_rtl8201.c
- https://github.com/rsta2/circle/blob/master/lib/bcm54213.cpp

### Notes
- ethernet IC are more low level then [network interface controller](https://en.wikipedia.org/wiki/Network_interface_controller)

### Table
| Layer                              | Embedded/MCU Example         | Linux/PC Example                   |
|-------------------------------------|------------------------------|-------------------------------------|
| Hardware Mapping                    | Wi-Fi/Ethernet PHY           | NIC, TUN/TAP device                |
| Driver / Vendor-Specific Low-Level code | Vendor C driver, ESP-IDF HAL | Kernel module, TUN/TAP kernel code |
| Network Interface Abstraction       | esp_netif, esp_netif l2 tap, glueing code        | `eth0`, `tap0`, `/dev/net/tun`     |
| TCP/IP Stack                        | lwIP, ESP-IDF                | Kernel stack                       |
| Application Layer Protocols         | HTTP/FTP/MQTT libs           | HTTP/FTP/MQTT libs (on sockets)    |

### Graphs
- [ESP-NETIF - ESP32 - — ESP-IDF Programming Guide v5.5.1 documentation](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/api-reference/network/esp_netif.html#esp-netif-architecture)
- [Linux_kernel_diagram.svg](https://graphviz.org/Gallery/directed/Linux_kernel_diagram.svg)
