# Output of `acpi_listen`

Below is the output of `acpi_listen` for various buttons, function keys, mains power, and lid actions.

## Brightness control

### Brightness down function key

```sh
video/brightnessdown BRTDN 00000087 00000000
wmi PNP0C14:00 000000d0 00000000
```

### Brightness up function key

```sh
video/brightnessup BRTUP 00000086 00000000
wmi PNP0C14:00 000000d0 00000000
```

### Keyboard brightness function key

```sh
wmi PNP0C14:00 000000d0 00000000
```

## Lid actions

### Lid close

```sh
button/lid LID close
```

### Lid open

```sh
button/lid LID open
```

## Power & sleep control

### Power button

```sh
button/power PBTN 00000080 00000000
```

### Sleep function key

```sh
button/sleep SBTN 00000080 00000000
button/sleep PNP0C0E:00 00000080 00000001
```

### Mains power removed

```sh
ac_adapter ACPI0003:00 00000080 00000000
processor LNXCPU:00 00000081 00000000
processor LNXCPU:01 00000081 00000000
processor LNXCPU:02 00000081 00000000
processor LNXCPU:03 00000081 00000000
battery PNP0C0A:00 00000080 00000001
```

### Mains power restored

```sh
ac_adapter ACPI0003:00 00000080 00000001
processor LNXCPU:00 00000081 00000000
processor LNXCPU:01 00000081 00000000
processor LNXCPU:02 00000081 00000000
processor LNXCPU:03 00000081 00000000
battery PNP0C0A:00 00000080 00000001
```

## Volume control

### Mute button

```sh
button/mute MUTE 00000080 00000000 K
```

### Volume up button

```sh
button/volumedown VOLDN 00000080 00000000 K
```

### Volume down button

```sh
button/volumeup VOLUP 00000080 00000000 K
```

## Media controls

### Previous function key

```sh
cd/prev CDPREV 00000080 00000000 K
```

### Play/pause function key

```sh
cd/play CDPLAY 00000080 00000000 K
```

### Next function key

```sh
cd/next CDNEXT 00000080 00000000 K
```