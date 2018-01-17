# PackerAttacker

## Description

The Packer Attacker is a generic unpacker for Windows malware. It supports the following types of packers:

1. Running from heap
2. Replacing PE header
3. Injecting in a process using WriteProcessMemory/NtWriteVirtualMemory
4. Process Doppelganging

The Packer Attacker is based on Microsoft Detours.

## Compilation

Compile with Visual Studio 2017 and Detours library. You'll have two files:

1. PackerAttackerHook.dll - unpacking engine
2. PackerAttacker.exe - DLL injector that executes malware and injects PackerAttackerHook.dll

Make sure your detours library file is the same version as in the header.

## Setting up

1. Create folder C:\dumps - all the extracted hidden code will be saved there
2. Put PackerAttacker.exe and PackerAttackerHook.dll to %PATH%

## Usage

PackerAttacker.exe <malware.exe>

## Misc

Currently only PE EXE files are supported.

## Credits

BromiumLabs for the original PackerAttacker.
