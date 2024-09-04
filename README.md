# Pyinstaller-Decomplie

PyInstaller Extractor is a Python script to extract the contents of a PyInstaller generated executable file.

The header of the pyc files are automatically fixed so that a Python bytecode decompiler will recognize it. The script can run on both Python 2.x and 3.x. PyInstaller versions 2.0, 2.1, 3.0, 3.1, 3.2, 3.3, 3.4, 3.5, 3.6, 4.0, 4.1, 4.2, 4.3, 4.4, 4.5, 4.5.1, 4.6, 4.7, 4.8, 4.9, 4.10, 5.0, 5.0.1, 5.1, 5.2, 5.3, 5.4, 5.4.1, 5.5, 5.6, 5.6.1, 5.6.2, 5.7.0, 5.8.0, 5.9.0, 5.10.0, 5.10.1, 5.11.0, 5.12.0, 5.13.0, 5.13.1, 5.13.2, 6.0.0, 6.1.0, 6.2.0, 6.3.0, 6.4.0, 6.5.0, 6.6.0, 6.7.0, 6.8.0, 6.9.0 are tested & supported. Probably will work with other versions too.

## Usage

The script can be run by passing the name of the exe as an argument.

```
$ python Anti-pyinstaller.py <filename>
X:\>python pyinstxtractor.py <filename>
```

It is recommended to run the script in the same version of Python which was used to generate the executable. This is to prevent unmarshalling errors(if any) while extracting the PYZ archive.

## Example

```
X:\> python pyinstxtractor.py test.exe
[+] Processing dist\test.exe
[+] Pyinstaller version: 2.1+
[+] Python version: 36
[+] Length of package: 5612452 bytes
[+] Found 59 files in CArchive
[+] Beginning extraction...please standby
[+] Possible entry point: pyiboot01_bootstrap.pyc
[+] Possible entry point: test.pyc
[+] Found 133 files in PYZ archive
[+] Successfully extracted pyinstaller archive: dist\test.exe

You can now use a python decompiler on the pyc files within the extracted directory
```

After extracting the pyc's you have to use (if you want to get source code) a Python decompiler like [pylingual](https://pylingual.io/).

## License

GNU General Public License v3.0
