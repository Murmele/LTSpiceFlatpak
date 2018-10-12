# LTSpiceFlatpak

Flatpak manifest for the LTSpice App.

http://www.analog.com/en/design-center/design-tools-and-calculators/ltspice-simulator.html

## Installation

### Platform and Sdk
    flatpak remote-add --if-not-exists winepak https://dl.winepak.org/repo/winepak.flatpakrepo
	flatpak install winepak org.winepak.Platform/i386/3.0
	flatpak install winepak org.winepak.Sdk/i386/3.0

### Happy Foto
    flatpak-builder --repo=LTSpiceRepo --force-clean LTSpice com.analog.ltspice-simulator.yml
	flatpak remote-add LTSpiceRepo LTSpiceRepo --no-gpg-verify
	flatpak install LTSpiceRepo com.analog.ltspice-simulator
