# NeoPDF

NeoPDF is a Windows x64 PDF reader, editor, and smart print-pricing calculator.

## Supported build profiles

- **Legacy x64:** Windows 7 SP1 target (Python 3.8 x64 profile; requires real Windows 7 testing).
- **Modern x64:** Windows 8.1, Windows 10, and Windows 11 target (Python 3.11 x64 profile).

Windows 8 (non-8.1) is not currently included in the Modern compatibility claim.

## Build outputs

The project is intended to produce:
- `NeoPDF-Legacy-x64.exe`
- `NeoPDF-x64.exe`
- `Setup_NeoPDF_Legacy_Win7_x64.exe`
- `Setup_NeoPDF_Win8-11_x64.exe`

The application EXE bundles Python and its application dependencies. Users should not need to install Python separately. Windows printer drivers are still provided by Windows or the printer manufacturer.

## Important status

This repository is being initialized. The full NeoPDF source package and the Windows build workflow need to be added before Actions can compile the EXE. A workflow run is not proof of Windows 7 compatibility; test on clean Windows 7 SP1 x64, Windows 8.1, Windows 10, and Windows 11 machines before publishing.

## Project limitations to verify

- CMYK ink/coverage classification is an estimate, not a physical toner measurement.
- Text replacement currently uses a redaction-and-overlay approach, not native in-place PDF text editing.
- Installer signing and printer-driver compatibility require separate release testing.
