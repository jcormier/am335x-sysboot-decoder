# am335x-sysboot-decoder
Simple JavaScript decoder for TI AM335x SYSBOOT register.

[AM335x TRM Section 9.3.1.4](https://www.ti.com/lit/ug/spruh73q/spruh73q.pdf)

## Usage

Open [the decoder page](https://jcormier.github.io/am335x-sysboot-decoder/) and enter the value
of the AM335x `CONTROL_STATUS` register (address `0x44E10040`) to decode the SYSBOOT configuration.

![AM335x SYSBOOT Decoder screenshot](https://github.com/user-attachments/assets/3c97d5ca-e7a9-472e-8e5b-944ec71b7cbc)

The decoder displays:
- Crystal frequency (SYSBOOT[15:14])
- SYSBOOT[13:12] validity check
- GPMC CS0 address/data muxing mode (SYSBOOT[11:10])
- GPMC CS0 WAIT input usage (SYSBOOT[9])
- GPMC CS0 data bus width (SYSBOOT[8])
- Device type (GP or non-GP)
- EMAC interface type (SYSBOOT[7:6])
- CLKOUT1 state (SYSBOOT[5])
- Boot device sequence (SYSBOOT[4:0])

## URL Sharing & History Navigation

Each decode updates the browser URL with the current register value (e.g. `?regval=0x20000F00`),
making it easy to bookmark or share a specific decode result.

You can also navigate back and forward through previous decodes using the browser's history buttons.

To link directly to a pre-decoded value, append `?regval=<value>` to the URL:

```
https://jcormier.github.io/am335x-sysboot-decoder/?regval=0x20000F00
```
