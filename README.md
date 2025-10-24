# GAMES
different tests and simulations

TESTs tests and flags
---------------------------
* Detect shellcode that loads DLL with socket API after process creation
* Penetration framework or shellcode was detected
* Changed protection type of library in a remote process space
* Indirect command was executed
* The executable has section names not typically seen in standard compilers
* The executable uses APIs related to debugging, which could indicate anti-debugging or self-analysis. (LoadLibrary)
* File can delay its execution (Sleep)
* File can create a reverse shell. (include <winsock2.h>)
* File can retrieve thread local storage values (Thread)
* File can allocate memory (VirtualAlloc)
* File can create processes on Windows (CreateProcess, OpenProcess)
* File can write\read to files on Windows (fopen)
* File can write to a pipe for inter-process communication (CreateNamedPipe)
* This binary was packed with UPX

GAMES
---------------------------
|#| GAME| Notes| TODO|
|---| --------------------------- | -------------------------- |-------------------|
|1| NTLM_LPE_CVE-2025-33073| not working| to repeat with bettercap? new printerbug?|
|2| LNK_CVE-2025-50154| working, but hangs| repeat with smbserver with user\password?|
|3| DLL loading with powerchell| SUPER| hide console, make upload command|
|4| ICMP_SHELL| SUPER| binary is suspicios, improve OPSEC|
|5| EDRfreeze| ??| -|
|6| IPv6 sniff| ??| -|
|7| NTLM_leakage_mslib| ??| -|
|8| Asmloader| ??| -|
|9| Asm loader + polymorph + KrbrelayUp| ? will it trigger binary?| -|




