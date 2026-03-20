# am335x-sysboot-decoder
Simple JavaScript decoder for TI AM335x SYSBOOT register.

## Usage

Open [the decoder page](https://jcormier.github.io/am335x-sysboot-decoder/) and enter the value
of the AM335x `CONTROL_STATUS` register (address `0x44E10040`) to decode the SYSBOOT configuration.

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
