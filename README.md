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

Obfuscation flow
---------------------------
manual: https://g3tsyst3m.com/shellcode/pic/Let's-Create-Some-Polymorphic-PIC-Shellcode!/
tools: SuperNova, Polaris-Obfuscator

manual steps (creating polimorph + asm + random)
* compile exe
* cut bin with Infaltive Loader
* place shellcode into asm loader\runner
* The Assembly Code Scrambler - Polymorphic prep part 1 - asmobfuscator.py: python asm_obfuscator.py input.asm
* compile this using nasm to get our .obj file: nasm -fwin64 locate_kernel32_mod.asm
* extract the shellcode from the compiled assembly .obj file using python helper
* encode it to add more layers of polymorphism to our code - Bitwise NOT (python) key will be in the encoded shellcode itself! - We need to note positions so to use on the next phase in the decoder
* place into asm x64 decoder: Just pick one of the index locations the script discovered as your decoding key and apply it to our .asm file below
* Part III - Adding in the Alphanumeric / mix Component to our Shellcode. go ahead and copy and paste that shellcode somewhere
* Place into C runner or whatever place
* test on ANYRUN






