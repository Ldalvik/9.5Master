# Mode 31 (Routine Control)

| Command | Name | Source | Header | Payload | Request bytes | Response layout | Response bytes | SecurityAccess mode | Field source | Field name | Field ID | Offset / bit | Mask | Parse / decode |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 31/0201 | verified monitor routine; partial semantics | L640 | 31 CONTROL 02 01 | — | 4 | 71 CONTROL 02 01 | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/0202 | verified application branch; subsystem TBD | L640 | 31 CONTROL 02 02 | — | 4 | 71 CONTROL 02 02 | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/0203 | state only; no application consumer | L640 | 31 CONTROL 02 03 | — | 4 | 71 CONTROL 02 03 | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/0204 | state only; no application consumer | L640 | 31 CONTROL 02 04 | — | 4 | 71 CONTROL 02 04 | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/0205 | verified monitor routine | L640 | 31 CONTROL 02 05 | — | 4 | 71 CONTROL 02 05 | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/0207 | FI_RZ_OFFSET_CAL | HDS only | 31 02 07 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 31/0208 | FI_STARTER_CRANK_CTRL | HDS only | 31 02 08 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 31/020A | FI_ENG_MOTOR_MODE_REQ | HDS only | 31 02 0A | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 31/020C | state only; no application consumer | L640 | 31 CONTROL 02 0C | — | 4 | 71 CONTROL 02 0C | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/020D | empty body; response/effect TBD | L640 | 31 CONTROL 02 0D | — | 4 | 71 CONTROL 02 0D | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/020E | verified routine-status advertisement; actuator effect not proven | L640 | 31 CONTROL 02 0E | — | 4 | 71 CONTROL 02 0E | 4 | 41/42 | — | — | — | — | — | — |
| 31/0211 | verified application branch; subsystem TBD | L640 | 31 CONTROL 02 11 | — | 4 | 71 CONTROL 02 11 | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/0212 | state only; no application consumer | L640 | 31 CONTROL 02 12 | — | 4 | 71 CONTROL 02 12 | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/0213 | verified monitor/application-state routine; exact subsystem TBD | L640 | 31 CONTROL 02 13 | — | 4 | 71 CONTROL 02 13 | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/021B | pending snapshot staging; final persistence TBD | L640 | 31 CONTROL 02 1B | — | 4 | 71 CONTROL 02 1B | 4 | 05/06 | — | — | — | — | — | — |
| 31/021C | state only; no application consumer | L640 | 31 CONTROL 02 1C | — | 4 | 71 CONTROL 02 1C | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/111A | verified inline diagnostic state; HDS AT_CANCEL_DIFF_GEAR_PROT wrapper | L640 | 31 CONTROL 11 1A | — | 4 | 71 CONTROL 11 1A | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/1145 | recognized but NOT_APPLICABLE in exact stock L640; HDS CVT_OIL_PRES_LEARN wrapper | L640 | 31 CONTROL 11 45 | — | 4 | 71 CONTROL 11 45 | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/1146 | recognized but NOT_APPLICABLE in exact stock L640 | L640 | 31 CONTROL 11 46 | — | 4 | 71 CONTROL 11 46 | 4 | 41/42 | — | — | — | — | — | — |
| 31/1147 | verified inline diagnostic state; no HDS selector join | L640 | 31 CONTROL 11 47 | — | 4 | 71 CONTROL 11 47 | 4 | 41/42 | — | — | — | — | — | — |
| 31/1148 | recognized but NOT_APPLICABLE in exact stock L640; HDS definition only | L640 | 31 CONTROL 11 48 | — | 4 | 71 CONTROL 11 48 | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/1149 | recognized but NOT_APPLICABLE in exact stock L640; HDS CVT_ACCEL_LEARN_TYPE2 wrapper | L640 | 31 CONTROL 11 49 | — | 4 | 71 CONTROL 11 49 | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/114A | recognized but NOT_APPLICABLE in exact stock L640; HDS CVT_ACCEL_CORR_LEARN_TYPE1 wrapper | L640 | 31 CONTROL 11 4A | — | 4 | 71 CONTROL 11 4A | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/114B | recognized but NOT_APPLICABLE in exact stock L640; HDS CVT_ACCEL_CORR_LEARN_TYPE2 wrapper | L640 | 31 CONTROL 11 4B | — | 4 | 71 CONTROL 11 4B | 4 | None in recovered handler | — | — | — | — | — | — |
| 31/114C | recognized but NOT_APPLICABLE in exact stock L640 | L640 | 31 CONTROL 11 4C | — | 4 | 71 CONTROL 11 4C | 4 | 41/42 | — | — | — | — | — | — |
| 31/1152 | verified inline diagnostic state; no HDS selector join | L640 | 31 CONTROL 11 52 | — | 4 | 71 CONTROL 11 52 | 4 | 41/42 | — | — | — | — | — | — |
| 31/3F00 | E81E-configured diagnostic routine; no application consumer | L640 | 31 CONTROL 3F 00 | — | 4 | 71 CONTROL 3F 00 | 4 | 05/06 | — | — | — | — | — | — |
