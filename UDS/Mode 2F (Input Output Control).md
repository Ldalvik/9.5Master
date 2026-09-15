# Mode 2F (Input Output Control)

| Command | Name | Source | Header | Payload | Request bytes | Response layout | Response bytes | SecurityAccess mode | Field source | Field name | Field ID | Offset / bit | Mask | Parse / decode |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 2F/0101 | FI_RACV_CLOSE | HDS only | 2F 01 01 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2F/0102 | accepted diagnostic state only; no physical effect proven | L640 | 2F 01 02 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 02 STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/0110 | accepted diagnostic storage with readback only | L640 | 2F 01 10 | 00 / 03 VALUE_HI VALUE_LO | 4 | [PROVEN] Response/status nuance: wire-status construction is handler-specific; a positive response alone does not prove that application state is installed | UNKNOWN | None in recovered handler | — | — | — | — | — | — |
| 2F/0111 | verified monitor-state effect; exact monitor identity TBD | L640 | 2F 01 11 | 00 / 03 VALUE_HI VALUE_LO | 4 | [PROVEN] Response/status nuance: wire-status construction is handler-specific; a positive response alone does not prove that application state is installed | UNKNOWN | None in recovered handler | — | — | — | — | — | — |
| 2F/0112 | accepted diagnostic storage with readback only | L640 | 2F 01 12 | 00 / 03 VALUE_HI VALUE_LO | 4 | [PROVEN] Response/status nuance: wire-status construction is handler-specific; a positive response alone does not prove that application state is installed | UNKNOWN | None in recovered handler | — | — | — | — | — | — |
| 2F/0113 | accepted diagnostic storage with readback only | L640 | 2F 01 13 | 00 / 03 VALUE_HI VALUE_LO | 4 | [PROVEN] Response/status nuance: wire-status construction is handler-specific; a positive response alone does not prove that application state is installed | UNKNOWN | None in recovered handler | — | — | — | — | — | — |
| 2F/0114 | accepted diagnostic storage/readback; no physical effect proven | L640 | 2F 01 14 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 14 STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/0116 | verified monitor-state effect; exact monitor identity TBD | L640 | 2F 01 16 | 00 / 03 VALUE_HI VALUE_LO | 4 | [PROVEN] Response/status nuance: wire-status construction is handler-specific; a positive response alone does not prove that application state is installed | UNKNOWN | None in recovered handler | — | — | — | — | — | — |
| 2F/0119 | accepted diagnostic storage with readback only | L640 | 2F 01 19 | 00 / 03 VALUE_HI VALUE_LO | 4 | [PROVEN] Response/status nuance: wire-status construction is handler-specific; a positive response alone does not prove that application state is installed | UNKNOWN | None in recovered handler | — | — | — | — | — | — |
| 2F/011A | accepted diagnostic state only; no physical effect proven | L640 | 2F 01 1A | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 1A STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/0132 | accepted shared diagnostic selector; no physical effect proven | L640 | 2F 01 32 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 32 STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/0137 | accepted shared diagnostic selector; no physical effect proven | L640 | 2F 01 37 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 37 STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/0138 | verified monitor-state effect; exact monitor identity TBD | L640 | 2F 01 38 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 38 STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/0139 | accepted shared diagnostic selector; no physical effect proven | L640 | 2F 01 39 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 39 STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/013B | accepted shared diagnostic selector; no physical effect proven | L640 | 2F 01 3B | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 3B STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/013C | accepted shared diagnostic selector; no physical effect proven | L640 | 2F 01 3C | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 3C STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/013D | accepted shared diagnostic selector; no physical effect proven | L640 | 2F 01 3D | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 3D STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/0141 | accepted shared diagnostic selector; no physical effect proven | L640 | 2F 01 41 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 41 STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/0142 | FI_CSS | HDS only | 2F 01 42 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2F/0144 | FI_VFP | HDS only | 2F 01 44 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2F/0146 | FI_WGS | HDS only | 2F 01 46 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2F/0147 | FI_ABV | HDS only | 2F 01 47 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2F/0148 | accepted shared diagnostic selector; no physical effect proven | L640 | 2F 01 48 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 48 STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/0149 | accepted shared diagnostic selector; no physical effect proven | L640 | 2F 01 49 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 49 STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/014A | accepted shared diagnostic selector; no physical effect proven | L640 | 2F 01 4A | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 4A STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/014B | FI_VCM | HDS only | 2F 01 4B | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2F/014C | FI_ACM | HDS only | 2F 01 4C | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2F/014E | verified ETC mode/inhibit effect; flag names and polarity TBD | L640 | 2F 01 4E | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 4E 03 | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/014F | verified ETC command/request override; physical unit TBD | L640 | 2F 01 4F | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 4F STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/0150 | FI_ACDSD | HDS only | 2F 01 50 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2F/0151 | FI_VFT | HDS only | 2F 01 51 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2F/0152 | FI_FFVSFUEL | HDS only | 2F 01 52 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2F/0153 | recognized helper slot with empty body | L640 | 2F 01 53 | — | 3 | [PROVEN] Body 0x000E7B9A constructs no positive response and no NRC. The eventual wire result after returning to the parent is UNKNOWN; only service-level minimum-format behavior is proved | UNKNOWN | Not applicable; no usable positive operation | — | — | — | — | — | — |
| 2F/0154 | recognized helper slot with empty body | L640 | 2F 01 54 | — | 3 | [PROVEN] Body 0x000E7B9C constructs no positive response and no NRC. The eventual wire result after returning to the parent is UNKNOWN; only service-level minimum-format behavior is proved | UNKNOWN | Not applicable; no usable positive operation | — | — | — | — | — | — |
| 2F/0155 | FI_VCM2 | HDS only | 2F 01 55 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2F/0156 | FI_VCM2SOL | HDS only | 2F 01 56 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2F/0159 | accepted shared diagnostic selector; no physical effect proven | L640 | 2F 01 59 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 59 STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/015D | FI_CNGRLYB | HDS only | 2F 01 5D | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2F/0161 | accepted shared diagnostic selector; no physical effect proven | L640 | 2F 01 61 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 01 61 STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/112C | accepted high internal selector; no physical effect proven | L640 | 2F 11 2C | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 11 2C STATUS | 4 | No SecurityAccess gate identified; handler conditions unresolved | — | — | — | — | — | — |
| 2F/112D | accepted high internal selector; no physical effect proven | L640 | 2F 11 2D | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 11 2D STATUS | 4 | No SecurityAccess gate identified; handler conditions unresolved | — | — | — | — | — | — |
| 2F/112E | accepted high internal selector; no physical effect proven | L640 | 2F 11 2E | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 11 2E STATUS | 4 | No SecurityAccess gate identified; handler conditions unresolved | — | — | — | — | — | — |
| 2F/112F | accepted high internal selector; no physical effect proven | L640 | 2F 11 2F | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 11 2F STATUS | 4 | No SecurityAccess gate identified; handler conditions unresolved | — | — | — | — | — | — |
| 2F/1130 | accepted high internal selector; no physical effect proven | L640 | 2F 11 30 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 11 30 STATUS | 4 | No SecurityAccess gate identified; handler conditions unresolved | — | — | — | — | — | — |
| 2F/1131 | accepted high internal selector; no physical effect proven | L640 | 2F 11 31 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 11 31 STATUS | 4 | No SecurityAccess gate identified; handler conditions unresolved | — | — | — | — | — | — |
| 2F/1132 | recognized negative-only | L640 | 2F 11 32 | 00 / 03 VALUE_HI VALUE_LO | 4 | [PROVEN] none. NRC behavior: 0x31 | UNKNOWN | Not applicable; no usable positive operation | — | — | — | — | — | — |
| 2F/1133 | accepted high internal selector; no physical effect proven | L640 | 2F 11 33 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 11 33 STATUS | 4 | No SecurityAccess gate identified; handler conditions unresolved | — | — | — | — | — | — |
| 2F/1134 | accepted high internal selector; no physical effect proven | L640 | 2F 11 34 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 11 34 STATUS | 4 | No SecurityAccess gate identified; handler conditions unresolved | — | — | — | — | — | — |
| 2F/1135 | accepted high internal selector; no physical effect proven | L640 | 2F 11 35 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 11 35 STATUS | 4 | No SecurityAccess gate identified; handler conditions unresolved | — | — | — | — | — | — |
| 2F/1136 | accepted high internal selector; no physical effect proven | L640 | 2F 11 36 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 11 36 STATUS | 4 | No SecurityAccess gate identified; handler conditions unresolved | — | — | — | — | — | — |
| 2F/1137 | verified volatile four-channel-family current-loop/PWM target override; 0.1-A scaling corroborated; direct-injector-bank hypothesis and exact actuator/unit TBD | L640 | 2F 11 37 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 11 37 STATUS | 4 | None in recovered handler | — | — | — | — | — | — |
| 2F/1138 | accepted high internal selector; no physical effect proven | L640 | 2F 11 38 | 00 / 03 VALUE_HI VALUE_LO | 4 | 6F 11 38 STATUS | 4 | No SecurityAccess gate identified; handler conditions unresolved | — | — | — | — | — | — |
| 2F/1156 | accepted selector only; no physical effect proven | L640 | 2F 11 56 | 00 / 03 VALUE_HI VALUE_LO | 4 | [PROVEN] 0x6F then 11 56 then status byte. NRC behavior: 0x13,0x31,0x7F | UNKNOWN | None in recovered handler | — | — | — | — | — | — |
