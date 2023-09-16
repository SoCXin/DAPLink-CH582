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
           FLASH:       28056 B       448 KB      6.12%
             RAM:        6944 B        32 KB     21.19%
   text	   data	    bss	    dec	    hex	filename
  27888	    168	   2256	  30312	   7668	DAPLink-CH582.elf

```


