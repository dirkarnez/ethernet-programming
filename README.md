ethernet-programming
====================
- https://github.com/qemu/qemu/blob/master/hw/net/rtl8139.c
- https://github.com/espressif/esp-idf/blob/master/examples/ethernet/basic/components/ethernet_init/ethernet_init.c#L86
- https://github.com/espressif/esp-idf/blob/master/components/esp_eth/src/phy/esp_eth_phy_rtl8201.c
- https://github.com/espressif/esp-idf/blob/master/components/esp_eth/src/phy/esp_eth_phy_rtl8201.c
- https://github.com/rsta2/circle/blob/master/lib/bcm54213.cpp
- [PHY的MDIO/MDC简介_phy的mdc-CSDN博客](https://blog.csdn.net/linyangspring/article/details/27177277)
- https://www.ti.com/lit/ds/symlink/dp83849c.pdf?ts=1758537606936
- [【驱动】以太网扫盲（二）phy寄存器简介 - 学习，积累，成长 - 博客园](https://www.cnblogs.com/dongxb/p/17365055.html)
- [RTL8201-RMII电路_rtl8201f 参考电路-CSDN博客](https://blog.csdn.net/weixin_42005993/article/details/88563909)
- https://docs.rs-online.com/018c/0900766b80bfd63c.pdf
- [MICROCHIP KSZ8081MNXIA PHY配置详解-CSDN博客](https://blog.csdn.net/qq_44832590/article/details/127102685)
- [rtl8201以太网卡调试【转】 - Sky&Zhang - 博客园](https://www.cnblogs.com/sky-heaven/p/10335510.html)
- [esp-idf/examples/ethernet/basic/components/ethernet_init/Kconfig.projbuild at 5c5eb99eabc7d3e7f704656ffe9ebf8f5a77afbd · espressif/esp-idf](https://github.com/espressif/esp-idf/blob/5c5eb99eabc7d3e7f704656ffe9ebf8f5a77afbd/examples/ethernet/basic/components/ethernet_init/Kconfig.projbuild#L16)
- [以太网 - ESP32 - — ESP-IDF 编程指南 v5.5.1 文档](https://docs.espressif.com/projects/esp-idf/zh_CN/stable/esp32/api-reference/network/esp_eth.html#misc-operation-of-driver)
- [PHY芯片快速深度理解-CSDN博客](https://blog.csdn.net/zhiyuan2021/article/details/125420299)
- [【科普】一文读懂以太网PHY芯片-CSDN博客](https://blog.csdn.net/weixin_43381663/article/details/131874207)
- [ESP-IDF](https://sourcevu.sysprogs.com/espressif/esp-idf/)

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
