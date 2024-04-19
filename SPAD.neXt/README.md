CORE FLIGHT TECHONOLOGIES A320 FCU driver for SPAD SERIAL V2

Special thanks to @1L2P (Discord ID: 1L2P#5598) for his excellent work!

FCU communicates with SPAD.neXt via SerialV2. The Baud Rate is 115200 (default SPAD serial device bitrate)

How to install firmware -> https://github.com/coreflighttech/Uploader


*** R01-008 ***

Special formats to be used in SPAD.neXt
 - Send ' ' spaces strings to clear SPD, HDG, ALT or VS digits
 - SPD mode values are 0 to 999 string formatted integers (###). Use '---' to display dashes.
 - MACH mode value are 0.00 to 9.99 string formatted floats (#.##). Use '---' to display dashes.
 - HDG values are 0 to 999 string formatted integers (###). Use '---' to display dashes.  
 - VS values are -9999 to 9999 string formatted integers (#####). Use '-----' to display dashes.  
 - FPA values are -9.9 to 9.9 string formatted floats (#.# or -#.#). Use '-----' to display dashes.
 - Other chars strings can also be displayed but with well known 8 segments limitations.  

Internal devices features (not designed to be used when connected to SPAD)
 - Turn on/off panel backlight by pressing SPD MACH + METRIC ALT
 - Turn on/off LCD display backlight by pressing SPD MACH + HDG VS TRK FPA
 - Show firmware version references by pressing SPD MACH + EXPED
 - Panel backlight brightness level setting by pressing SPD MACH and turning ALT encoder (Better use DEVICE:1L2P/CFTA320FCU/DISPLAY_BRI var in SPAD when connected, 0 to 255 range)
 - LCD display backlight brightness level setting by pressing SPD MACH and turning VS encoder (Better use DEVICE:1L2P/CFTA320FCU/BACKLIGHT_BRI var in SPAD when connected, 0 to 255 range)
 - Soft reset by pressing SPD MACH + APPR (only use when not connected to SPAD, or just plug/unplug USB cable)

To manage A320 FCU panel digits and backlight brightness from SPAD, search for these variables.
 - DISPLAY_BRI : A320 FCU panel digits brightness from 0 to 255 (DEVICE:1L2P/CFTA320FCU/DISPLAY_BRI)
 - BACKLIGHT_BRI : A320 FCU panel backlight brightness from 0 to 255 (DEVICE:1L2P/CFTA320FCU/BACKLIGHT_BRI)

SPAD complete device test snippet for FlyByWire A32NX is <b>#10242</b> (SPAD 0.9.15.27+)

SPAD complete device for Fenix A320 v2.0.0.392+ <b>#10859</b>

*** History ***
 - r01-003 Initial release
 - r01-005 Backlight variables fix, SPAD GUI and LCD control improvements, Snippet FBW A32NX #10242 updated
 - r01-006 SPAD GUI layout updated, Strings management added, Snippet FBW A32NX #10242 updated
 - r01-007 Cool down LCD display events rate, Snippet FBW A32NX #10242 updated
 - r01-008 Fix Altitude display overflow, Fenix A320 Snippet #10859 added

