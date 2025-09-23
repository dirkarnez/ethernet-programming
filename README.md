ethernet-programming
====================
- https://github.com/qemu/qemu/blob/master/hw/net/rtl8139.c
- https://github.com/espressif/esp-idf/blob/master/components/esp_eth/src/phy/esp_eth_phy_rtl8201.c
- https://github.com/espressif/esp-idf/blob/master/components/esp_eth/src/phy/esp_eth_phy_rtl8201.c
- https://github.com/rsta2/circle/blob/master/lib/bcm54213.cpp

### Notes
- ethernet IC are more low level then [network interface controller](https://en.wikipedia.org/wiki/Network_interface_controller)
- hardware mapping -> driver -> virtual io -> tcp/ip interfaces (mixing libraries like `esp_netif` `lwip`, etc) -> network stack (aka some http / ftp / smtp interfaces and libraries)

### Graphs
- [ESP-NETIF - ESP32 - — ESP-IDF Programming Guide v5.5.1 documentation](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/api-reference/network/esp_netif.html#esp-netif-architecture)
- [Linux_kernel_diagram.svg](https://graphviz.org/Gallery/directed/Linux_kernel_diagram.svg)
