# Config files for Dell Latitude E7440

I use a Dell Latitude E7440 laptop for a low-power Proxmox home server with the
bonus that it has a built-in battery backup. This is only meant to simplify
administration and make configuration repeatable.

A `.deb` file is available as a [release](https://github.com/curtistinkers/acpid-config-dell-latitude-e7440/releases)
for your convenience.

## Output of `acpi_listen`

For a complete list of outputs for the buttons, function keys, and lid actions,
see the [acpid-output.md](acpid-output.md) file.

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
