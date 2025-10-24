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
|1| NTLM LPE| not working| to repeat with bettercap?|
