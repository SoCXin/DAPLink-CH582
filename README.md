# [DAPLink-CH582](https://github.com/SoCXin/DAPLink-CH582)

[CMSIS-DAP](https://github.com/OS-Q/DAPLink) compliant debugger based on Ch582F [￥4.3 QFN28(4x4mm)](https://item.szlcsc.com/3483855.html)


## Features

- [x] Connected & Running LED
- [x] CMSIS-DAP V2.1
- [x] SWD
- [x] UART
- [ ] JTAG
- [ ] USB Host
- [ ] BLE

## Usage

| Function | Label | GPIO |
|:-|:-:|:-:|
| JTAG_TDI | TDI | A0 |
| JTAG_TDO | TDO | A1 |
| JTAG_TMS | TMS  | A2 |
| JTAG_TCK | TCK  | A15 |
| SWD_SWDIO | TMS | A2 |
| SWD_SWCLK | TCK | A15 |
| nRESET | RTS | A4 |
| UART TX | TX | B7 |
| UART RX | RX | B4 |

Notice that 3.3V level I/O is required.


## Dependent

* [CherryUSB-Daplink](https://github.com/OS-Q/CherryUSB-Daplink)
    * [CherryUSB](https://github.com/OS-Q/CherryUSB)


```
git submodule update --init --recursive
```

IDE:[MounRiver Studio](http://mounriver.com/download)

```
Memory region         Used Size  Region Size  %age Used
           FLASH:       27396 B       448 KB      5.97%
             RAM:        6292 B        32 KB     19.20%
   text	   data	    bss	    dec	    hex	filename
  27224	    172	   2252	  29648	   73d0	DAPLink-CH582.elf
```


TODO:
* base on RTOS
* base on PlatformIO


```
./CherryUSB-Daplink/src/winusb.c:82:29: warning: initialization of 'const uint8_t **' {aka 'const unsigned char **'} from incompatible pointer type 'const uint8_t (*)[142]' {aka 'const unsigned char (*)[142]'} [-Wincompatible-pointer-types]
         .comp_id_property = &WINUSB_IF0_WCIDProperties,
```
