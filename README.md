# Config files for Dell Latitude E7440

I use a Dell Latitude E7440 laptop for a low-power Proxmox home server with the
bonus that it has a built-in battery backup. This is only meant to simplify
function key and lid close events in the event I need to reinstall Proxmox (or
any Debian-based distribution).

A `.deb` file is available as a [release](https://github.com/curtistinkers/acpid-config-dell-latitude-e7440/releases)
for convenience.

## Event handling

### Lid switch

The `lid` handler script is called by the `lid_close` and `lid_open` event
files in response to the lid being closed and opened, respectively. On close it
saves the current backlight level to `/run/backlight_level_save` and sets the
turns off the backlight. Upon opening, it sets the backlight to the previously
saved value and removes the save file. If not value is saved, it defaults to
`467` (50% brightness).

### Brightness up/down

The `backlight` handler script is called by the `brightness_up` and
`brightness_down` event files. It steps the brightness in 10% increments.

## Build and install as `.deb` package

Strictly speaking, this is not necessary. You may copy the files into
`/etc/acpi/` if you prefer not to have the files managed by `dpkg`.

```sh
# Clone the repo
git clone https://github.com/curtistinkers/acpid-config-dell-latitude-e7440

# Package it into a .deb
dpkg-deb -b acpid-config-dell-latitude-e7440

# Install the package
dpkg -i acpid-config-dell-latitude-e7440.deb
```

## Output of `acpi_listen`

For a complete list of outputs for the buttons, function keys, and lid actions,
see the [acpid-output.md](acpid-output.md) file.
