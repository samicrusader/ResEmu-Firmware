# ResEmu-X Modchip Images

This is a collection of files for ResEmu-X that allow it to emulate a Xecuter X3 modchip.

## X3 files

[x3_flashrom.bin](x3_flashrom.bin): FlashROM banks 1-4 = 1x1 MB X3.3294 BIOS

x3_flashrom.bin: FlashROM banks 4-8 = 4x256KB FlashBIOS v3.0.3

[x3_eeprom.bin](x3_eeprom.bin)>: Chip EEPROM file is empty

[flashbios_v303.bin](flashbios_v303.bin): FlashBIOS v3.0.3 IS your recovery BIOS

Use with MCPX v1.0 or v1.1 ROM + standard issue Xbox BIOS + system 256-byte EEPROM file

## Modified X2 5035 for QEMU (set as non-modchip Flash ROM)

Patched Xecuter2 5035 BIOS for use with xemu & Insignia

[x2_5035_vOld_512k.\(xblive\).\(cdbpatch\).\(Force480p\).bin](x2_5035_vOld_512k.(xblive).(cdbpatch).(Force480p).bin)

- Force480p applied
- LBA48 (137gb) not applied (see [`lba48.txt`](lba48.txt) if need be)
- Xbox Live connectivity force-allowed (unblocked, x2config option is broken)
- Ignores `READ DVD STRUCTURE` failure (allows mounted ISOs to be read with xemu's very basic DVD drive emulation)
- Patches the allowed media boot type (what the XBE can be boot from) option to allow all media (again, xemu doesn't emulate a full fucking Xbox drive)

Works with v1.0/v1.1 MCPX boot rom & EEPROM set to console revision 1.1+

