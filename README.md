# Composite led-strip driver for Zephyr

This modularises the excellent work done by Xingrz in https://github.com/zmkfirmware/zmk/pull/1433 and brings it up to date for Zephyr 3.5

to use just instantiate in the top level devicetree node

```
led_strip: led-strip-composite {
        compatible = "zmk,led-strip-composite";
        chain-length = <82>;
        strip-0 {
            led-strip = <&led_strip_0>;
        };
        strip-1 {
            led-strip = <&led_strip_1>;
        };
    };

```