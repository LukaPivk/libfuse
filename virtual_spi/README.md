# This example only implements some IOCTLs. 

This is a good staring point to implement virutal SPI driver.

## How to build me

To build spidev_test use 
```
gcc spidev_test.c -o spidev_test
```

To build spidev use

```
gcc spidev.c -Wall `pkg-config fuse3 --cflags --libs`   -o spidev
```


## How to use

make folder for mount point for example
```
sudo /dev/spi3
```
start 
```
sudo ./spidev /dev/spi3
```

Now you can use spidev_test to setting speed. 

```
sudo ./spidev_test -D /dev/spi3/fioc -s 341  
```

