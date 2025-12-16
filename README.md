# Exe-Launcher
A GUI for launching exe files when AppLocker's AWL isn't properly setup.

# Disclaimer
This is for ethical+legal authorised use or other legal and ethical educational purposes only. Any misuse of this software will not be the responsibility of the author. 

# Usage
run the hta file, select an exe, and launch it. It's that simple :D (It may not work 100% of the time I haven't tested it on many exe files, but so far I've had a 100% success rate)

# How it works
It uses the ieadvpack.dll lolbin using rundll32. More information on this lolbin can be found here: https://lolbas-project.github.io/lolbas/Libraries/Ieadvpack/

# Remediation
It is usually good practice to block hta files from running as well as mshta.exe altogether, but for the LOLBIN it is reccommended to restrict the execution locations of rundll32 specifically through the denial of exection on user writable paths, as that prevents the targeted exe from loading if it is in any of those user writable paths (which should be the only paths they should be able to put the exe in to begin with). 
