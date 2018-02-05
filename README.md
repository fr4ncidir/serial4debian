# serial4debian

This repository contain a library useful to quickly communicate over serial port with your external device with C language.

The functions are largely documented.

Here following, a simple example on how to use it.

```C
SerialOptions so;
// your declarations...

// serial opening
so.baudRate = B115200;
so.dataBits = CS8;
so.parityBit = NO_PARITY;
so.stopbits = ONE_STOP;
if (open_serial(usb_address,&so) == ERROR) return EXIT_FAILURE;
// serial opening end

// your software...

close(so.serial_fd);
```