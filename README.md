# Amstrad_PPC_XT_CF_Lite
Internal CF interface for the Amstrad PPC512/640

Replaces the internal modem board with a combination ISA interface & XT-IDE/Compact Flash interface.<br> 

Heavily based on Sergey Kiselev's design<br>
[Github page](https://github.com/skiselev)<br>
[WWW page](http://www.malinov.com/Home/sergeys-projects/xt-cf-lite)<br>

Which is apparently a remake of James Pearce's card:<br>
[WWW page](http://www.lo-tech.co.uk/wiki/XT-CF-lite)<br>

I am using some of Sergey's Kicad symbols/footprints:<br>
[Sergey's Kicad symbols](https://github.com/skiselev/my_kicad_library)<br>

Changes requires for internal mounting in the Amstrad PPC:<br>
[1] The following signals are generated directly from the internal gate arrays and should be buffered with a non-inverting buffer (i.e. 72HC244): A00 to A07, !MEMW, !MEMR, !IOW, !IOR, RESET<br>
_(there are others but irrelevant for our purposes)_<br>
[2] The data signals (D0 to D7) are at CMOS levels and should be pulled up to TTL levels with 10KΩ resistors<br>
[3] The internal modem board we are replacing is roughly 200x120mm<br>
[4] Technically the PPC should be powered by the "expansion unit" and not the other way around ... don't tell anyone<br>

Currently untested ...<br><br>
![Amstrad_PPC_Internal_Modem](Amstrad_PPC_Internal_modem.jpg)
![Amstrad_PPC_Internal_CF_Lite](Amstrad_PPC_Internal_PCB.png)
