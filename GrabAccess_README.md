# GrabAccess -- Advanced UEFI WPBT Bootkit \| Windows Login Password Bypass Tool (2025)

Bypass Windows login password with physical access --- execute commands
as SYSTEM, reset passwords, implant persistent backdoors, and achieve
hardware-level persistence even after OS reinstall or hard drive
replacement.

------------------------------------------------------------------------

## Key Features

-   **Instant Windows Login Bypass**
    -   Boot from USB and gain System privileges without knowing the
        password.
    -   Works on Windows 10 & Windows 11 (TPM, Microsoft accounts, PIN,
        local accounts).
-   **Automated Payload Implantation**
    -   Deploy any program (`payload.exe`) and add it to Windows startup
        automatically.
-   **True Hardware Persistence (Bootkit)**
    -   Embed into UEFI firmware using WPBT.
    -   Survives OS reinstall, formatting, and drive replacement.
-   **No Kernel Patching**
    -   Uses legitimate WPBT mechanism instead of patching the kernel.

------------------------------------------------------------------------

## Quick Start: Bypass Windows Login Password

1.  Prepare a USB drive (FAT32 or FAT16).
2.  Download and extract `GrabAccess_Release.zip` to the USB root.
3.  Insert USB → Reboot → Enter BIOS.
4.  Set USB as first boot device.
5.  Disable Secure Boot if enabled.
6.  Boot from USB.

**Result:** - CMD opens with SYSTEM privileges. - Reset password or
execute commands.

------------------------------------------------------------------------

## Automated Payload Implantation

1.  Place your executable in USB root as `payload.exe`.
2.  Run `build.bat`.
3.  Boot using USB.

**Result:** - Payload installs to:
`C:\Windows\System32\GrabAccess.exe` - Runs automatically on startup.

------------------------------------------------------------------------

## Hardware-Level Bootkit (Advanced)

⚠️ Warning: Can damage your motherboard.

Steps: 1. Extract UEFI firmware. 2. Open with UEFITool. 3. Insert
required modules. 4. Replace raw section with payload. 5. Flash modified
firmware.

------------------------------------------------------------------------

## How It Works

-   Uses **Windows Platform Binary Table (WPBT)**

### Stage 1 (UEFI)

-   Injects WPBT into ACPI tables.

### Stage 2 (Native NT)

-   Runs before login.
-   Deploys payload and persistence.

------------------------------------------------------------------------

## Supported Systems

-   Windows 10 (1803+)
-   Windows 11
-   x64 UEFI systems only

------------------------------------------------------------------------

## Limitations

-   Does NOT bypass Secure Boot
-   Requires physical access

------------------------------------------------------------------------

## SEO Notes

-   Primary keyword: Windows login password bypass
-   Secondary: UEFI bootkit, WPBT bootkit, persistent bootkit
