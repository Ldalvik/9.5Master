# Mode 22 (Read DID)

| Command | Name | Source | Header | Payload | Request bytes | Response layout | Response bytes | SecurityAccess mode | Field source | Field name | Field ID | Offset / bit | Mask | Parse / decode |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 22/2300 | Firmware data record 2300 | L640 | 22 23 00 | — | 3 | 62 23 00 + D[0..35] | 39 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d00..d03 | — | D[0..3] | — | 4 ; ROM[0x0003F64D..0x0003F650] = 9E 7F FF 60 [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d04 | 0xFFF94E3A | D[4] | — | 1 ; U8[0xFFF94E3A] [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d05 | — | D[5] | — | 1 ; 00 [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d06 | 0xFFF93EE8 | D[6] | — | 1 ; high byte of U16[0xFFF93EE8] [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d07..d08 | 0xFFF912A0, 0xFFF959E2 | D[7..8] | — | 2 ; 0xFFF959E2==0 ? BE16(U16[0xFFF912A0]) : FF FF [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d09..d10 | 0xFFF93F98 | D[9..10] | — | 2 ; BE16(U16[0xFFF93F98] >> 2) [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d11..d12 | 0xFFF9409A | D[11..12] | — | 2 ; BE16(U16[0xFFF9409A] >> 2) [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d13 | 0xFFF94C6E | D[13] | — | 1 ; U8[0xFFF94C6E] [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d14 | 0xFFF8F72E | D[14] | — | 1 ; sat_u8(trunc_toward_zero(S16[0xFFF8F72E]/16)) [PROVEN transform] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d15 | 0xFFF8F730 | D[15] | — | 1 ; low8(trunc_toward_zero(S16[0xFFF8F730]/4)) [PROVEN transform] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d16 | 0xFFF92AFC | D[16] | — | 1 ; sat_u8(trunc_toward_zero(S16[0xFFF92AFC]/100)) [PROVEN transform] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d17 | 0xFFF91060 | D[17] | — | 1 ; low8(trunc_toward_zero(S16[0xFFF91060]/4)) [PROVEN transform] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d18 | 0xFFF91066 | D[18] | — | 1 ; low8(trunc_toward_zero(S16[0xFFF91066]/4)) [PROVEN transform] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d19 | 0xFFF8F710 | D[19] | — | 1 ; low8(trunc_toward_zero(S16[0xFFF8F710]/4)) [PROVEN transform] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d20 | 0xFFF94A53 | D[20] | — | 1 ; U8[0xFFF94A53] [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d21 | 0xFFF8F6FE | D[21] | — | 1 ; low8(trunc_toward_zero(S16[0xFFF8F6FE]/4)) [PROVEN transform] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d22 | 0xFFF94A18 | D[22] | — | 1 ; U8[0xFFF94A18] [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d23 | 0xFFF8F6FA | D[23] | — | 1 ; low8(trunc_toward_zero(S16[0xFFF8F6FA]/4)) [PROVEN transform] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d24 | 0xFFF94A08 | D[24] | — | 1 ; U8[0xFFF94A08] [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d25 | 0xFFF8F708 | D[25] | — | 1 ; low8(trunc_toward_zero(S16[0xFFF8F708]/4)) [PROVEN transform] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d26 | 0xFFF8F70A | D[26] | — | 1 ; sat_u8(trunc_toward_zero(S16[0xFFF8F70A]/10)+40) [PROVEN transform] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d27 | 0xFFF91818 | D[27] | — | 1 ; sat_u8(trunc_toward_zero(S16[0xFFF91818]/40)) [PROVEN transform] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d28 | — | D[28] | — | 1 ; 00 [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d29 | 0xFFF8F70C | D[29] | — | 1 ; low8(trunc_toward_zero(S16[0xFFF8F70C]/4)) [PROVEN transform] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d30 | 0xFFF94A3A | D[30] | — | 1 ; U8[0xFFF94A3A] [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d31..d32 | 0xFFF913F4 | D[31..32] | — | 2 ; BE16(U16[0xFFF913F4] >> 2) [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d33..d35 | — | D[33..35] | — | 3 ; 00 00 00 [PROVEN] |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware | CVTF Temperature | — | 26 | — | degC = D[offset] - 40 |
| 22/2301 | CVTF Temperature; CVTF Temp Sensor (V) | L640 | 22 23 01 | — | 3 | 62 23 01 + D[0..35] | 39 when appended | None in recovered handler | Firmware | CVTF Temp Sensor (V) | — | 25 | — | V = D[offset] * 0.019600000232458115 |
| 22/2311 | Firmware data record 2311 | L640 | 22 23 11 | — | 3 | 62 23 11 + D[0..35] | 39 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/2320 | CVT solenoid command/actual-current data list; five exact HDS pairs at data8..17 | L640 | 22 23 20 | — | 3 | 62 23 20 + D[0..35] | 39 when appended | None in recovered handler | Firmware | Drive Pulley Sol Command | — | 8 | — | raw = D[8]; wire encoder: sat_u8(floor(u16(raw)/100)) |
| 22/2320 | CVT solenoid command/actual-current data list; five exact HDS pairs at data8..17 | L640 | 22 23 20 | — | 3 | 62 23 20 + D[0..35] | 39 when appended | None in recovered handler | Firmware | Drive Pulley Sol Actual | — | 9 | — | raw = D[9]; wire encoder: sat_u8(floor(u16(raw)/100)) |
| 22/2320 | CVT solenoid command/actual-current data list; five exact HDS pairs at data8..17 | L640 | 22 23 20 | — | 3 | 62 23 20 + D[0..35] | 39 when appended | None in recovered handler | Firmware | Driven Pulley Sol Command | — | 10 | — | raw = D[10]; wire encoder: sat_u8(floor(u16(raw)/100)) |
| 22/2320 | CVT solenoid command/actual-current data list; five exact HDS pairs at data8..17 | L640 | 22 23 20 | — | 3 | 62 23 20 + D[0..35] | 39 when appended | None in recovered handler | Firmware | Driven Pulley Sol Actual | — | 11 | — | raw = D[11]; wire encoder: sat_u8(floor(u16(raw)/100)) |
| 22/2320 | CVT solenoid command/actual-current data list; five exact HDS pairs at data8..17 | L640 | 22 23 20 | — | 3 | 62 23 20 + D[0..35] | 39 when appended | None in recovered handler | Firmware | Start Clutch Control Sol Command | — | 12 | — | raw = D[12]; wire encoder: sat_u8(floor(u16(raw)/100)) |
| 22/2320 | CVT solenoid command/actual-current data list; five exact HDS pairs at data8..17 | L640 | 22 23 20 | — | 3 | 62 23 20 + D[0..35] | 39 when appended | None in recovered handler | Firmware | Start Clutch Control Sol Actual | — | 13 | — | raw = D[13]; wire encoder: sat_u8(floor(u16(raw)/100)) |
| 22/2320 | CVT solenoid command/actual-current data list; five exact HDS pairs at data8..17 | L640 | 22 23 20 | — | 3 | 62 23 20 + D[0..35] | 39 when appended | None in recovered handler | Firmware | Pressure Control Sol Command | — | 14 | — | raw = D[14]; wire encoder: sat_u8(floor(u16(raw)/100)) |
| 22/2320 | CVT solenoid command/actual-current data list; five exact HDS pairs at data8..17 | L640 | 22 23 20 | — | 3 | 62 23 20 + D[0..35] | 39 when appended | None in recovered handler | Firmware | Pressure Control Sol Actual | — | 15 | — | raw = D[15]; wire encoder: sat_u8(floor(u16(raw)/100)) |
| 22/2320 | CVT solenoid command/actual-current data list; five exact HDS pairs at data8..17 | L640 | 22 23 20 | — | 3 | 62 23 20 + D[0..35] | 39 when appended | None in recovered handler | Firmware | LCC Linear Sol Command | — | 16 | — | raw = D[16]; wire encoder: sat_u8(floor(u16(raw)/100)) |
| 22/2320 | CVT solenoid command/actual-current data list; five exact HDS pairs at data8..17 | L640 | 22 23 20 | — | 3 | 62 23 20 + D[0..35] | 39 when appended | None in recovered handler | Firmware | LCC Linear Sol Actual | — | 17 | — | raw = D[17]; wire encoder: sat_u8(floor(u16(raw)/100)) |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | A/T D Switch | — | 5 | — | value = (D[5] & 0X10) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | A/T L Switch | — | 5 | — | value = (D[5] & 0X04) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | A/T N Switch | — | 5 | — | value = (D[5] & 0X20) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | A/T P Switch | — | 5 | — | value = (D[5] & 0X80) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | A/T R Switch | — | 5 | — | value = (D[5] & 0X40) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | A/T S Switch | — | 5 | — | value = (D[5] & 0X08) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | ECON Mode Indicator | — | 15 | — | value = (D[15] & 0X40) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | Sport Mode Indicator | — | 15 | — | value = (D[15] & 0X80) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | Manual Mode Indicator | — | 23 | — | value = (D[23] & 0X80) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | LED A | — | 23 | — | value = (D[23] & 0X40) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | LED B | — | 23 | — | value = (D[23] & 0X20) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | LED C | — | 23 | — | value = (D[23] & 0X10) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | P Indicator | — | 13 | — | value = (D[13] & 0X80) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | R Indicator | — | 13 | — | value = (D[13] & 0X40) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | N Indicator | — | 13 | — | value = (D[13] & 0X20) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | D Indicator | — | 13 | — | value = (D[13] & 0X10) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | S Indicator | — | 13 | — | value = (D[13] & 0X08) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | L Indicator | — | 13 | — | value = (D[13] & 0X04) != 0 |
| 22/2321 | A/T D Switch; A/T L Switch; A/T N Switch; A/T P Switch; A/T R Switch; A/T S Switch; ECON Mode Indicator; Sport Mode Indicator; Manual Mode Indicator; LED A; LED B; LED C; P Indicator; R Indicator; N Indicator; D Indicator; S Indicator; L Indicator; Shift position indicator all segment | L640 | 22 23 21 | — | 3 | 62 23 21 + D[0..35] | 39 when appended | None in recovered handler | Firmware | Shift position indicator all segment | — | 13 | — | value = (D[13] & 0X02) != 0 |
| 22/2322 | ETR; Pulley Ratio | L640 | 22 23 22 | — | 3 | 62 23 22 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d25 | 0xFFF96BB6 | D[25] | — | 0xFFF96BB6, one byte. HDS catalog label Target Revolution Speed Following Status is CORROBORATED; the exact source byte is PROVEN. [Dossier] |
| 22/2322 | ETR; Pulley Ratio | L640 | 22 23 22 | — | 3 | 62 23 22 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d26 | 0xFFF9370C | D[26] | — | ETR percent byte from u16 0xFFF9370C. Exact formula for the nonnegative source domain is `sat_u8(floor(raw * 0.005))`; the listing implements this with signed multiply constant 0x51EB851F and shift 38. HDS CANCVT `ETR@26`, source, formula, and handler join are PROVEN. HDS defines ETR as torque-converter slip ratio in percent. [Dossier] |
| 22/2322 | ETR; Pulley Ratio | L640 | 22 23 22 | — | 3 | 62 23 22 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d27 | 0xFFF96434 | D[27] | — | 0xFFF96434, one byte. HDS Pulley Ratio Rate interpretation is CORROBORATED; source is PROVEN. [Dossier] |
| 22/2322 | ETR; Pulley Ratio | L640 | 22 23 22 | — | 3 | 62 23 22 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d28 | 0xFFF8F7C8 | D[28] | — | high byte of u16 0xFFF8F7C8. This is the exact Q14 actual CVT/pulley ratio source also transmitted in CAN 0x191 b3; ratio lower bound is d28/64 and the hidden interval is `[d28/64,(d28+1)/64)`. [Dossier] |
| 22/2322 | ETR; Pulley Ratio | L640 | 22 23 22 | — | 3 | 62 23 22 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d29 | 0xFFF96438 | D[29] | — | 0xFFF96438, one byte. HDS Warm Up Status interpretation is CORROBORATED; source is PROVEN. [Dossier] |
| 22/2322 | ETR; Pulley Ratio | L640 | 22 23 22 | — | 3 | 62 23 22 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d30 | 0xFFF96435 | D[30] | — | 0xFFF96435, one byte. HDS Vehicle Speed Rate interpretation is CORROBORATED; source is PROVEN. [Dossier] |
| 22/2322 | ETR; Pulley Ratio | L640 | 22 23 22 | — | 3 | 62 23 22 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d31 | — | D[31] | — | ROM byte 0x0003F667, stock value 0x3B. [Dossier] |
| 22/2322 | ETR; Pulley Ratio | L640 | 22 23 22 | — | 3 | 62 23 22 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d32 | 0xFFF95C1C, 0xFFF963CA, 0xFFF963CE, 0xFFF963D2, 0xFFF96B64 | D[32] | — | packed MSB-first from FFF963CE[1], FFF963CE[0], FFF963D2[1], FFF963D2[0], boolean FFF95C1C, `(FFF96B64==0x11)`, FFF963CA[1], FFF963CA[0]. Bit packing is PROVEN; physical meanings remain TBD. [Dossier] |
| 22/2322 | ETR; Pulley Ratio | L640 | 22 23 22 | — | 3 | 62 23 22 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d33 | 0xFFF8F706 | D[33] | — | signed 0xFFF8F706 divided by four with truncation toward zero, narrowed to one byte; physical meaning TBD. [Dossier] |
| 22/2322 | ETR; Pulley Ratio | L640 | 22 23 22 | — | 3 | 62 23 22 + D[0..35] | 39 when appended | None in recovered handler | Firmware dossier | Data d34..d35 | 0xFFF8F8C2 | D[34..35] | — | big-endian u16 0xFFF8F8C2; physical meaning TBD. [Dossier] |
| 22/2322 | ETR; Pulley Ratio | L640 | 22 23 22 | — | 3 | 62 23 22 + D[0..35] | 39 when appended | None in recovered handler | Firmware | ETR | — | 26 | — | raw = D[26]; wire encoder: sat_u8(floor(u16(raw)*0.005)) |
| 22/2322 | ETR; Pulley Ratio | L640 | 22 23 22 | — | 3 | 62 23 22 + D[0..35] | 39 when appended | None in recovered handler | Firmware | Pulley Ratio | — | 28 | — | raw = D[28]; wire encoder: (u16[FFF8F7C8]>>8)&255; mask0x00FF; CAN191 same byte; raw/64 gives ratio lower bound |
| 22/2323 | PMSTRCYL; VSACASEN | L640 | 22 23 23 | — | 3 | 62 23 23 + D[0..35] | 39 when appended | None in recovered handler | Firmware | PMSTRCYL | — | 12..13 | — | BE16=data12*256+data13; kPa=raw |
| 22/2323 | PMSTRCYL; VSACASEN | L640 | 22 23 23 | — | 3 | 62 23 23 + D[0..35] | 39 when appended | None in recovered handler | Firmware | VSACASEN | — | 9 bit0 | — | value = D[9] & 1 |
| 22/2330 | Firmware data record 2330 | L640 | 22 23 30 | — | 3 | 62 23 30 + D[0..35] | 39 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/2331 | Firmware data record 2331 | L640 | 22 23 31 | — | 3 | 62 23 31 + D[0..35] | 39 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/2332 | Firmware data record 2332 | L640 | 22 23 32 | — | 3 | 62 23 32 + D[0..35] | 39 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/2333 | Firmware data record 2333 | L640 | 22 23 33 | — | 3 | 62 23 33 + D[0..35] | 39 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/2340 | Firmware data record 2340 | L640 | 22 23 40 | — | 3 | 62 23 40 + D[0..35] | 39 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/2341 | Firmware data record 2341 | L640 | 22 23 41 | — | 3 | 62 23 41 + D[0..2] | 6 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/2342 | Firmware data record 2342 | L640 | 22 23 42 | — | 3 | 62 23 42 + D[0..2] | 6 when appended | None in recovered handler | Firmware dossier | FRZDTC(H) | 0xFFF83532 | D[0] | — | High byte of uint16 at 0xFFF83532 [PROVEN dossier table] |
| 22/2342 | Firmware data record 2342 | L640 | 22 23 42 | — | 3 | 62 23 42 + D[0..2] | 6 when appended | None in recovered handler | Firmware dossier | FRZDTC(L) | 0xFFF849E1 | D[2] | — | uint8 at 0xFFF849E1 [PROVEN dossier table] |
| 22/23E0 | Firmware data record 23E0 | L640 | 22 23 E0 | — | 3 | 62 23 E0 + D[0..35] | 39 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/23E1 | Firmware data record 23E1 | L640 | 22 23 E1 | — | 3 | 62 23 E1 + D[0..35] | 39 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/23E2 | Firmware data record 23E2 | L640 | 22 23 E2 | — | 3 | 62 23 E2 + D[0..35] | 39 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/23E3 | Firmware data record 23E3 | L640 | 22 23 E3 | — | 3 | 62 23 E3 + D[0..35] | 39 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/23E4 | Firmware data record 23E4 | L640 | 22 23 E4 | — | 3 | 62 23 E4 + D[0..35] | 39 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/2600 | hds_ecu_identity_fingerprint_ECUID1_5_OBDSID | L640 | 22 26 00 | — | 3 | 62 26 00 32 16 00 21 01 EE 0E 00 00 00 | 13 | None in recovered handler | HDS | ECUID1 | ECUID1 | 0 | 0xFF | raw = D[0] |
| 22/2600 | hds_ecu_identity_fingerprint_ECUID1_5_OBDSID | L640 | 22 26 00 | — | 3 | 62 26 00 32 16 00 21 01 EE 0E 00 00 00 | 13 | None in recovered handler | HDS | ECUID2 | ECUID2 | 1 | 0xFF | raw = D[1] |
| 22/2600 | hds_ecu_identity_fingerprint_ECUID1_5_OBDSID | L640 | 22 26 00 | — | 3 | 62 26 00 32 16 00 21 01 EE 0E 00 00 00 | 13 | None in recovered handler | HDS | ECUID3 | ECUID3 | 2 | 0xFF | raw = D[2] |
| 22/2600 | hds_ecu_identity_fingerprint_ECUID1_5_OBDSID | L640 | 22 26 00 | — | 3 | 62 26 00 32 16 00 21 01 EE 0E 00 00 00 | 13 | None in recovered handler | HDS | ECUID4 | ECUID4 | 3 | 0xFF | raw = D[3] |
| 22/2600 | hds_ecu_identity_fingerprint_ECUID1_5_OBDSID | L640 | 22 26 00 | — | 3 | 62 26 00 32 16 00 21 01 EE 0E 00 00 00 | 13 | None in recovered handler | HDS | ECUID5 | ECUID5 | 4 | 0xFF | raw = D[4] |
| 22/2600 | hds_ecu_identity_fingerprint_ECUID1_5_OBDSID | L640 | 22 26 00 | — | 3 | 62 26 00 32 16 00 21 01 EE 0E 00 00 00 | 13 | None in recovered handler | HDS | OBDSID | OBDSID | 6 | 0xFF | raw = D[6] |
| 22/2601 | Firmware data record 2601 | L640 | 22 26 01 | — | 3 | 62 26 01 + D[0..2] | 6 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/260F | CANFI data packet 260F | HDS only | 22 26 0F | — | 3 | — | — | — | HDS | DEVEDATA | DEVEDATA | 255 | 0xFF | raw = D[255] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d00 | — | D[0] | — | FF [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d01 | 0xFFF95057 | D[1] | — | 0xFFF95057!=0 ? FD : CD [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d02 | 0xFFF91428 | D[2] | — | F0 if (U16[0xFFF91428]&F000)==1000, else B0 [PROVEN packed constants/condition] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d03 | 0xFFF9504C, 0xFFF9505F | D[3] | — | (0xFFF9504C?7C:60) &#124; (0xFFF9505F?01:00) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d04 | 0xFFF9505F | D[4] | — | 0xFFF9505F!=0 ? E0 : 60 [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d05 | — | D[5] | — | FC [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d06..d07 | 0xFFF912A0 | D[6..7] | — | BE16(U16[0xFFF912A0] << 2) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d08 | 0xFFF94C6C | D[8] | — | U8[0xFFF94C6C] [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d09 | 0xFFF94C6E | D[9] | — | U8[0xFFF94C6E] [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d10 | 0xFFF8F710 | D[10] | — | low8(trunc0(S16[0xFFF8F710]/4)) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d11 | 0xFFF94A53 | D[11] | — | U8[0xFFF94A53] [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d12 | 0xFFF8F70C | D[12] | — | low8(trunc0(S16[0xFFF8F70C]/4)) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d13 | 0xFFF94A3A | D[13] | — | U8[0xFFF94A3A] [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d14 | 0xFFF8F6FE | D[14] | — | low8(trunc0(S16[0xFFF8F6FE]/4)) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d15 | 0xFFF94A18 | D[15] | — | U8[0xFFF94A18] [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d16 | 0xFFF8F6FA | D[16] | — | low8(trunc0(S16[0xFFF8F6FA]/4)) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d17 | 0xFFF94A08 | D[17] | — | U8[0xFFF94A08] [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d18 | 0xFFF94E3A | D[18] | — | U8[0xFFF94E3A] [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d19 | 0xFFF961EC | D[19] | — | U8[0xFFF961EC] [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d20 | — | D[20] | — | 00 [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d21 | 0xFFF8DB80, 0xFFF94CFD, 0xFFF94DDB | D[21] | — | 0x000E3B12 result: source 0 unless 0xFFF94CFD==0 and 0xFFF94DDB!=0; source is S16[0xFFF8DB80] when state==2 else S16[ROM 0x3F64A]; source<-640 ->0, otherwise sat_u8(trunc0(source/5)+128) [PROVEN algorithm; physical meaning TBD] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d22 | 0xFFF91818 | D[22] | — | sat_u8(trunc0(S16[0xFFF91818]/40)) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d23 | 0xFFF8F7A4 | D[23] | — | low8(trunc0(S16[0xFFF8F7A4]/4)) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d24..d25 | 0xFFF8DB14 | D[24..25] | — | BE16(min(65535,trunc0(S32[0xFFF8DB14]/2))) [PROVEN transform; negative domain TBD] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d26..d30 | — | D[26..30] | — | 00 00 00 00 00 [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d31 | 0xFFF95077 | D[31] | — | 0xFFF95077!=0 ? 0F : 0B [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d32 | 0xFFF9493D, 0xFFF94981, 0xFFF94DEF, 0xFFF95B4A | D[32] | — | bit3=0xFFF9493D!=0; bit2=0xFFF94DEF in {1,2}; bit1=0xFFF95B4A!=0; bit0=0xFFF94981!=0 [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d33 | 0xFFF8F6DC | D[33] | — | low8(trunc0(S16[0xFFF8F6DC]/4)) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d34..d35 | 0xFFF928F6 | D[34..35] | — | BE16(U16[0xFFF928F6]) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d36 | — | D[36] | — | 00 [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d37 | 0xFFF8F70E | D[37] | — | low8(trunc0(S16[0xFFF8F70E]/4)) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d38 | 0xFFF90FBE | D[38] | — | sat_u8(trunc0(S16[0xFFF90FBE]/10)+40) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d39..d40 | 0xFFF928F2 | D[39..40] | — | BE16(U16[0xFFF928F2]) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d41..d45 | — | D[41..45] | — | 00 00 00 00 00 [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d46..d47 | 0xFFF91818 | D[46..47] | — | BE16(U16[0xFFF91818]) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d48..d49 | 0xFFF90F88 | D[48..49] | — | BE16(U16[0xFFF90F88]) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d50..d51 | 0xFFF923EA | D[50..51] | — | BE16(U16[0xFFF923EA]) [PROVEN] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d52..d53 | — | D[52..53] | — | 00 00 [PROVEN at 0x000ECFB4/0x000ECFBE] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | Firmware | MIL | — | 32 | — | value = (D[32] >> 3) & 1 |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Engine Speed | NE | 6 | 0xFF | raw = D[6] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Engine Speed | NE | 7 | 0xFF | raw = D[7] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | TP Sensor | ABSTH | 8 | 0xFF | raw = D[8] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | REL TP Sensor | RELTH | 9 | 0xFF | raw = D[9] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | ECT Sensor 1 | TW | 10 | 0xFF | raw = D[10] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | ECT Sensor 1 | ECT | 11 | 0xFF | raw = D[11] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | IAT Sensor (1) | TA | 12 | 0xFF | raw = D[12] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | IAT Sensor (1) | IAT | 13 | 0xFF | raw = D[13] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | MAP Sensor | PB | 14 | 0xFF | raw = D[14] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | MAP Sensor | MAP | 15 | 0xFF | raw = D[15] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Baro Sensor | PA | 16 | 0xFF | raw = D[16] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Baro Sensor | BARO | 17 | 0xFF | raw = D[17] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Vehicle Speed | VSP | 18 | 0xFF | raw = D[18] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | CLV | CLV | 19 | 0xFF | raw = D[19] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Memory Back-Up Voltage | VKAM | 20 | 0xFF | raw = D[20] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Spark Advance | IG | 21 | 0xFF | raw = D[21] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Battery | VB | 22 | 0xFF | raw = D[22] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Alternator | ACGF | 23 | 0xFF | raw = D[23] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | F Injector | TOUT | 24 | 0xFF | raw = D[24] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | F Injector | TOUT | 25 | 0xFF | raw = D[25] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | EGR Valve Position Sensor (EGR Vls) | LIFT | 26 | 0xFF | raw = D[26] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | EGR L Command | LCMD | 27 | 0xFF | raw = D[27] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | EGR Valve Lift | LACT | 28 | 0xFF | raw = D[28] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | IAC Command | ICMD | 30 | 0xFF | raw = D[30] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | IAC Command | ICMD_QIDL | 30 | 0xFF | raw = D[30] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | A/C Switch | ACS | 32 | 0x01 | raw = (D[32] & 0x01) >> 0 |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | A/C Clutch | ACC | 32 | 0x02 | raw = (D[32] & 0x02) >> 1 |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Immobilizer | IMBLIZ | 32 | 0x04 | raw = (D[32] & 0x04) >> 2 |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | MIL | WARN | 32 | 0x08 | raw = (D[32] & 0x08) >> 3 |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | MAF Sensor | AFM | 33 | 0xFF | raw = D[33] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | MAF Sensor | GAIR | 34 | 0xFF | raw = D[34] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | MAF Sensor | GAIR | 35 | 0xFF | raw = D[35] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Spark Advance Exhaust Side | IGSP | 36 | 0xFF | raw = D[36] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | ECT Sensor 2 | TW2 | 37 | 0xFF | raw = D[37] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | ECT Sensor 2 | ECT2A | 38 | 0xFF | raw = D[38] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | IAT Sensor (2) | TAA | 41 | 0xFF | raw = D[41] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | IAT Sensor (2) | SIAT | 42 | 0xFF | raw = D[42] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Rocker Arm Oil Pressure Sensor | VEOPS | 43 | 0xFF | raw = D[43] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Rocker Arm Oil Pressure Sensor | EOPSPHY | 44 | 0xFF | raw = D[44] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Rocker Arm Oil Pressure Sensor | EOPSPHY | 45 | 0xFF | raw = D[45] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Battery (Hi Res) | VBENAN | 46 | 0xFF | raw = D[46] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Battery (Hi Res) | VBENAN | 47 | 0xFF | raw = D[47] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | MAP Sensor (Hi Res) | PBAENAN | 48 | 0xFF | raw = D[48] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | MAP Sensor (Hi Res) | PBAENAN | 49 | 0xFF | raw = D[49] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Spark Advance (Hi Res) | IGENAN | 50 | 0xFF | raw = D[50] |
| 22/2610 | CANFI/FC-MG engine data packet 2610 | L640 | 22 26 10 | — | 3 | 62 26 10 + D[0..53] | 57 when appended | None in recovered handler | HDS | Spark Advance (Hi Res) | IGENAN | 51 | 0xFF | raw = D[51] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor | XILAF | 6 | 0xFF | raw = D[6] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor | XILAF | 7 | 0xFF | raw = D[7] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Lambda | LAMBDA | 8 | 0xFF | raw = D[8] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | Air Fuel Ratio | LAMBDA_AFR | 8 | 0xFF | raw = D[8] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Lambda | LAMBDA | 9 | 0xFF | raw = D[9] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | Air Fuel Ratio | LAMBDA_AFR | 9 | 0xFF | raw = D[9] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB (ST Fuel Trim) | KLAF | 10 | 0xFF | raw = D[10] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB AVE (LT Fuel Trim) | KLAFAVE | 11 | 0xFF | raw = D[11] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Lambda Cmd | CMDEQRAT | 12 | 0xFF | raw = D[12] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB Cmd | CMDEQRAT/KCMD | 12 | 0xFF | raw = D[12] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Lambda Cmd | CMDEQRAT | 13 | 0xFF | raw = D[13] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB Cmd | CMDEQRAT/KCMD | 13 | 0xFF | raw = D[13] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | FSS | FSS | 14 | 0xFF | raw = D[14] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S S2 | SVO2 | 15 | 0xFF | raw = D[15] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S S2 Heater Current | ISO2HT | 16 | 0xFF | raw = D[16] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S S2 Heater Current | ISO2HT | 17 | 0xFF | raw = D[17] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor B1 | XILAF-B1 | 18 | 0xFF | raw = D[18] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor B1 | XILAF-B1 | 19 | 0xFF | raw = D[19] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B1 Lambda | LAMBDA-B1 | 20 | 0xFF | raw = D[20] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B1 Lambda | LAMBDA-B1 | 21 | 0xFF | raw = D[21] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | ST Fuel Trim B1 | KLAF-B1 | 22 | 0xFF | raw = D[22] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB AVE(LT Fuel Trim) B1 | KLAFAVE-B1 | 23 | 0xFF | raw = D[23] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B1 Lambda Cmd | CMDEQRAT-B1 | 24 | 0xFF | raw = D[24] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB Cmd B1 | CMDEQRAT-B1/KCMD | 24 | 0xFF | raw = D[24] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B1 Lambda Cmd | CMDEQRAT-B1 | 25 | 0xFF | raw = D[25] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB Cmd B1 | CMDEQRAT-B1/KCMD | 25 | 0xFF | raw = D[25] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | FSS B1 | FSS-B1 | 26 | 0xFF | raw = D[26] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S B1 S2 | SVO2-B1 | 27 | 0xFF | raw = D[27] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S(B1) S2 Heater Current | ISO2HT-B1 | 28 | 0xFF | raw = D[28] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S(B1) S2 Heater Current | ISO2HT-B1 | 29 | 0xFF | raw = D[29] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor B2 | XILAF-B2 | 30 | 0xFF | raw = D[30] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor B2 | XILAF-B2 | 31 | 0xFF | raw = D[31] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B2 Lambda | LAMBDA-B2 | 32 | 0xFF | raw = D[32] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B2 Lambda | LAMBDA-B2 | 33 | 0xFF | raw = D[33] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | ST Fuel Trim B2 | KLAF-B2 | 34 | 0xFF | raw = D[34] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB AVE(LT Fuel Trim) B2 | KLAFAVE-B2 | 35 | 0xFF | raw = D[35] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B2 Lambda Cmd | CMDEQRAT-B2 | 36 | 0xFF | raw = D[36] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB Cmd B2 | CMDEQRAT-B2/KCMD | 36 | 0xFF | raw = D[36] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B2 Lambda Cmd | CMDEQRAT-B2 | 37 | 0xFF | raw = D[37] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB Cmd B2 | CMDEQRAT-B2/KCMD | 37 | 0xFF | raw = D[37] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | FSS B2 | FSS-B2 | 38 | 0xFF | raw = D[38] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S B2 S2 | SVO2-B2 | 39 | 0xFF | raw = D[39] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S B2 S2 Heater Current | ISO2HT-B2 | 40 | 0xFF | raw = D[40] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S B2 S2 Heater Current | ISO2HT-B2 | 41 | 0xFF | raw = D[41] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S (AF) S1 Heater | HTCNT | 43 | 0x01 | raw = (D[43] & 0x01) >> 0 |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S S2 Heater | SHTCNT | 43 | 0x02 | raw = (D[43] & 0x02) >> 1 |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S (AF) B1 S1 Heater | HTCNT-B1 | 43 | 0x04 | raw = (D[43] & 0x04) >> 2 |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S B1 S2 Heater | SHTCNT-B1 | 43 | 0x08 | raw = (D[43] & 0x08) >> 3 |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S (AF) B2 S1 Heater | HTCNT-B2 | 43 | 0x10 | raw = (D[43] & 0x10) >> 4 |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S B2 S2 Heater | SHTCNT-B2 | 43 | 0x20 | raw = (D[43] & 0x20) >> 5 |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | IMA | IMA | 44 | 0xFF | raw = D[44] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | Alcohol Percentage at Learned | AFP | 45 | 0xFF | raw = D[45] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Alcohol Content Learned Value | KFKIND | 46 | 0xFF | raw = D[46] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | Subfuel Solenoid Operation | FFVSTDTY | 47 | 0xFF | raw = D[47] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | Engine Oil Dilution Influenced Rate | RGCTMREM | 48 | 0xFF | raw = D[48] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | Alcohol Fuel Percentage | ETACONPHY | 49 | 0xFF | raw = D[49] |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | Engine Cold Start Condition | FFVCSC | 51 | 0x01 | raw = (D[51] & 0x01) >> 0 |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | Abnormal Fuel Information | FLABNORM | 51 | 0x02 | raw = (D[51] & 0x02) >> 1 |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Alcohol Content Learned Condition | KREFBSON | 51 | 0x08 | raw = (D[51] & 0x08) >> 3 |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | Engine Oil Dilution Influence | OCTM | 51 | 0x10 | raw = (D[51] & 0x10) >> 4 |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | FFVRFUEL | FFVRFUEL | 51 | 0x20 | raw = (D[51] & 0x20) >> 5 |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | ACLRDY | ACLRDY | 51 | 0x40 | raw = (D[51] & 0x40) >> 6 |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Alcohol Content Learned Condition | ACLEND | 51 | 0x80 | raw = (D[51] & 0x80) >> 7 |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | Subfuel Pump Relay Command | FFVFLR | 53 | 0x01 | raw = (D[53] & 0x01) >> 0 |
| 22/2611 | CANFI data packet 2611 | L640 | 22 26 11 | — | 3 | 62 26 11 + D[0..51] | 55 when appended | None in recovered handler | HDS | Subfuel Solenoid System Condition | FFVFUELSOK | 53 | 0x20 | raw = (D[53] & 0x20) >> 5 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | APP Sensor A | APPS1 | 6 | 0xFF | raw = D[6] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | APP Sensor B | APPS2 | 7 | 0xFF | raw = D[7] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | APP Sensor | APP | 8 | 0xFF | raw = D[8] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | APP Sensor | APP | 9 | 0xFF | raw = D[9] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | TP Sensor A | TH-1 | 10 | 0xFF | raw = D[10] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | TP Sensor B | TH-2 | 11 | 0xFF | raw = D[11] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Throttle VLV | RELTHW | 12 | 0xFF | raw = D[12] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Throttle VLV | RELTHW | 13 | 0xFF | raw = D[13] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | TP Sensor | TH | 14 | 0xFF | raw = D[14] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Target TH VLV | THO | 14 | 0xFF | raw = D[14] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | TP Sensor | TH | 15 | 0xFF | raw = D[15] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Target TH VLV | THO | 15 | 0xFF | raw = D[15] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | APP SENSOR | THAPDEG | 18 | 0xFF | raw = D[18] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Target TH | THICMD | 18 | 0xFF | raw = D[18] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | APP SENSOR | THAPDEG | 19 | 0xFF | raw = D[19] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Target TH | THICMD | 19 | 0xFF | raw = D[19] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | VTEC Solenoid Valve | VTS | 21 | 0x01 | raw = (D[21] & 0x01) >> 0 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | VTEC Press Sw | VTM | 21 | 0x02 | raw = (D[21] & 0x02) >> 1 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Rocker Arm Oil Control Solenoid A (Bank 1) | VTS-B1 | 21 | 0x04 | raw = (D[21] & 0x04) >> 2 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | VTS Except VTEC Sw (Bank1) | VTSB1 | 21 | 0x04 | raw = (D[21] & 0x04) >> 2 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Rocker Arm Oil Pressure Switch A (Bank 1) | VTMB1 | 21 | 0x08 | raw = (D[21] & 0x08) >> 3 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Rocker Arm Oil Control Solenoid A (Bank 2) | VTS-B2 | 21 | 0x10 | raw = (D[21] & 0x10) >> 4 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | VTS Except VTEC Sw (Bank2) | VTSB2 | 21 | 0x10 | raw = (D[21] & 0x10) >> 4 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | VTEC Press Sw B2 | VTM-B2 | 21 | 0x20 | raw = (D[21] & 0x20) >> 5 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Rocker Arm Oil Pressure Switch A (Bank 2) | VTMB2 | 21 | 0x20 | raw = (D[21] & 0x20) >> 5 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Solenoid Return Signal | RVTS | 23 | 0x01 | raw = (D[23] & 0x01) >> 0 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | VTSB1 Circuit Monitoring | VTSB1R | 23 | 0x02 | raw = (D[23] & 0x02) >> 1 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | VTSB1R Except VTSB2 Circuit Monitoring | VTSB2R | 23 | 0x04 | raw = (D[23] & 0x04) >> 2 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | i-VTEC Indicator Command | VTECIND | 23 | 0x80 | raw = (D[23] & 0x80) >> 7 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | CMP Ctrl | VTCANGL | 24 | 0xFF | raw = D[24] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | IVTCSOL | IVTCSOL | 25 | 0xFF | raw = D[25] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Rocker Arm Oil Control Sol.  1 | VTS1 | 27 | 0x01 | raw = (D[27] & 0x01) >> 0 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Solenoid 1 Return Signal | VTS1R | 27 | 0x02 | raw = (D[27] & 0x02) >> 1 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | ROCKER ARM OIL CONTROL SOL.  2 | VTS2 | 27 | 0x04 | raw = (D[27] & 0x04) >> 2 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | SOLENOID 2 RETURN SIGNAL | VTS2R | 27 | 0x08 | raw = (D[27] & 0x08) >> 3 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Rocker Arm Oil Pressure Switch | VTMACD | 27 | 0x20 | raw = (D[27] & 0x20) >> 5 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Estimated air pressure (PA) | PAEST | 28 | 0xFF | raw = D[28] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | F Injector Active Side | TOUTA | 29 | 0xFF | raw = D[29] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | F Injector Active Side | TOUTA | 30 | 0xFF | raw = D[30] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | (Rocker Arm) Oil Pressure Sensor (B) | POIL_B | 31 | 0xFF | raw = D[31] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | (Rocker Arm) Oil Pressure Sensor (B) | EOP | 32 | 0xFF | raw = D[32] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | (Rocker Arm) Oil Pressure Sensor (B) | EOP | 33 | 0xFF | raw = D[33] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Rocker Arm Oil Control Solenoid B (Bank 1) | CDACTS | 35 | 0x01 | raw = (D[35] & 0x01) >> 0 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Rocker Arm Oil Control Solenoid B Return | CDACTSR | 35 | 0x02 | raw = (D[35] & 0x02) >> 1 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Rocker Arm Oil Pressure Switch B (Bank 1) | VCMCDACT | 35 | 0x04 | raw = (D[35] & 0x04) >> 2 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | SVSOUT | SVSOUT | 36 | 0xFF | raw = D[36] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | IMT (IMRC) Valve Cmd | SVSCMD | 38 | 0x01 | raw = (D[38] & 0x01) >> 0 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | IMT (IMRC) Valve Sw | SVM | 38 | 0x02 | raw = (D[38] & 0x02) >> 1 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | SVSP | SVSP | 38 | 0x04 | raw = (D[38] & 0x04) >> 2 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | SVSM | SVSM | 38 | 0x08 | raw = (D[38] & 0x08) >> 3 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | M Shaft Spd | NM | 39 | 0xFF | raw = D[39] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | M Shaft Spd | NM | 40 | 0xFF | raw = D[40] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | C Shaft Spd | VNC | 41 | 0xFF | raw = D[41] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Reverse Lock Sol | RVSLCK | 43 | 0x01 | raw = (D[43] & 0x01) >> 0 |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Gear Position | NGP | 44 | 0xFF | raw = D[44] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Actual Gear Position | ACTLGEAR | 46 | 0xFF | raw = D[46] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Slip Ratio of Torq or Startclutch | ETSENAN | 47 | 0xFF | raw = D[47] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Commanded Electric Current of Linear Solenoid E | ICMDENAN | 48 | 0xFF | raw = D[48] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Commanded Electric Current of Linear Solenoid E | ICMDENAN | 49 | 0xFF | raw = D[49] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | ILOADENAN | ILOADENAN | 50 | 0xFF | raw = D[50] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | ILOADENAN | ILOADENAN | 51 | 0xFF | raw = D[51] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Knock sensor retard calculation factor | KIGKNENAN | 52 | 0xFF | raw = D[52] |
| 22/2612 | engine/throttle/VTEC/transmission data-list packet | L640 | 22 26 12 | — | 3 | 62 26 12 + D[0..51] | 55 when appended | None in recovered handler | HDS | Knock sensor retard calculation factor | KIGKNENAN | 53 | 0xFF | raw = D[53] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d00 | 0xFFF95016, 0xFFF95018, 0xFFF95036, 0xFFF9505A | D[0] | — | bit7=0xFFF9505A; bits6,5=0xFFF95016; bit4=0xFFF95018; low nibble=0xFFF95036 [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d01 | 0xFFF9504B | D[1] | — | 0xFFF9504B!=0 ? E0 : 00 [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d02..d04 | — | D[2..4] | — | 00 00 00 [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d05 | 0xFFF95018, 0xFFF9505A | D[5] | — | bits7,6=0xFFF95018; bits5,4=0xFFF9505A; low nibble0 [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d06 | 0xFFF961F1 | D[6] | — | U8[0xFFF961F1] [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d07 | 0xFFF94FFB, 0xFFF95016 | D[7] | — | bit7=0xFFF94FFB; bits2,1=0xFFF95016 [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d08 | 0xFFF871F3, 0xFFF9432A, 0xFFF95F27 | D[8] | — | bit7=0xFFF871F3; bit2=0xFFF9432A; bit1=0xFFF95F27 [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d09 | 0xFFF8F746 | D[9] | — | low8(trunc0(S16[0xFFF8F746]/4)) [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d10 | 0xFFF90FE2, 0xFFF94B51 | D[10] | — | 0xFFF94B51==0 ? low8(trunc0(S16[0xFFF90FE2]/4)) : 00 [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d11 | 0xFFF94D32 | D[11] | — | U8[0xFFF94D32] [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d12..d13 | 0xFFF92894, 0xFFF94B51 | D[12..13] | — | 0xFFF94B51==0 ? BE16(U16[0xFFF92894]) : 00 00 [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d14 | 0xFFF8F6C0 | D[14] | — | low8(trunc0(S16[0xFFF8F6C0]/4)) [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d15..d16 | 0xFFF90EE8 | D[15..16] | — | BE16(U16[0xFFF90EE8]) [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d17..d45 | — | D[17..45] | — | all zero [PROVEN at 0x000ED87E onward] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d46..d47 | 0xFFF912DC | D[46..47] | — | BE16(U16[0xFFF912DC]) [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d48..d49 | 0xFFF92A22 | D[48..49] | — | BE16(U16[0xFFF92A22]) [PROVEN] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d50..d53 | — | D[50..53] | — | 00 00 00 00 [PROVEN at 0x000ED8B8..0x000ED8CC] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d06 | 0xFFF961F1 | D[6] | — | U8[FFF961F1] ; DPCS / EVAP PC Duty; raw/256*100 percent [PROVEN with OBD PID 0x2E corroboration] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d08 | 0xFFF871F3 | D[8] | — | bit7 ; FFF871F3 ; FCAPOPEN / FUEL CAP [CORROBORATED physical name] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d08 | 0xFFF9432A | D[8] | — | bit2 ; FFF9432A ; RVSV / Re CVS Valve [CORROBORATED physical name] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d08 | 0xFFF95F27 | D[8] | — | bit1 ; FFF95F27 ; VSV / EVAP CVS Valve [CORROBORATED physical name] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d09 | 0xFFF8F746 | D[9] | — | low8(trunc0(S16[FFF8F746]/4)) ; PTANK / FTP Sensor voltage-domain field [CORROBORATED physical name] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d10 | 0xFFF90FE2, 0xFFF94B51 | D[10] | — | FFF94B51==0 ? low8(trunc0(S16[FFF90FE2]/4)) : 00 ; FLSVLV / Fuel Level Sensor voltage [PROVEN received 0x1A6 d4 byte; voltage converter TBD] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d11 | 0xFFF94D32 | D[11] | — | U8[FFF94D32] ; FLI / Fuel Level; raw*100/255 percent [PROVEN with OBD PID 0x2F chain] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d12..d13 | 0xFFF92894, 0xFFF94B51 | D[12..13] | — | FFF94B51==0 ? BE16(U16[FFF92894]) : 00 00 ; FLEVELF / Fuel Level(Average); raw*0.1 percent ; END_TO_END_PROVEN [Dossier] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d14 | 0xFFF8F6C0 | D[14] | — | low8(trunc0(S16[FFF8F6C0]/4)) ; ACRPS / A/C Pressure Sensor raw field [PROVEN via P0532/P0533 and AN15 mux1] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d15..d16 | 0xFFF90EE8 | D[15..16] | — | BE16(U16[FFF90EE8]) ; ACRP / A/C Pressure Sensor calculated field [PROVEN physical meaning; engineering unit TBD] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d17..d45 | — | D[17..45] | — | all zero ; HDS fields in this region belong to other CANFI variants and are not L640 assignments [PROVEN zeros] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d46..d47 | 0xFFF912DC | D[46..47] | — | BE16(U16[FFF912DC]) ; EVAPVP / FTP Sensor (Fine); also exact OBD PID 0x32 source [PROVEN shared diagnostic quantity] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d48..d49 | 0xFFF92A22 | D[48..49] | — | BE16(U16[FFF92A22]) ; DPCSENAN / EVAP PC Duty (Hi Res) [CORROBORATED physical name] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d50..d53 | — | D[50..53] | — | 00 00 00 00 ; no L640 payload fields [PROVEN zeros] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | EVAP PC Duty | DPCS | 6 | 0xFF | raw = D[6] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | EVAP CVS Valve | VSV | 8 | 0x02 | raw = (D[8] & 0x02) >> 1 |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | Re CVS Valve | RVSV | 8 | 0x04 | raw = (D[8] & 0x04) >> 2 |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FUEL CAP | FCAPOPEN | 8 | 0x80 | raw = (D[8] & 0x80) >> 7 |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FTP Sensor | PTANK | 9 | 0xFF | raw = D[9] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | Fuel Level Sensor voltage | FLSVLV | 10 | 0xFF | raw = D[10] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | Fuel Level | FLI | 11 | 0xFF | raw = D[11] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | Fuel Level(Average) | FLEVELF | 12 | 0xFF | raw = D[12] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | Fuel Level(Average) | FLEVELF | 13 | 0xFF | raw = D[13] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | A/C Pressure Sensor | ACRPS | 14 | 0xFF | raw = D[14] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | A/C Pressure Sensor | ACRP | 15 | 0xFF | raw = D[15] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | A/C Pressure Sensor | ACRP | 16 | 0xFF | raw = D[16] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | Fuel Press. | PF2G | 22 | 0xFF | raw = D[22] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FP Sensor | PF2 | 23 | 0xFF | raw = D[23] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FP Sensor | PF2PHY | 24 | 0xFF | raw = D[24] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FP Sensor | PF2PHY | 25 | 0xFF | raw = D[25] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | Differential Pressure | PF2S | 26 | 0xFF | raw = D[26] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | Differential Pressure | PF2S | 27 | 0xFF | raw = D[27] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FT Sensor | TF2 | 28 | 0xFF | raw = D[28] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FT Sensor | TF2PHY | 29 | 0xFF | raw = D[29] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FTP Sensor | PF0 | 30 | 0xFF | raw = D[30] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FTP Sensor | PF0PHY | 31 | 0xFF | raw = D[31] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FTP Sensor | PF0PHY | 32 | 0xFF | raw = D[32] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FTT Sensor | TF0 | 33 | 0xFF | raw = D[33] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FTT Sensor | TF0PHY | 34 | 0xFF | raw = D[34] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | Fuel Meter Ctrl | FMODA | 35 | 0xFF | raw = D[35] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | Main Relay | FSR | 37 | 0x01 | raw = (D[37] & 0x01) >> 0 |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | Low Fuel Indi. | FWARN | 37 | 0x02 | raw = (D[37] & 0x02) >> 1 |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | Injector Mode | INJMODE | 37 | 0x08 | raw = (D[37] & 0x08) >> 3 |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | Fuel Rail Pressure SW | P2SW | 37 | 0x20 | raw = (D[37] & 0x20) >> 5 |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FFVUGAS | FFVUGAS | 38 | 0xFF | raw = D[38] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FFVUGAS | FFVUGAS | 39 | 0xFF | raw = D[39] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FTP Sensor (Fine) | EVAPVP | 46 | 0xFF | raw = D[46] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | FTP Sensor (Fine) | EVAPVP | 47 | 0xFF | raw = D[47] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | EVAP PC Duty (Hi Res) | DPCSENAN | 48 | 0xFF | raw = D[48] |
| 22/2613 | CANFI data packet 2613 | L640 | 22 26 13 | — | 3 | 62 26 13 + D[0..53] | 57 when appended | None in recovered handler | HDS | EVAP PC Duty (Hi Res) | DPCSENAN | 49 | 0xFF | raw = D[49] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Vehicle Status | STIMAOP | 6 | 0xFF | raw = D[6] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Driving Status | TQRMODE | 7 | 0xFF | raw = D[7] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | MASTOK | MASTOK | 9 | 0x02 | raw = (D[9] & 0x02) >> 1 |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Idle Stop Control | ENGRDY | 9 | 0x40 | raw = (D[9] & 0x40) >> 6 |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | A/C Compressor Command | ECONRQ | 9 | 0x80 | raw = (D[9] & 0x80) >> 7 |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | A/C Compressor Speed Command | NECOMPTG | 10 | 0xFF | raw = D[10] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | A/C Compressor Speed Command | NECOMPTG | 11 | 0xFF | raw = D[11] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | A/C Compressor Speed | NECOMP | 12 | 0xFF | raw = D[12] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | A/C Compressor Speed | NECOMP | 13 | 0xFF | raw = D[13] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | A/C Power Consumption | PWDHBAC | 14 | 0xFF | raw = D[14] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | A/C Power Consumption | PWDHBAC | 15 | 0xFF | raw = D[15] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IMA Output Command | PWBEMREQ | 16 | 0xFF | raw = D[16] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IMA Output Command | PWBEMREQ | 17 | 0xFF | raw = D[17] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | SOC | QBATC | 18 | 0xFF | raw = D[18] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | SOC | QBATC | 19 | 0xFF | raw = D[19] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IMA Output | PWBATF | 20 | 0xFF | raw = D[20] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IMA Output | PWBATF | 21 | 0xFF | raw = D[21] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IMA Battery Temperature | TBATC | 22 | 0xFF | raw = D[22] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DC-DC Converter Control | VDVREQ | 23 | 0xFF | raw = D[23] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Driving Status | TSTQMMODE | 25 | 0xFF | raw = D[25] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Driver'S Request Torque | TQAPOBJF | 26 | 0xFF | raw = D[26] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Driver'S Request Torque | TQAPOBJF | 27 | 0xFF | raw = D[27] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | VSA Control Torque | TQREQVSA | 28 | 0xFF | raw = D[28] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | VSA Control Torque | TQREQVSA | 29 | 0xFF | raw = D[29] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Cruise Control Torque | TQREQCRU | 30 | 0xFF | raw = D[30] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Cruise Control Torque | TQREQCRU | 31 | 0xFF | raw = D[31] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TM Control Torque | TQREQAT | 32 | 0xFF | raw = D[32] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TM Control Torque | TQREQAT | 33 | 0xFF | raw = D[33] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TQMBKLMT | TQMBKLMT | 34 | 0xFF | raw = D[34] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TQMBKLMT | TQMBKLMT | 35 | 0xFF | raw = D[35] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Regeneration Torque | TQMBKREQ | 36 | 0xFF | raw = D[36] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Regeneration Torque | TQMBKREQ | 37 | 0xFF | raw = D[37] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Target P/P Torque | TQCOBJ | 38 | 0xFF | raw = D[38] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Target P/P Torque | TQCOBJ | 39 | 0xFF | raw = D[39] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Actual P/P Torque | TQCACT | 40 | 0xFF | raw = D[40] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Actual P/P Torque | TQCACT | 41 | 0xFF | raw = D[41] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Requested Total Torque | TQPPRQF | 42 | 0xFF | raw = D[42] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Requested Total Torque | TQPPRQF | 43 | 0xFF | raw = D[43] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Target Engine Torque | TQECMD | 44 | 0xFF | raw = D[44] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Target Engine Torque | TQECMD | 45 | 0xFF | raw = D[45] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Requested IMA Motor Torque | TQMCMDDC | 48 | 0xFF | raw = D[48] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Requested IMA Motor Torque | TQMCMDDC | 49 | 0xFF | raw = D[49] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IMA Motor Torque | TQMACT | 50 | 0xFF | raw = D[50] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IMA Motor Torque | TQMACT | 51 | 0xFF | raw = D[51] |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Auto Idle Stop Does Not Occur (Brake) | ISPRHVBM | 53 | 0x01 | raw = (D[53] & 0x01) >> 0 |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Auto Idle Stop Does Not Occur (Idle Stop Sw) | ISPRHISSW | 53 | 0x02 | raw = (D[53] & 0x02) >> 1 |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Auto Idle Stop Does Not Occur (A/C) | ISPRHAC | 53 | 0x04 | raw = (D[53] & 0x04) >> 2 |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Clutch Pedal Position Switch(I/S) | ISPRHCLSW | 53 | 0x08 | raw = (D[53] & 0x08) >> 3 |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Auto Idle Stop Does Not Occur (NP Switch) | ISPRHNSW | 53 | 0x10 | raw = (D[53] & 0x10) >> 4 |
| 22/2614 | CANFI data packet 2614 | L640 | 22 26 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Auto Idle Stop Does Not Occur (PCU) | ISPRHPCU | 53 | 0x20 | raw = (D[53] & 0x20) >> 5 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TC Boost Pressure Sensor | P3 | 6 | 0xFF | raw = D[6] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TC Boost Pressure | TCBP | 7 | 0xFF | raw = D[7] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TC Boost Pressure | TCBP | 8 | 0xFF | raw = D[8] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TC Boost Pressure Upper Limit | P3TCOBJ | 9 | 0xFF | raw = D[9] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TC Boost Pressure Upper Limit | P3TCOBJ | 10 | 0xFF | raw = D[10] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Bi-Fuel System | CNGSTATUS | 11 | 0xFF | raw = D[11] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Normal Judgment Information | FFVHCUOK | 13 | 0x40 | raw = (D[13] & 0x40) >> 6 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Wakeup Signal Record | LCHWKUP | 13 | 0x80 | raw = (D[13] & 0x80) >> 7 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TC Boost Control Sol.V. | DVFTS | 14 | 0xFF | raw = D[14] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TC Wastegate Sol.V. | WGS | 15 | 0xFF | raw = D[15] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Air Bypass Sol.V. | ABVS | 17 | 0x01 | raw = (D[17] & 0x01) >> 0 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TC Bypass Sol.V. Return | ABVSR | 17 | 0x02 | raw = (D[17] & 0x02) >> 1 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Output Duty to HCU | DHCU | 18 | 0xFF | raw = D[18] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Power consumption of  HCU | PWFBHCU | 19 | 0xFF | raw = D[19] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Fuel Tank Center Sensor voltage | FLEVELCENAD | 20 | 0xFF | raw = D[20] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Neutral Position Sensor 1 | NPS1 | 26 | 0xFF | raw = D[26] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Neutral Position Sensor 2 | NPS2 | 27 | 0xFF | raw = D[27] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | T-Oil | TOIL | 28 | 0xFF | raw = D[28] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Pressure Sensor A | POIL2 | 30 | 0xFF | raw = D[30] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Pressure Sensor A | EOP2 | 31 | 0xFF | raw = D[31] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Pressure Sensor A | EOP2 | 32 | 0xFF | raw = D[32] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Engine Oil long interval mode | FFOILSEL | 34 | 0x80 | raw = (D[34] & 0x80) >> 7 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Solenoid B | CSSA | 37 | 0x01 | raw = (D[37] & 0x01) >> 0 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Solenoid B Return | CSSAR | 37 | 0x02 | raw = (D[37] & 0x02) >> 1 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Solenoid A | CSSB | 37 | 0x04 | raw = (D[37] & 0x04) >> 2 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Solenoid A Return | CSSBR | 37 | 0x08 | raw = (D[37] & 0x08) >> 3 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Solenoid A | VTSI | 39 | 0x01 | raw = (D[39] & 0x01) >> 0 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Sol A Return | RVTSI | 39 | 0x02 | raw = (D[39] & 0x02) >> 1 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Pressure Switch A | VTMI | 39 | 0x04 | raw = (D[39] & 0x04) >> 2 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Solenoid B | VTSE | 39 | 0x10 | raw = (D[39] & 0x10) >> 4 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Sol B Return | RVTSE | 39 | 0x20 | raw = (D[39] & 0x20) >> 5 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Pressure Switch B | VTME | 39 | 0x40 | raw = (D[39] & 0x40) >> 6 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Upper shutter grill initial learning | UPSGCALFIN | 41 | 0x04 | raw = (D[41] & 0x04) >> 2 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Lower shutter grill initial learning | LWSGCALFIN | 41 | 0x08 | raw = (D[41] & 0x08) >> 3 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | EGT Sensor1 Voltage | EGTS1 | 42 | 0xFF | raw = D[42] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | EGT Sensor2 Voltage | EGTS2 | 43 | 0xFF | raw = D[43] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | EGT Sensor1 | EGTS1P | 44 | 0xFF | raw = D[44] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | EGT Sensor2 | EGTS2P | 45 | 0xFF | raw = D[45] |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Sol A (B1) | CDACTS1 | 47 | 0x01 | raw = (D[47] & 0x01) >> 0 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Sol B (B1) | CDACTS2 | 47 | 0x02 | raw = (D[47] & 0x02) >> 1 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Sol A (B2) | CDACTS3 | 47 | 0x04 | raw = (D[47] & 0x04) >> 2 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Sol A (B1) Return | CDACTSR1 | 47 | 0x10 | raw = (D[47] & 0x10) >> 4 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Sol B (B1) Return | CDACTSR2 | 47 | 0x20 | raw = (D[47] & 0x20) >> 5 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Sol A (B2) Return | CDACTSR3 | 47 | 0x40 | raw = (D[47] & 0x40) >> 6 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rear Rocker Arm Oil Pressure Switch | CDACTM1 | 49 | 0x01 | raw = (D[49] & 0x01) >> 0 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Front Rocker Arm Oil Pressure Switch | CDACTM2 | 49 | 0x02 | raw = (D[49] & 0x02) >> 1 |
| 22/2615 | CANFI data packet 2615 | L640 | 22 26 15 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | VPS Status | NDACTCYL | 50 | 0xFF | raw = D[50] |
| 22/2616 | CANFI data packet 2616 | HDS only | 22 26 16 | — | 3 | — | — | — | HDS | TMU Brake Pressure | TMUCLOPAW | 6 | 0xFF | raw = D[6] |
| 22/2616 | CANFI data packet 2616 | HDS only | 22 26 16 | — | 3 | — | — | — | HDS | TMU Brake Pressure | TMUCLOPAW | 7 | 0xFF | raw = D[7] |
| 22/2616 | CANFI data packet 2616 | HDS only | 22 26 16 | — | 3 | — | — | — | HDS | TMU Brake Pressure Voltage | POILTMU | 8 | 0xFF | raw = D[8] |
| 22/2616 | CANFI data packet 2616 | HDS only | 22 26 16 | — | 3 | — | — | — | HDS | TMU EOP Speed | RTEOPOUTAW | 10 | 0xFF | raw = D[10] |
| 22/2616 | CANFI data packet 2616 | HDS only | 22 26 16 | — | 3 | — | — | — | HDS | TMU EOP Speed | RTEOPOUTAW | 11 | 0xFF | raw = D[11] |
| 22/2616 | CANFI data packet 2616 | HDS only | 22 26 16 | — | 3 | — | — | — | HDS | TMU Hi/Lo Solenoid Signal | OPHLSRAW | 15 | 0x20 | raw = (D[15] & 0x20) >> 5 |
| 22/2616 | CANFI data packet 2616 | HDS only | 22 26 16 | — | 3 | — | — | — | HDS | TMU Brake Solenoid Signal | BKSRAW | 15 | 0x80 | raw = (D[15] & 0x80) >> 7 |
| 22/2617 | CANFI data packet 2617 | HDS only | 22 26 17 | — | 3 | — | — | — | HDS | TC Boost Pressure Sensor Bank2 | P3B2 | 22 | 0xFF | raw = D[22] |
| 22/2617 | CANFI data packet 2617 | HDS only | 22 26 17 | — | 3 | — | — | — | HDS | TC Boost Pressure Bank2 | TCBPB2 | 23 | 0xFF | raw = D[23] |
| 22/2617 | CANFI data packet 2617 | HDS only | 22 26 17 | — | 3 | — | — | — | HDS | TC Boost Pressure Bank2 | TCBPB2 | 24 | 0xFF | raw = D[24] |
| 22/2617 | CANFI data packet 2617 | HDS only | 22 26 17 | — | 3 | — | — | — | HDS | CMP Ctrl Bank2 | VTCANGLB2 | 29 | 0xFF | raw = D[29] |
| 22/2617 | CANFI data packet 2617 | HDS only | 22 26 17 | — | 3 | — | — | — | HDS | MAF SENSOR Bank1 | GAIRB1 | 30 | 0xFF | raw = D[30] |
| 22/2617 | CANFI data packet 2617 | HDS only | 22 26 17 | — | 3 | — | — | — | HDS | MAF SENSOR Bank1 | GAIRB1 | 31 | 0xFF | raw = D[31] |
| 22/2617 | CANFI data packet 2617 | HDS only | 22 26 17 | — | 3 | — | — | — | HDS | MAF SENSOR Bank2 | GAIRB2 | 32 | 0xFF | raw = D[32] |
| 22/2617 | CANFI data packet 2617 | HDS only | 22 26 17 | — | 3 | — | — | — | HDS | MAF SENSOR Bank2 | GAIRB2 | 33 | 0xFF | raw = D[33] |
| 22/2617 | CANFI data packet 2617 | HDS only | 22 26 17 | — | 3 | — | — | — | HDS | IAT Sensor Bank2 | TAB2 | 34 | 0xFF | raw = D[34] |
| 22/2617 | CANFI data packet 2617 | HDS only | 22 26 17 | — | 3 | — | — | — | HDS | IAT Sensor Bank2 | IATB2 | 35 | 0xFF | raw = D[35] |
| 22/2617 | CANFI data packet 2617 | HDS only | 22 26 17 | — | 3 | — | — | — | HDS | TP Sensor A Bank2 | TH1B2 | 38 | 0xFF | raw = D[38] |
| 22/2617 | CANFI data packet 2617 | HDS only | 22 26 17 | — | 3 | — | — | — | HDS | TP Sensor B Bank2 | TH2B2 | 39 | 0xFF | raw = D[39] |
| 22/2617 | CANFI data packet 2617 | HDS only | 22 26 17 | — | 3 | — | — | — | HDS | Throttle VLV Bank2 | RELTHWB2 | 40 | 0xFF | raw = D[40] |
| 22/2617 | CANFI data packet 2617 | HDS only | 22 26 17 | — | 3 | — | — | — | HDS | Throttle VLV Bank2 | RELTHWB2 | 41 | 0xFF | raw = D[41] |
| 22/261A | CANFI data packet 261A | HDS only | 22 26 1A | — | 3 | — | — | — | HDS | Primary O2 Sensor / Primary HO2S (Sensor1) | PVO2 | 6 | 0xFF | raw = D[6] |
| 22/261A | CANFI data packet 261A | HDS only | 22 26 1A | — | 3 | — | — | — | HDS | Oil Temperature sensor | TOILG | 8 | 0xFF | raw = D[8] |
| 22/261A | CANFI data packet 261A | HDS only | 22 26 1A | — | 3 | — | — | — | HDS | Oil Temperature | TOILPHYG | 9 | 0xFF | raw = D[9] |
| 22/261A | CANFI data packet 261A | HDS only | 22 26 1A | — | 3 | — | — | — | HDS | Intake air temperature sensor(voltage) | TBST | 10 | 0xFF | raw = D[10] |
| 22/261A | CANFI data packet 261A | HDS only | 22 26 1A | — | 3 | — | — | — | HDS | Intake air temperature sensor(temperature) | TBSTPHY | 11 | 0xFF | raw = D[11] |
| 22/261A | CANFI data packet 261A | HDS only | 22 26 1A | — | 3 | — | — | — | HDS | Variable capacity engine oil pump output | SOLOILV | 14 | 0x01 | raw = (D[14] & 0x01) >> 0 |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | Engine Speed | NE | 6 | 0xFF | raw = D[6] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | Engine Speed | NE | 7 | 0xFF | raw = D[7] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | TP Sensor | ABSTH | 8 | 0xFF | raw = D[8] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | REL TP Sensor | RELTH | 9 | 0xFF | raw = D[9] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | ECT Sensor 1 | TW | 10 | 0xFF | raw = D[10] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | ECT Sensor 1 | ECT | 11 | 0xFF | raw = D[11] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | IAT Sensor (1) | TA | 12 | 0xFF | raw = D[12] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | IAT Sensor (1) | IAT | 13 | 0xFF | raw = D[13] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | MAP Sensor | PB | 14 | 0xFF | raw = D[14] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | MAP Sensor | MAP | 15 | 0xFF | raw = D[15] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | Baro Sensor | PA | 16 | 0xFF | raw = D[16] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | Baro Sensor | BARO | 17 | 0xFF | raw = D[17] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | Vehicle Speed | VSP | 18 | 0xFF | raw = D[18] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | CLV | CLV | 19 | 0xFF | raw = D[19] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | Spark Advance | IG | 21 | 0xFF | raw = D[21] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | Battery | VB | 22 | 0xFF | raw = D[22] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | F Injector | TOUT | 24 | 0xFF | raw = D[24] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | F Injector | TOUT | 25 | 0xFF | raw = D[25] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | EGR Valve Position Sensor (EGR Vls) | LIFT | 26 | 0xFF | raw = D[26] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | EGR L Command | LCMD | 27 | 0xFF | raw = D[27] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | MAF Sensor | AFM | 33 | 0xFF | raw = D[33] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | MAF Sensor | GAIR | 34 | 0xFF | raw = D[34] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | MAF Sensor | GAIR | 35 | 0xFF | raw = D[35] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | Spark Advance Exhaust Side | IGSP | 36 | 0xFF | raw = D[36] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | Rocker Arm Oil Pressure Sensor | EOPSPHY | 44 | 0xFF | raw = D[44] |
| 22/2620 | CANFI data packet 2620 | L640 | 22 26 20 | — | 3 | 62 26 20 + D[0..51] | 55 when appended | None in recovered handler | HDS | Rocker Arm Oil Pressure Sensor | EOPSPHY | 45 | 0xFF | raw = D[45] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor | XILAF | 6 | 0xFF | raw = D[6] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor | XILAF | 7 | 0xFF | raw = D[7] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Lambda | LAMBDA | 8 | 0xFF | raw = D[8] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Lambda | LAMBDA | 9 | 0xFF | raw = D[9] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB (ST Fuel Trim) | KLAF | 10 | 0xFF | raw = D[10] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB AVE (LT Fuel Trim) | KLAFAVE | 11 | 0xFF | raw = D[11] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Lambda Cmd | CMDEQRAT | 12 | 0xFF | raw = D[12] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB Cmd | CMDEQRAT/KCMD | 12 | 0xFF | raw = D[12] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Lambda Cmd | CMDEQRAT | 13 | 0xFF | raw = D[13] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB Cmd | CMDEQRAT/KCMD | 13 | 0xFF | raw = D[13] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | FSS | FSS | 14 | 0xFF | raw = D[14] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S S2 | SVO2 | 15 | 0xFF | raw = D[15] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor B1 | XILAF-B1 | 18 | 0xFF | raw = D[18] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor B1 | XILAF-B1 | 19 | 0xFF | raw = D[19] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B1 Lambda | LAMBDA-B1 | 20 | 0xFF | raw = D[20] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B1 Lambda | LAMBDA-B1 | 21 | 0xFF | raw = D[21] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | ST Fuel Trim B1 | KLAF-B1 | 22 | 0xFF | raw = D[22] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB AVE(LT Fuel Trim) B1 | KLAFAVE-B1 | 23 | 0xFF | raw = D[23] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B1 Lambda Cmd | CMDEQRAT-B1 | 24 | 0xFF | raw = D[24] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB Cmd B1 | CMDEQRAT-B1/KCMD | 24 | 0xFF | raw = D[24] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B1 Lambda Cmd | CMDEQRAT-B1 | 25 | 0xFF | raw = D[25] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB Cmd B1 | CMDEQRAT-B1/KCMD | 25 | 0xFF | raw = D[25] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | FSS B1 | FSS-B1 | 26 | 0xFF | raw = D[26] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S B1 S2 | SVO2-B1 | 27 | 0xFF | raw = D[27] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor B2 | XILAF-B2 | 30 | 0xFF | raw = D[30] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor B2 | XILAF-B2 | 31 | 0xFF | raw = D[31] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B2 Lambda | LAMBDA-B2 | 32 | 0xFF | raw = D[32] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B2 Lambda | LAMBDA-B2 | 33 | 0xFF | raw = D[33] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | ST Fuel Trim B2 | KLAF-B2 | 34 | 0xFF | raw = D[34] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB AVE(LT Fuel Trim) B2 | KLAFAVE-B2 | 35 | 0xFF | raw = D[35] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B2 Lambda Cmd | CMDEQRAT-B2 | 36 | 0xFF | raw = D[36] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB Cmd B2 | CMDEQRAT-B2/KCMD | 36 | 0xFF | raw = D[36] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | MAF Sensor (Hi Res) | GAIRCYL | 36 | 0xFF | raw = D[36] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF B2 Lambda Cmd | CMDEQRAT-B2 | 37 | 0xFF | raw = D[37] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | AF FB Cmd B2 | CMDEQRAT-B2/KCMD | 37 | 0xFF | raw = D[37] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | MAF Sensor (Hi Res) | GAIRCYL | 37 | 0xFF | raw = D[37] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | FSS B2 | FSS-B2 | 38 | 0xFF | raw = D[38] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S B2 S2 | SVO2-B2 | 39 | 0xFF | raw = D[39] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Alcohol Content Learned Value | KFKIND | 46 | 0xFF | raw = D[46] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | Subfuel Solenoid Operation | FFVSTDTY | 47 | 0xFF | raw = D[47] |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | Engine Cold Start Condition | FFVCSC | 51 | 0x01 | raw = (D[51] & 0x01) >> 0 |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | REFLECTION  OF THE AFP | KREFBSON | 51 | 0x08 | raw = (D[51] & 0x08) >> 3 |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | FFVRFUEL | FFVRFUEL | 51 | 0x20 | raw = (D[51] & 0x20) >> 5 |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | ACLRDY | ACLRDY | 51 | 0x40 | raw = (D[51] & 0x40) >> 6 |
| 22/2621 | CANFI data packet 2621 | L640 | 22 26 21 | — | 3 | 62 26 21 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Alcohol Content Learned Condition | ACLEND | 51 | 0x80 | raw = (D[51] & 0x80) >> 7 |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | APP Sensor A | APPS1 | 6 | 0xFF | raw = D[6] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | APP Sensor B | APPS2 | 7 | 0xFF | raw = D[7] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | APP Sensor | APP | 8 | 0xFF | raw = D[8] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | APP Sensor | APP | 9 | 0xFF | raw = D[9] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | TP Sensor A | TH-1 | 10 | 0xFF | raw = D[10] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | TP Sensor B | TH-2 | 11 | 0xFF | raw = D[11] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | Throttle VLV | RELTHW | 12 | 0xFF | raw = D[12] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | Throttle VLV | RELTHW | 13 | 0xFF | raw = D[13] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | Target TH VLV | THO | 14 | 0xFF | raw = D[14] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | Target TH VLV | THO | 15 | 0xFF | raw = D[15] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Target TH | THICMD | 18 | 0xFF | raw = D[18] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Target TH | THICMD | 19 | 0xFF | raw = D[19] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | Rocker Arm Oil Control Sol.  1 | VTS1 | 27 | 0x01 | raw = (D[27] & 0x01) >> 0 |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | Solenoid 1 Return Signal | VTS1R | 27 | 0x02 | raw = (D[27] & 0x02) >> 1 |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | ROCKER ARM OIL CONTROL SOL.  2 | VTS2 | 27 | 0x04 | raw = (D[27] & 0x04) >> 2 |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | SOLENOID 2 RETURN SIGNAL | VTS2R | 27 | 0x08 | raw = (D[27] & 0x08) >> 3 |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | Rocker Arm Oil Pressure Switch | VTMACD | 27 | 0x20 | raw = (D[27] & 0x20) >> 5 |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | F Injector Active Side | TOUTA | 29 | 0xFF | raw = D[29] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | F Injector Active Side | TOUTA | 30 | 0xFF | raw = D[30] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | (Rocker Arm) Oil Pressure Sensor (B) | POIL_B | 31 | 0xFF | raw = D[31] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | (Rocker Arm) Oil Pressure Sensor (B) | EOP | 32 | 0xFF | raw = D[32] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | (Rocker Arm) Oil Pressure Sensor (B) | EOP | 33 | 0xFF | raw = D[33] |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | VPS SOL | CDACTS | 35 | 0x01 | raw = (D[35] & 0x01) >> 0 |
| 22/2622 | CANFI data packet 2622 | L640 | 22 26 22 | — | 3 | 62 26 22 + D[0..51] | 55 when appended | None in recovered handler | HDS | Rocker Arm Oil Pressure Switch B (Bank 1) | VCMCDACT | 35 | 0x04 | raw = (D[35] & 0x04) >> 2 |
| 22/2623 | CANFI data packet 2623 | L640 | 22 26 23 | — | 3 | 62 26 23 + D[0..51] | 55 when appended | None in recovered handler | HDS | EVAP PC Duty | DPCS | 6 | 0xFF | raw = D[6] |
| 22/2623 | CANFI data packet 2623 | L640 | 22 26 23 | — | 3 | 62 26 23 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Level | FLI | 11 | 0xFF | raw = D[11] |
| 22/2623 | CANFI data packet 2623 | L640 | 22 26 23 | — | 3 | 62 26 23 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Press. | PF2G | 22 | 0xFF | raw = D[22] |
| 22/2623 | CANFI data packet 2623 | L640 | 22 26 23 | — | 3 | 62 26 23 + D[0..51] | 55 when appended | None in recovered handler | HDS | FP Sensor | PF2 | 23 | 0xFF | raw = D[23] |
| 22/2623 | CANFI data packet 2623 | L640 | 22 26 23 | — | 3 | 62 26 23 + D[0..51] | 55 when appended | None in recovered handler | HDS | FP Sensor | PF2PHY | 24 | 0xFF | raw = D[24] |
| 22/2623 | CANFI data packet 2623 | L640 | 22 26 23 | — | 3 | 62 26 23 + D[0..51] | 55 when appended | None in recovered handler | HDS | FP Sensor | PF2PHY | 25 | 0xFF | raw = D[25] |
| 22/2623 | CANFI data packet 2623 | L640 | 22 26 23 | — | 3 | 62 26 23 + D[0..51] | 55 when appended | None in recovered handler | HDS | FT Sensor | TF2 | 28 | 0xFF | raw = D[28] |
| 22/2623 | CANFI data packet 2623 | L640 | 22 26 23 | — | 3 | 62 26 23 + D[0..51] | 55 when appended | None in recovered handler | HDS | FT Sensor | TF2PHY | 29 | 0xFF | raw = D[29] |
| 22/2623 | CANFI data packet 2623 | L640 | 22 26 23 | — | 3 | 62 26 23 + D[0..51] | 55 when appended | None in recovered handler | HDS | FTP Sensor (Fine) | EVAPVP | 46 | 0xFF | raw = D[46] |
| 22/2623 | CANFI data packet 2623 | L640 | 22 26 23 | — | 3 | 62 26 23 + D[0..51] | 55 when appended | None in recovered handler | HDS | FTP Sensor (Fine) | EVAPVP | 47 | 0xFF | raw = D[47] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Vehicle Status | STIMAOP | 6 | 0xFF | raw = D[6] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Driving Status | TQRMODE | 7 | 0xFF | raw = D[7] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | A/C Compressor Speed Command | NECOMPTG | 10 | 0xFF | raw = D[10] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | A/C Compressor Speed Command | NECOMPTG | 11 | 0xFF | raw = D[11] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | A/C Compressor Speed | NECOMP | 12 | 0xFF | raw = D[12] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | A/C Compressor Speed | NECOMP | 13 | 0xFF | raw = D[13] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | A/C Power Consumption | PWDHBAC | 14 | 0xFF | raw = D[14] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | A/C Power Consumption | PWDHBAC | 15 | 0xFF | raw = D[15] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IMA Output Command | PWBEMREQ | 16 | 0xFF | raw = D[16] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IMA Output Command | PWBEMREQ | 17 | 0xFF | raw = D[17] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | SOC | QBATC | 18 | 0xFF | raw = D[18] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | SOC | QBATC | 19 | 0xFF | raw = D[19] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IMA Output | PWBATF | 20 | 0xFF | raw = D[20] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IMA Output | PWBATF | 21 | 0xFF | raw = D[21] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IMA Battery Temperature | TBATC | 22 | 0xFF | raw = D[22] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Driving Status | TSTQMMODE | 25 | 0xFF | raw = D[25] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TQMBKLMT | TQMBKLMT | 34 | 0xFF | raw = D[34] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TQMBKLMT | TQMBKLMT | 35 | 0xFF | raw = D[35] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Regeneration Torque | TQMBKREQ | 36 | 0xFF | raw = D[36] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Regeneration Torque | TQMBKREQ | 37 | 0xFF | raw = D[37] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Target Engine Torque | TQECMD | 44 | 0xFF | raw = D[44] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Target Engine Torque | TQECMD | 45 | 0xFF | raw = D[45] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Requested IMA Motor Torque | TQMCMDDC | 48 | 0xFF | raw = D[48] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Requested IMA Motor Torque | TQMCMDDC | 49 | 0xFF | raw = D[49] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IMA Motor Torque | TQMACT | 50 | 0xFF | raw = D[50] |
| 22/2624 | CANFI data packet 2624 | L640 | 22 26 24 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IMA Motor Torque | TQMACT | 51 | 0xFF | raw = D[51] |
| 22/2625 | CANFI data packet 2625 | L640 | 22 26 25 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TC Boost Pressure Sensor | P3 | 6 | 0xFF | raw = D[6] |
| 22/2625 | CANFI data packet 2625 | L640 | 22 26 25 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TC Boost Pressure | TCBP | 7 | 0xFF | raw = D[7] |
| 22/2625 | CANFI data packet 2625 | L640 | 22 26 25 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TC Boost Pressure | TCBP | 8 | 0xFF | raw = D[8] |
| 22/2625 | CANFI data packet 2625 | L640 | 22 26 25 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Neutral Position Sensor 1 | NPS1 | 26 | 0xFF | raw = D[26] |
| 22/2625 | CANFI data packet 2625 | L640 | 22 26 25 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Pressure Sensor A | POIL2 | 30 | 0xFF | raw = D[30] |
| 22/2625 | CANFI data packet 2625 | L640 | 22 26 25 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Pressure Sensor A | EOP2 | 31 | 0xFF | raw = D[31] |
| 22/2625 | CANFI data packet 2625 | L640 | 22 26 25 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Pressure Sensor A | EOP2 | 32 | 0xFF | raw = D[32] |
| 22/2625 | CANFI data packet 2625 | L640 | 22 26 25 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Solenoid B | CSSA | 37 | 0x01 | raw = (D[37] & 0x01) >> 0 |
| 22/2625 | CANFI data packet 2625 | L640 | 22 26 25 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Solenoid B Return | CSSAR | 37 | 0x02 | raw = (D[37] & 0x02) >> 1 |
| 22/2625 | CANFI data packet 2625 | L640 | 22 26 25 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Solenoid A | CSSB | 37 | 0x04 | raw = (D[37] & 0x04) >> 2 |
| 22/2625 | CANFI data packet 2625 | L640 | 22 26 25 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rocker Arm Oil Control Solenoid A Return | CSSBR | 37 | 0x08 | raw = (D[37] & 0x08) >> 3 |
| 22/2625 | CANFI data packet 2625 | L640 | 22 26 25 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Rear Rocker Arm Oil Pressure Switch | CDACTM1 | 49 | 0x01 | raw = (D[49] & 0x01) >> 0 |
| 22/2625 | CANFI data packet 2625 | L640 | 22 26 25 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Front Rocker Arm Oil Pressure Switch | CDACTM2 | 49 | 0x02 | raw = (D[49] & 0x02) >> 1 |
| 22/2625 | CANFI data packet 2625 | L640 | 22 26 25 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | VPS Status | NDACTCYL | 50 | 0xFF | raw = D[50] |
| 22/2627 | CANFI data packet 2627 | HDS only | 22 26 27 | — | 3 | — | — | — | HDS | TC Boost Pressure Sensor Bank2 | P3B2 | 22 | 0xFF | raw = D[22] |
| 22/2627 | CANFI data packet 2627 | HDS only | 22 26 27 | — | 3 | — | — | — | HDS | TC Boost Pressure Bank2 | TCBPB2 | 23 | 0xFF | raw = D[23] |
| 22/2627 | CANFI data packet 2627 | HDS only | 22 26 27 | — | 3 | — | — | — | HDS | TC Boost Pressure Bank2 | TCBPB2 | 24 | 0xFF | raw = D[24] |
| 22/2627 | CANFI data packet 2627 | HDS only | 22 26 27 | — | 3 | — | — | — | HDS | MAF SENSOR Bank1 | GAIRB1 | 30 | 0xFF | raw = D[30] |
| 22/2627 | CANFI data packet 2627 | HDS only | 22 26 27 | — | 3 | — | — | — | HDS | MAF SENSOR Bank1 | GAIRB1 | 31 | 0xFF | raw = D[31] |
| 22/2627 | CANFI data packet 2627 | HDS only | 22 26 27 | — | 3 | — | — | — | HDS | MAF SENSOR Bank2 | GAIRB2 | 32 | 0xFF | raw = D[32] |
| 22/2627 | CANFI data packet 2627 | HDS only | 22 26 27 | — | 3 | — | — | — | HDS | MAF SENSOR Bank2 | GAIRB2 | 33 | 0xFF | raw = D[33] |
| 22/2627 | CANFI data packet 2627 | HDS only | 22 26 27 | — | 3 | — | — | — | HDS | IAT Sensor Bank2 | TAB2 | 34 | 0xFF | raw = D[34] |
| 22/2627 | CANFI data packet 2627 | HDS only | 22 26 27 | — | 3 | — | — | — | HDS | IAT Sensor Bank2 | IATB2 | 35 | 0xFF | raw = D[35] |
| 22/2627 | CANFI data packet 2627 | HDS only | 22 26 27 | — | 3 | — | — | — | HDS | TP Sensor A Bank2 | TH1B2 | 38 | 0xFF | raw = D[38] |
| 22/2627 | CANFI data packet 2627 | HDS only | 22 26 27 | — | 3 | — | — | — | HDS | TP Sensor B Bank2 | TH2B2 | 39 | 0xFF | raw = D[39] |
| 22/262A | CANFI data packet 262A | HDS only | 22 26 2A | — | 3 | — | — | — | HDS | Primary O2 Sensor / Primary HO2S (Sensor1) | PVO2 | 6 | 0xFF | raw = D[6] |
| 22/2630 | CANFI data packet 2630 | L640 | 22 26 30 | — | 3 | 62 26 30 | 3 | None in recovered handler | HDS | FRZDTC | FRZDTC | 0 | 0xFF | raw = D[0] |
| 22/2630 | CANFI data packet 2630 | L640 | 22 26 30 | — | 3 | 62 26 30 | 3 | None in recovered handler | HDS | FRZDTC | FRZDTC | 1 | 0xFF | raw = D[1] |
| 22/2630 | CANFI data packet 2630 | L640 | 22 26 30 | — | 3 | 62 26 30 | 3 | None in recovered handler | HDS | FRZDTC | FRZDTC | 2 | 0xFF | raw = D[2] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d00..d02 | — | D[0..2] | — | 80 1F FF [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d03 | 0xFFF94FFA, 0xFFF9504C | D[3] | — | C0 &#124; (0xFFF94FFA?30:00) &#124; (0xFFF9504C?03:00) [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d04 | 0xFFF9504C | D[4] | — | 0xFFF9504C!=0 ? F7 : 07 [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d05 | — | D[5] | — | F0 [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d06 | 0xFFF83588 | D[6] | — | sat_u8(U16[0xFFF83588]) after helper 0x000F7DA0 [PROVEN DTC summary/count] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d07..d16 | — | D[7..16] | — | all zero [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d17..d18 | 0xFFF841C0 | D[17..18] | — | BE16(U16[0xFFF841C0]) [PROVEN; also OBD Mode01 PID21 counter] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d19..d20 | 0xFFF835AC | D[19..20] | — | BE16(U16[0xFFF835AC]) [PROVEN; also OBD Mode01 PID31 counter] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d21 | 0xFFF95061 | D[21] | — | 0xFFF95061!=0 ? 1F : 1E [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d22 | 0xFFF95A97, 0xFFF95AD1, 0xFFF95C1C, 0xFFF95C31, 0xFFF96324 | D[22] | — | bit4=0xFFF95C1C; bit3=0xFFF95C31; bit2=0xFFF95A97; bit1=(0xFFF95AD1==0); bit0=0xFFF96324 [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d23 | — | D[23] | — | 01 [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d24 | 0xFFF94321 | D[24] | — | 0xFFF94321!=0 ? 01 : 00 [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d25 | — | D[25] | — | 04 [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d26 | 0xFFF94757, 0xFFF94758 | D[26] | — | (0xFFF94757&#124;0xFFF94758)!=0 ? 04 : 00 [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d27 | 0xFFF95056 | D[27] | — | 0xFFF95056!=0 ? 40 : 00 [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d28 | 0xFFF95D62 | D[28] | — | 0xFFF95D62!=0 ? 40 : 00 [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d29 | 0xFFF91426 | D[29] | — | (U16[0xFFF91426]&F000)==1000 ? 83 : 82 [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d30 | 0xFFF87445, 0xFFF94759, 0xFFF9476D | D[30] | — | bit7=0xFFF87445; bit1=0xFFF9476D; bit0=0xFFF94759 [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d31 | 0xFFF96276 | D[31] | — | U8[0xFFF96276] [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d32..d33 | 0xFFF8473A | D[32..33] | — | BE16(U16[0xFFF8473A]) [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d34..d35 | — | D[34..35] | — | 00 00 [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d36..d37 | 0xFFF91AA0 | D[36..37] | — | BE16(U16[0xFFF91AA0]) [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d38..d39 | 0xFFF91A98 | D[38..39] | — | BE16(U16[0xFFF91A98]) [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d40..d41 | 0xFFF91AAE | D[40..41] | — | BE16(U16[0xFFF91AAE]) [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d42 | — | D[42] | — | 00 [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d43..d45 | 0xFFF8CD98 | D[43..45] | — | U24_BE(min(U32[0xFFF8CD98],999999)) [PROVEN transform] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d46..d47 | 0xFFF928F8 | D[46..47] | — | BE16(U16[0xFFF928F8]) [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d48..d49 | 0xFFF8CFA0 | D[48..49] | — | BE16(min(65535,trunc0(S32[0xFFF8CFA0]/10))) [PROVEN transform; negative domain TBD] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d50..d53 | — | D[50..53] | — | 00 00 00 00 [PROVEN] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | Firmware | MIL Status | — | 6 | — | value = (D[6] >> 7) & 1 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | NTRBCD | NTRBCD | 6 | 0x01 | raw = (D[6] & 0x01) >> 0 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | NTRBCD | NTRBCD | 6 | 0x02 | raw = (D[6] & 0x02) >> 1 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | NTRBCD | NTRBCD | 6 | 0x04 | raw = (D[6] & 0x04) >> 2 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | NTRBCD | NTRBCD | 6 | 0x08 | raw = (D[6] & 0x08) >> 3 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | NTRBCD | NTRBCD | 6 | 0x10 | raw = (D[6] & 0x10) >> 4 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | NTRBCD | NTRBCD | 6 | 0x20 | raw = (D[6] & 0x20) >> 5 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | NTRBCD | NTRBCD | 6 | 0x40 | raw = (D[6] & 0x40) >> 6 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | MIL Status | MILSTAT | 6 | 0x80 | raw = (D[6] & 0x80) >> 7 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | DRDNS-1 | DRDNS-1 | 8 | 0xFF | raw = D[8] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | DRDNS-2 | DRDNS-2 | 10 | 0xFF | raw = D[10] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | DRDNS-3 | DRDNS-3 | 12 | 0xFF | raw = D[12] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | RDYEVPSLK | RDYEVPSLK | 14 | 0x01 | raw = (D[14] & 0x01) >> 0 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | RDYEVPLLK | RDYEVPLLK | 14 | 0x02 | raw = (D[14] & 0x02) >> 1 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | RDYPGFLW | RDYPGFLW | 14 | 0x04 | raw = (D[14] & 0x04) >> 2 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | RDYPCSOPN | RDYPCSOPN | 14 | 0x08 | raw = (D[14] & 0x08) >> 3 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | RDYVSVCLS | RDYVSVCLS | 14 | 0x10 | raw = (D[14] & 0x10) >> 4 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | RDYLAFAB2 | RDYLAFAB2 | 14 | 0x20 | raw = (D[14] & 0x20) >> 5 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | RDYLAFCB2 | RDYLAFCB2 | 14 | 0x40 | raw = (D[14] & 0x40) >> 6 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | DRDNS-4 | DRDNS-4 | 14 | 0xFF | raw = D[14] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | RDYPGFWTB | RDYPGFWTB | 16 | 0x01 | raw = (D[16] & 0x01) >> 0 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | RDYPGFWTB2 | RDYPGFWTB2 | 16 | 0x02 | raw = (D[16] & 0x02) >> 1 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | MIL Dist | DSTMIL | 17 | 0xFF | raw = D[17] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | MIL Dist | DSTMIL | 18 | 0xFF | raw = D[18] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | VTC Status | VTCACT | 22 | 0x01 | raw = (D[22] & 0x01) >> 0 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Idling | IDLING | 22 | 0x02 | raw = (D[22] & 0x02) >> 1 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Idling Throttle Position Learn | IDLBLC | 22 | 0x04 | raw = (D[22] & 0x04) >> 2 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Fuel Cut | FC | 22 | 0x08 | raw = (D[22] & 0x08) >> 3 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Fuel Cut Decel | FCDEC | 22 | 0x10 | raw = (D[22] & 0x10) >> 4 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | VTC Status | VTCSTP | 22 | 0x20 | raw = (D[22] & 0x20) >> 5 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | SCS | SCS | 24 | 0x01 | raw = (D[24] & 0x01) >> 0 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | QCKMIL | QCKMIL | 26 | 0x01 | raw = (D[26] & 0x01) >> 0 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | BASADJ | BASADJ | 26 | 0x02 | raw = (D[26] & 0x02) >> 1 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | ISTPIM | ISTPIM | 26 | 0x08 | raw = (D[26] & 0x08) >> 3 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | KSOK | KSOK | 28 | 0x01 | raw = (D[28] & 0x01) >> 0 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Knock Sensor | KSBOK | 28 | 0x40 | raw = (D[28] & 0x40) >> 6 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | DNAT40 | DNAT40 | 28 | 0x80 | raw = (D[28] & 0x80) >> 7 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | All Injector Deactivation Mode | AINJDACT | 30 | 0x80 | raw = (D[30] & 0x80) >> 7 |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | OBRTRGMD | OBRTRGMD | 31 | 0xFF | raw = D[31] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Engine Oil Life | ROLF | 32 | 0xFF | raw = D[32] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Engine Oil Life | ROLF | 33 | 0xFF | raw = D[33] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | MAF Sensor (Hi Res) | GAIRCYL | 36 | 0xFF | raw = D[36] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | MAF Sensor (Hi Res) | GAIRCYL | 37 | 0xFF | raw = D[37] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | GAIRAVE | GAIRAVE | 38 | 0xFF | raw = D[38] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | GAIRAVE | GAIRAVE | 39 | 0xFF | raw = D[39] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | MAPAVE | MAPAVE | 40 | 0xFF | raw = D[40] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | MAPAVE | MAPAVE | 41 | 0xFF | raw = D[41] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | MAF Sensor | PLSTAFM | 42 | 0xFF | raw = D[42] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Total Mileage | DSTODO | 43 | 0xFF | raw = D[43] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Total Mileage | DSTODO | 44 | 0xFF | raw = D[44] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Total Mileage | DSTODO | 45 | 0xFF | raw = D[45] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Eng Run Time | ERUNTM | 46 | 0xFF | raw = D[46] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Eng Run Time | ERUNTM | 47 | 0xFF | raw = D[47] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Drive Dist | DSTTRV | 48 | 0xFF | raw = D[48] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Drive Dist | DSTTRV | 49 | 0xFF | raw = D[49] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | DSTIPTL | DSTIPTL | 50 | 0xFF | raw = D[50] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | DSTIPTL | DSTIPTL | 51 | 0xFF | raw = D[51] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Integrated Value of Fuel Consumption | TITRIP | 52 | 0xFF | raw = D[52] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Fuel Consumption For 1DC | TTRIP | 52 | 0xFF | raw = D[52] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Integrated Value of Fuel Consumption | TITRIP | 53 | 0xFF | raw = D[53] |
| 22/2660 | MIL Status | L640 | 22 26 60 | — | 3 | 62 26 60 + D[0..53] | 57 when appended | None in recovered handler | HDS | Fuel Consumption For 1DC | TTRIP | 53 | 0xFF | raw = D[53] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | STARTER SWITCH | STS | 7 | 0x01 | raw = (D[7] & 0x01) >> 0 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | PSP Switch | PSW | 7 | 0x04 | raw = (D[7] & 0x04) >> 2 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | PNP Switch | ATNP | 7 | 0x10 | raw = (D[7] & 0x10) >> 4 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Clutch Pedal Position Switch A | CLSW | 9 | 0x02 | raw = (D[9] & 0x02) >> 1 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | NP Switch | NSW | 9 | 0x04 | raw = (D[9] & 0x04) >> 2 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Clutch Pedal Position Switch A (C) | CLSWEG | 9 | 0x08 | raw = (D[9] & 0x08) >> 3 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Status of Neutral Position | NPOK | 9 | 0x10 | raw = (D[9] & 0x10) >> 4 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Clutch Pedal Position Switch D | CLSWIS | 9 | 0x20 | raw = (D[9] & 0x20) >> 5 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Clutch Pedal Position Switch B Status | CLSWCC | 9 | 0x40 | raw = (D[9] & 0x40) >> 6 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | EPS Signal | EPSLD | 11 | 0x10 | raw = (D[11] & 0x10) >> 4 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Clutch Engagement Information (Cruise Control) | CLEPBCC | 11 | 0x20 | raw = (D[11] & 0x20) >> 5 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Clutch Engagement Information (Idling Stop) | CLEPBIS | 11 | 0x40 | raw = (D[11] & 0x40) >> 6 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Clutch Engagement Information (SIL) | CLEPBSIL | 11 | 0x80 | raw = (D[11] & 0x80) >> 7 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | A/T R Switch | ATPR | 13 | 0x01 | raw = (D[13] & 0x01) >> 0 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Back-Up Light Switch | RVSSW | 13 | 0x02 | raw = (D[13] & 0x02) >> 1 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | IG1 Level | IG1LVL | 15 | 0x01 | raw = (D[15] & 0x01) >> 0 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Oil Pressure Switch | OPSWR | 15 | 0x10 | raw = (D[15] & 0x10) >> 4 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Output Signal for Meter Warning | OPSENWARN | 15 | 0x20 | raw = (D[15] & 0x20) >> 5 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | ELD Sensor Output Voltage | ELD | 16 | 0xFF | raw = D[16] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | ELD (Electric Load Value) | ELOAD | 17 | 0xFF | raw = D[17] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | ECONO Light | ECONO | 19 | 0x01 | raw = (D[19] & 0x01) >> 0 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | SIL-U | SIL-U | 19 | 0x04 | raw = (D[19] & 0x04) >> 2 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | SIL-D | SIL-D | 19 | 0x08 | raw = (D[19] & 0x08) >> 3 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | FIWARN | FIWARN | 19 | 0x80 | raw = (D[19] & 0x80) >> 7 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Mount Ctrl Sol | MCS | 25 | 0x01 | raw = (D[25] & 0x01) >> 0 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Air Pump Relay | APR | 27 | 0x01 | raw = (D[27] & 0x01) >> 0 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Air Control Sol | SAVS | 27 | 0x02 | raw = (D[27] & 0x02) >> 1 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Air Pump Signal | VAP | 27 | 0x04 | raw = (D[27] & 0x04) >> 2 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Ixref/Qxref | IXREF | 28 | 0xFF | raw = D[28] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Target | TRGIDL | 29 | 0xFF | raw = D[29] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Target | TRGIDL | 30 | 0xFF | raw = D[30] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Learn (Idle air) | IALSTAT | 32 | 0xFF | raw = D[32] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Air Block Lean | IAIRBL | 33 | 0xFF | raw = D[33] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Air Block Lean | IAIRBL | 34 | 0xFF | raw = D[34] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | TP Sensor | THDEG | 35 | 0xFF | raw = D[35] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | THIDLL | THIDLL | 35 | 0xFF | raw = D[35] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | TP Sensor | THDEG | 36 | 0xFF | raw = D[36] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | THIDLL | THIDLL | 36 | 0xFF | raw = D[36] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Radiator Fan Control | DRFC | 37 | 0xFF | raw = D[37] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | A/C Seting Temprature | ACTMP | 38 | 0xFF | raw = D[38] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | A/C Temperature Sensor | TAC | 39 | 0xFF | raw = D[39] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | PDSW | PDSW | 41 | 0x01 | raw = (D[41] & 0x01) >> 0 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | A/C Temperature Sensor | ACET | 42 | 0xFF | raw = D[42] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | A/C Pressure | ACRP_T | 43 | 0xFF | raw = D[43] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | A/C Pressure | ACRP_T | 44 | 0xFF | raw = D[44] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Alt L Signal | ACGL | 46 | 0x01 | raw = (D[46] & 0x01) >> 0 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Alt Ctrl | ACGC | 46 | 0x02 | raw = (D[46] & 0x02) >> 1 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fan Ctrl | FANC | 46 | 0x04 | raw = (D[46] & 0x04) >> 2 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fan Low Ctrl | FANL | 46 | 0x08 | raw = (D[46] & 0x08) >> 3 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fan High Ctrl | FANH | 46 | 0x10 | raw = (D[46] & 0x10) >> 4 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Radiator Fan Relay | RFCR | 46 | 0x20 | raw = (D[46] & 0x20) >> 5 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Radiator Fan Control Module | RDRFC | 46 | 0x40 | raw = (D[46] & 0x40) >> 6 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Radiator Fan Control History | HRFCOFF | 46 | 0x80 | raw = (D[46] & 0x80) >> 7 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Starting Condition | STRCNT | 48 | 0x02 | raw = (D[48] & 0x02) >> 1 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Starter Cut Relay | RSTRCNT | 48 | 0x04 | raw = (D[48] & 0x04) >> 2 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Starter Cut Ctrl | STRCNT2 | 48 | 0x08 | raw = (D[48] & 0x08) >> 3 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Starter Cut Ctrl Return | RSTRCNT2 | 48 | 0x10 | raw = (D[48] & 0x10) >> 4 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | STRCUT | STRCUT | 48 | 0x20 | raw = (D[48] & 0x20) >> 5 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Starter Ctrl | STC | 48 | 0x80 | raw = (D[48] & 0x80) >> 7 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Starter Relay Can Signal | STENCAN | 50 | 0x01 | raw = (D[50] & 0x01) >> 0 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Starter Duty Signal Hi Mode | STENHWP | 50 | 0x02 | raw = (D[50] & 0x02) >> 1 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Starter Relay Duty Signal Condition | STENHWEN | 50 | 0x04 | raw = (D[50] & 0x04) >> 2 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Starter Relay Duty Signal | STENHW | 50 | 0x08 | raw = (D[50] & 0x08) >> 3 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Starter Relay Control | STRLYCNT | 50 | 0x10 | raw = (D[50] & 0x10) >> 4 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Starter Relay Control Return | RSTRLYCNT | 50 | 0x20 | raw = (D[50] & 0x20) >> 5 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Starter Relay Signal | STEN | 50 | 0x80 | raw = (D[50] & 0x80) >> 7 |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Estimated Electric Load Level | ELEST | 51 | 0xFF | raw = D[51] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | EPS Consumption Current | IEPSLD | 52 | 0xFF | raw = D[52] |
| 22/2661 | CANFI data packet 2661 | L640 | 22 26 61 | — | 3 | 62 26 61 + D[0..51] | 55 when appended | None in recovered handler | HDS | Starter Cut Relay | STRLD | 53 | 0xFF | raw = D[53] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | NLVLAD | NLVLAD | 6 | 0xFF | raw = D[6] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Knock Advance | KNADV | 7 | 0xFF | raw = D[7] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Knock Retard | KNRTD | 8 | 0xFF | raw = D[8] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Knock Sensor | NLSMPL | 9 | 0xFF | raw = D[9] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Knock Ctrl | KIGKREF | 10 | 0xFF | raw = D[10] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Knock Ctrl EGR | KIGKREFE | 11 | 0xFF | raw = D[11] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Catalyst Temp | TCAT | 12 | 0xFF | raw = D[12] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Catalyst Temp | TCAT | 13 | 0xFF | raw = D[13] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Catalyst Temp B1 | TCAT-B1 | 14 | 0xFF | raw = D[14] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Catalyst Temp B1 | TCAT-B1 | 15 | 0xFF | raw = D[15] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Catalyst Temp B2 | TCAT-B2 | 16 | 0xFF | raw = D[16] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Catalyst Temp B2 | TCAT-B2 | 17 | 0xFF | raw = D[17] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cata Monitor B1 | CATAGE | 18 | 0xFF | raw = D[18] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cata Monitor B1 | CATAGE | 19 | 0xFF | raw = D[19] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cata Monitor B1 | CATAGE-B1 | 20 | 0xFF | raw = D[20] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cata Monitor B1 | CATAGE-B1 | 21 | 0xFF | raw = D[21] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cata Monitor B2 | CATAGE-B2 | 22 | 0xFF | raw = D[22] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cata Monitor B2 | CATAGE-B2 | 23 | 0xFF | raw = D[23] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Main Relay (Fp) | FLR | 25 | 0x01 | raw = (D[25] & 0x01) >> 0 |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | FPCDIAG | FPCDIAG | 25 | 0x10 | raw = (D[25] & 0x10) >> 4 |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Pump Control Relay | FPCRLY | 25 | 0x20 | raw = (D[25] & 0x20) >> 5 |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | VTC Sol Duty | DVTCSOL | 28 | 0xFF | raw = D[28] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | CMP Ctrl Cmd | VTCCMD | 29 | 0xFF | raw = D[29] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | VTCABSA | VTCABSA | 30 | 0xFF | raw = D[30] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | VTCZP | VTCZP | 31 | 0xFF | raw = D[31] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | VTCABSAENAN | VTCABSAENAN | 32 | 0xFF | raw = D[32] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | VTCABSAENAN | VTCABSAENAN | 33 | 0xFF | raw = D[33] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | IAR Sol | RCS | 36 | 0x01 | raw = (D[36] & 0x01) >> 0 |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | TW Low Temp Light | TWLED1 | 36 | 0x02 | raw = (D[36] & 0x02) >> 1 |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | TW High Temp Light | TWLED2 | 36 | 0x04 | raw = (D[36] & 0x04) >> 2 |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Knock Sensor (Circuit Diag) | MBKSAD | 37 | 0xFF | raw = D[37] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Pump Control | DFPC | 38 | 0xFF | raw = D[38] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Start IAT | TA86INI | 39 | 0xFF | raw = D[39] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Start ECT | TW86INI | 40 | 0xFF | raw = D[40] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | EST ECT1 | CTW1 | 41 | 0xFF | raw = D[41] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | EST ECT1 | CTW1 | 42 | 0xFF | raw = D[42] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | EST ECT2 | CTW2 | 43 | 0xFF | raw = D[43] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | EST ECT2 | CTW2 | 44 | 0xFF | raw = D[44] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | IAT Sensor 1 Block Heater Info | BH10C | 46 | 0x10 | raw = (D[46] & 0x10) >> 4 |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | TW2INI | TW2INI | 51 | 0xFF | raw = D[51] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cmpctrl Cmd(Hi Res) | VTCCMDENAN | 52 | 0xFF | raw = D[52] |
| 22/2662 | CANFI data packet 2662 | L640 | 22 26 62 | — | 3 | 62 26 62 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cmpctrl Cmd(Hi Res) | VTCCMDENAN | 53 | 0xFF | raw = D[53] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Misfire | CMFIRE | 6 | 0xFF | raw = D[6] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Misfire | CMFIRE | 7 | 0xFF | raw = D[7] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Misfired Cyl | MFCYL | 9 | 0xFF | raw = D[9] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Multi Cylinder Misfire | MFCYLM | 11 | 0xFF | raw = D[11] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | CKP Pulser F/B Learn | KCREND | 13 | 0x01 | raw = (D[13] & 0x01) >> 0 |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | CKP Pulser F/B Learn | KCRBITS | 13 | 0x02 | raw = (D[13] & 0x02) >> 1 |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | CKP Pulser F/B Learn (High RPM) | CNLHSTAT0 | 15 | 0x01 | raw = (D[15] & 0x01) >> 0 |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | CKP Pulser F/B Learn (High RPM) | CNLHSTAT | 15 | 0xFF | raw = D[15] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | LEMFPTATF | LEMFPTATF | 19 | 0x02 | raw = (D[19] & 0x02) >> 1 |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | LEMFPTW | LEMFPTW | 19 | 0x10 | raw = (D[19] & 0x10) >> 4 |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | LEMFPFS | LEMFPFS | 19 | 0x80 | raw = (D[19] & 0x80) >> 7 |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl1 Misfire B | NMFBCYL1 | 20 | 0xFF | raw = D[20] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl1 Misfire B | NMFBCYL1 | 21 | 0xFF | raw = D[21] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl2 Misfire B | NMFBCYL2 | 22 | 0xFF | raw = D[22] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl2 Misfire B | NMFBCYL2 | 23 | 0xFF | raw = D[23] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl3 Misfire B | NMFBCYL3 | 24 | 0xFF | raw = D[24] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl3 Misfire B | NMFBCYL3 | 25 | 0xFF | raw = D[25] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl4 Misfire B | NMFBCYL4 | 26 | 0xFF | raw = D[26] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl4 Misfire B | NMFBCYL4 | 27 | 0xFF | raw = D[27] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl5 Misfire B | NMFBCYL5 | 28 | 0xFF | raw = D[28] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl5 Misfire B | NMFBCYL5 | 29 | 0xFF | raw = D[29] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl6 Misfire B | NMFBCYL6 | 30 | 0xFF | raw = D[30] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl6 Misfire B | NMFBCYL6 | 31 | 0xFF | raw = D[31] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Misfire Cycle B | NTDCB | 32 | 0xFF | raw = D[32] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Misfire Cycle B | NTDCB | 33 | 0xFF | raw = D[33] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl1 Misfire | NMFACYL1 | 34 | 0xFF | raw = D[34] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl1 Misfire | NMFACYL1 | 35 | 0xFF | raw = D[35] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl2 Misfire | NMFACYL2 | 36 | 0xFF | raw = D[36] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl2 Misfire | NMFACYL2 | 37 | 0xFF | raw = D[37] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl3 Misfire | NMFACYL3 | 38 | 0xFF | raw = D[38] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl3 Misfire | NMFACYL3 | 39 | 0xFF | raw = D[39] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl4 Misfire | NMFACYL4 | 40 | 0xFF | raw = D[40] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl4 Misfire | NMFACYL4 | 41 | 0xFF | raw = D[41] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl5 Misfire | NMFACYL5 | 42 | 0xFF | raw = D[42] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl5 Misfire | NMFACYL5 | 43 | 0xFF | raw = D[43] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl6 Misfire | NMFACYL6 | 44 | 0xFF | raw = D[44] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl6 Misfire | NMFACYL6 | 45 | 0xFF | raw = D[45] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Misfire Cycle | NTDCA | 46 | 0xFF | raw = D[46] |
| 22/2663 | CANFI data packet 2663 | L640 | 22 26 63 | — | 3 | 62 26 63 + D[0..51] | 55 when appended | None in recovered handler | HDS | Misfire Cycle | NTDCA | 47 | 0xFF | raw = D[47] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | Firmware | Cruise Indicator | — | 7 | — | value = (D[7] >> 7) & 1 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | Firmware | Brake Switch | — | 38 | — | value = (D[38] >> 0) & 1 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | Firmware | Cruise Brake Sw/Idle Stop Sw | — | 38 | — | value = (D[38] >> 2) & 1 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Sw | CRBKSW | 7 | 0x01 | raw = (D[7] & 0x01) >> 0 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cruise Master(Main) Sw | CRMSW | 7 | 0x02 | raw = (D[7] & 0x02) >> 1 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cruise Set Sw | CRSETSW | 7 | 0x04 | raw = (D[7] & 0x04) >> 2 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cruise Resume Sw | CRRESSW | 7 | 0x08 | raw = (D[7] & 0x08) >> 3 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cruise Cancel Sw | CRCANCELSW | 7 | 0x10 | raw = (D[7] & 0x10) >> 4 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Shift/Clutch Sw | CEATSFT_CRMTCLS | 7 | 0x20 | raw = (D[7] & 0x20) >> 5 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Clutch Pedal Position Switch B | CRTMSW | 7 | 0x20 | raw = (D[7] & 0x20) >> 5 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cruise Indicator | CRPL | 7 | 0x80 | raw = (D[7] & 0x80) >> 7 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.1 | CCSTATUS0 | 8 | 0xFF | raw = D[8] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.1 | CCSTATUS0 | 9 | 0xFF | raw = D[9] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.2 | CCSTATUS1 | 10 | 0xFF | raw = D[10] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.2 | CCSTATUS1 | 11 | 0xFF | raw = D[11] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.3 | CCSTATUS2 | 12 | 0xFF | raw = D[12] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.3 | CCSTATUS2 | 13 | 0xFF | raw = D[13] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.4 | CCSTATUS3 | 14 | 0xFF | raw = D[14] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.4 | CCSTATUS3 | 15 | 0xFF | raw = D[15] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.5 | CCSTATUS4 | 16 | 0xFF | raw = D[16] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.5 | CCSTATUS4 | 17 | 0xFF | raw = D[17] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.6 | CCSTATUS5 | 18 | 0xFF | raw = D[18] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.6 | CCSTATUS5 | 19 | 0xFF | raw = D[19] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.7 | CCSTATUS6 | 20 | 0xFF | raw = D[20] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.7 | CCSTATUS6 | 21 | 0xFF | raw = D[21] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.8 | CCSTATUS7 | 22 | 0xFF | raw = D[22] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.8 | CCSTATUS7 | 23 | 0xFF | raw = D[23] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.9 | CCSTATUS8 | 24 | 0xFF | raw = D[24] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.9 | CCSTATUS8 | 25 | 0xFF | raw = D[25] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.10 | CCSTATUS9 | 26 | 0xFF | raw = D[26] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | C.C Cancel History.10 | CCSTATUS9 | 27 | 0xFF | raw = D[27] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cruise Control System Switch Status | CCSW | 28 | 0xFF | raw = D[28] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Brake Switch | BKSW | 38 | 0x01 | raw = (D[38] & 0x01) >> 0 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Brake Switch B | BKPD | 38 | 0x02 | raw = (D[38] & 0x02) >> 1 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cruise Brake Sw/Idle Stop Sw | BKSWNC | 38 | 0x04 | raw = (D[38] & 0x04) >> 2 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Brake Fluid Pressure Sensor A | PBRKS1 | 39 | 0xFF | raw = D[39] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Brake Fluid Pressure Sensor A | PBRK1GN | 40 | 0xFF | raw = D[40] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Brake Fluid Pressure Sensor B | PBRKS2 | 42 | 0xFF | raw = D[42] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Brake Fluid Pressure Sensor B | PBRK2GN | 43 | 0xFF | raw = D[43] |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Battery Fan Return Signal | BFANR | 47 | 0x40 | raw = (D[47] & 0x40) >> 6 |
| 22/2664 | Cruise Indicator; Brake Switch; Cruise Brake Sw/Idle Stop Sw | L640 | 22 26 64 | — | 3 | 62 26 64 + D[0..51] | 55 when appended | None in recovered handler | HDS | Battery Fan Command | BFAN | 47 | 0x80 | raw = (D[47] & 0x80) >> 7 |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | EVPOFB | EVPOFB | 7 | 0x01 | raw = (D[7] & 0x01) >> 0 |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | EVPOFBFN | EVPOFBFN | 7 | 0x02 | raw = (D[7] & 0x02) >> 1 |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | EVPOFBOK | EVPOFBOK | 7 | 0x04 | raw = (D[7] & 0x04) >> 2 |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | EVPOFBEN | EVPOFBEN | 7 | 0x08 | raw = (D[7] & 0x08) >> 3 |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | EVPRDSS | EVPRDSS | 7 | 0x80 | raw = (D[7] & 0x80) >> 7 |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | Drive Time | CDCTIME | 8 | 0xFF | raw = D[8] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | Drive Time | CDCTIME | 9 | 0xFF | raw = D[9] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | Soak Time | IGOFFTMR | 10 | 0xFF | raw = D[10] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | Soak Time | IGOFFTMR | 11 | 0xFF | raw = D[11] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | Mildist | DISTFLM | 12 | 0xFF | raw = D[12] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | Mildist | DISTFLM | 13 | 0xFF | raw = D[13] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | Air Temp | TAOP | 14 | 0xFF | raw = D[14] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | Max Eng Spd | NEORMAX | 30 | 0xFF | raw = D[30] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | Max Eng Spd | NEORMAX | 31 | 0xFF | raw = D[31] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | Over Eng Tm | CF119S | 32 | 0xFF | raw = D[32] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | Over Eng Tm | CF119S | 33 | 0xFF | raw = D[33] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | EGR Flow Open Ratio | EGRST | 36 | 0xFF | raw = D[36] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | EGR Flow Open Ratio | EGRST | 37 | 0xFF | raw = D[37] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | CATRT | CATRT | 38 | 0xFF | raw = D[38] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | CATRT | CATRT | 39 | 0xFF | raw = D[39] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | CATRT-B1 | CATRT-B1 | 40 | 0xFF | raw = D[40] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | CATRT-B1 | CATRT-B1 | 41 | 0xFF | raw = D[41] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | CATRT-B2 | CATRT-B2 | 42 | 0xFF | raw = D[42] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | CATRT-B2 | CATRT-B2 | 43 | 0xFF | raw = D[43] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | Knock Sensor (Circuit Diag)-B1 | MBKSAD-B1 | 44 | 0xFF | raw = D[44] |
| 22/2665 | CANFI data packet 2665 | L640 | 22 26 65 | — | 3 | 62 26 65 + D[0..51] | 55 when appended | None in recovered handler | HDS | Knock Sensor (Circuit Diag)-B2 | MBKSAD-B2 | 45 | 0xFF | raw = D[45] |
| 22/2666 | CANFI data packet 2666 | L640 | 22 26 66 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Engine Oil Level | LOIL | 6 | 0xFF | raw = D[6] |
| 22/2666 | CANFI data packet 2666 | L640 | 22 26 66 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Engine Oil Level Ave | LOILREF | 7 | 0xFF | raw = D[7] |
| 22/2666 | CANFI data packet 2666 | L640 | 22 26 66 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Engine Oil Low Criteria | LOILLO | 8 | 0xFF | raw = D[8] |
| 22/2666 | CANFI data packet 2666 | L640 | 22 26 66 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Engine Oil Temperature | OILT | 11 | 0xFF | raw = D[11] |
| 22/2666 | CANFI data packet 2666 | L640 | 22 26 66 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Engine Oil Level Monitor Condition | CNDOLVL | 13 | 0x01 | raw = (D[13] & 0x01) >> 0 |
| 22/2666 | CANFI data packet 2666 | L640 | 22 26 66 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Engine Oil Temperature | TOILVL | 14 | 0xFF | raw = D[14] |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CNDRZVP | CNDRZVP | 7 | 0x01 | raw = (D[7] & 0x01) >> 0 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CNDRZTW | CNDRZTW | 7 | 0x02 | raw = (D[7] & 0x02) >> 1 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CNDRZMOT | CNDRZMOT | 7 | 0x04 | raw = (D[7] & 0x04) >> 2 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CNDRZBK | CNDRZBK | 7 | 0x08 | raw = (D[7] & 0x08) >> 3 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CNDRZAC | CNDRZAC | 7 | 0x10 | raw = (D[7] & 0x10) >> 4 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CNDRZAP | CNDRZAP | 7 | 0x20 | raw = (D[7] & 0x20) >> 5 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CNDRZDNE | CNDRZDNE | 7 | 0x40 | raw = (D[7] & 0x40) >> 6 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CNDRZNE | CNDRZNE | 7 | 0x80 | raw = (D[7] & 0x80) >> 7 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CNDRZPL1 | CNDRZPL1 | 7 | 0xFF | raw = D[7] |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CNDRZATP | CNDRZATP | 9 | 0x01 | raw = (D[9] & 0x01) >> 0 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | RZPLFAIL | RZPLFAIL | 9 | 0x10 | raw = (D[9] & 0x10) >> 4 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | RZPLCML | RZPLCML | 9 | 0x20 | raw = (D[9] & 0x20) >> 5 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | RZGO | RZGO | 9 | 0x40 | raw = (D[9] & 0x40) >> 6 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | RZST | RZST | 9 | 0x80 | raw = (D[9] & 0x80) >> 7 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Resolver Leraning-O/D Clutch Condition | CND2RZOD | 11 | 0x10 | raw = (D[11] & 0x10) >> 4 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Resolver Leraning-Vehicle Speed Condition | CND2RZVP | 11 | 0x20 | raw = (D[11] & 0x20) >> 5 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Resolver Leraning-Accelerator Pedal Sensor | CND2RZAP | 11 | 0x40 | raw = (D[11] & 0x40) >> 6 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Resolver Leraning-Battery Charging Condition | CND2RZSOC | 11 | 0x80 | raw = (D[11] & 0x80) >> 7 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Resolver Leraning Start by ECU | RZ2ST | 13 | 0x02 | raw = (D[13] & 0x02) >> 1 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ECU Does Learning About Traction Motor | RZTRCGO | 13 | 0x04 | raw = (D[13] & 0x04) >> 2 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ECU Does Learning About Generator Motor | RZGENGO | 13 | 0x08 | raw = (D[13] & 0x08) >> 3 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Traction Motor Not Learning | RZTRCFAIL | 13 | 0x10 | raw = (D[13] & 0x10) >> 4 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Traction Motor Learning Completion | RZTRCCML | 13 | 0x20 | raw = (D[13] & 0x20) >> 5 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Generator Motor Not Learning | RZGENFAIL | 13 | 0x40 | raw = (D[13] & 0x40) >> 6 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Generator Motor Learning Completion | RZGENCML | 13 | 0x80 | raw = (D[13] & 0x80) >> 7 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | STSTAT | STSTAT | 15 | 0x01 | raw = (D[15] & 0x01) >> 0 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | FSCTFAIL | FSCTFAIL | 15 | 0x10 | raw = (D[15] & 0x10) >> 4 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | FSCTPASS | FSCTPASS | 15 | 0x20 | raw = (D[15] & 0x20) >> 5 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | FSCTRDS | FSCTRDS | 15 | 0x80 | raw = (D[15] & 0x80) >> 7 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Shield Tank System EVAP Leak Inspection Mode | STL31EXC | 21 | 0x80 | raw = (D[21] & 0x80) >> 7 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ACDSDRQ | ACDSDRQ | 31 | 0x01 | raw = (D[31] & 0x01) >> 0 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ACDSDSTAT | ACDSDSTAT | 32 | 0xFF | raw = D[32] |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ACDSDRJC | ACDSDRJC | 34 | 0xFF | raw = D[34] |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Resolver Zero Point Learning (TMU) | RLRZSTATUS | 35 | 0xFF | raw = D[35] |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | TMU Failure | CNDRLRZTMU | 37 | 0x04 | raw = (D[37] & 0x04) >> 2 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | MOT ECU Failure | CNDRLRZMOT | 37 | 0x08 | raw = (D[37] & 0x08) >> 3 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Soc (State of Charge) Condition | CNDRLRZSOC | 37 | 0x10 | raw = (D[37] & 0x10) >> 4 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | System Ready State | CNDRLRZRDY | 37 | 0x20 | raw = (D[37] & 0x20) >> 5 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | P Position | CNDRLRZP | 37 | 0x40 | raw = (D[37] & 0x40) >> 6 |
| 22/2667 | CANFI data packet 2667 | L640 | 22 26 67 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Vehicle Interdiction | CNDRLRZVP | 37 | 0x80 | raw = (D[37] & 0x80) >> 7 |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | APP Sensor A | APP1 | 7 | 0xFF | raw = D[7] |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | APP Sensor A | APP1 | 8 | 0xFF | raw = D[8] |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | APP Sensor B | APP2 | 9 | 0xFF | raw = D[9] |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | APP Sensor B | APP2 | 10 | 0xFF | raw = D[10] |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | VSA REQ TH | THREQVSA | 23 | 0xFF | raw = D[23] |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | CRUS REQ TH | THREQCRU | 24 | 0xFF | raw = D[24] |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | Motor Duty | MDUTYF | 27 | 0xFF | raw = D[27] |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | Tacm Relay | DBWRLY | 37 | 0x01 | raw = (D[37] & 0x01) >> 0 |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | Throttle Actuator Supply Voltage | RDBWRLY | 37 | 0x02 | raw = (D[37] & 0x02) >> 1 |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | Throttle Actuator Supply Voltage Bank2 | RDBWRLYB2 | 37 | 0x04 | raw = (D[37] & 0x04) >> 2 |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | Sports Mode | SPMOD | 39 | 0x10 | raw = (D[39] & 0x10) >> 4 |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | DBW Stuck Ratio | KTHC_B | 45 | 0xFF | raw = D[45] |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | TRQREQVSA | TRQREQVSA | 46 | 0xFF | raw = D[46] |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | TRQREQVSA | TRQREQVSA | 47 | 0xFF | raw = D[47] |
| 22/2668 | CANFI data packet 2668 | L640 | 22 26 68 | — | 3 | 62 26 68 + D[0..51] | 55 when appended | None in recovered handler | HDS | Accelerator Pedal From Cruise Control | APREQCRU | 48 | 0xFF | raw = D[48] |
| 22/2669 | Firmware data record 2669 | L640 | 22 26 69 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | — | — | — | — | — | — |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Measurement Value | AFIINTGRT | 6 | 0xFF | raw = D[6] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Measurement Value | AFIINTGRT | 7 | 0xFF | raw = D[7] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Measurement Value | AFIINTGRT | 8 | 0xFF | raw = D[8] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Counter | AFICNT | 9 | 0xFF | raw = D[9] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Last Count | AFICNTFN | 10 | 0xFF | raw = D[10] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Judgement Threshold | AFIFSJDG | 11 | 0xFF | raw = D[11] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Judgement Threshold | AFIFSJDG | 12 | 0xFF | raw = D[12] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Judgement Threshold | AFIFSJDG | 13 | 0xFF | raw = D[13] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Measurement Value(B1) | AFIINTGRTB1 | 22 | 0xFF | raw = D[22] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Measurement Value(B1) | AFIINTGRTB1 | 23 | 0xFF | raw = D[23] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Measurement Value(B1) | AFIINTGRTB1 | 24 | 0xFF | raw = D[24] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Counter(B1) | AFICNTB1 | 25 | 0xFF | raw = D[25] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Last Count((B1) | AFICNTFNB1 | 26 | 0xFF | raw = D[26] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Judgement Threshold(B1) | AFIFSJDGB1 | 27 | 0xFF | raw = D[27] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Judgement Threshold(B1) | AFIFSJDGB1 | 28 | 0xFF | raw = D[28] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Judgement Threshold(B1) | AFIFSJDGB1 | 29 | 0xFF | raw = D[29] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Measurement Value(B2) | AFIINTGRTB2 | 38 | 0xFF | raw = D[38] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Measurement Value(B2) | AFIINTGRTB2 | 39 | 0xFF | raw = D[39] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Measurement Value(B2) | AFIINTGRTB2 | 40 | 0xFF | raw = D[40] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Counter(B2) | AFICNTB2 | 41 | 0xFF | raw = D[41] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Last Count(B2) | AFICNTFNB2 | 42 | 0xFF | raw = D[42] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Judgement Threshold(B2) | AFIFSJDGB2 | 43 | 0xFF | raw = D[43] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Judgement Threshold(B2) | AFIFSJDGB2 | 44 | 0xFF | raw = D[44] |
| 22/266A | CANFI data packet 266A | L640 | 22 26 6A | — | 3 | 62 26 6A + D[0..51] | 55 when appended | None in recovered handler | HDS | A/F Imbalance Judgement Threshold(B2) | AFIFSJDGB2 | 45 | 0xFF | raw = D[45] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | UGASSUMC | UGASSUMC | 6 | 0xFF | raw = D[6] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | UGASSUMC | UGASSUMC | 7 | 0xFF | raw = D[7] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | UGASSUMC | UGASSUMC | 8 | 0xFF | raw = D[8] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | UGASSUMC | UGASSUMC | 9 | 0xFF | raw = D[9] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | UGASSUMH | UGASSUMH | 10 | 0xFF | raw = D[10] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | UGASSUMH | UGASSUMH | 11 | 0xFF | raw = D[11] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | UGASSUMH | UGASSUMH | 12 | 0xFF | raw = D[12] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | UGASSUMH | UGASSUMH | 13 | 0xFF | raw = D[13] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | UGASSUMEH | UGASSUMEH | 14 | 0xFF | raw = D[14] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | UGASSUMEH | UGASSUMEH | 15 | 0xFF | raw = D[15] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | UGASSUMEH | UGASSUMEH | 16 | 0xFF | raw = D[16] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | UGASSUMEH | UGASSUMEH | 17 | 0xFF | raw = D[17] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DISTRVC | DISTRVC | 18 | 0xFF | raw = D[18] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DISTRVC | DISTRVC | 19 | 0xFF | raw = D[19] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DISTRVC | DISTRVC | 20 | 0xFF | raw = D[20] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DISTRVC | DISTRVC | 21 | 0xFF | raw = D[21] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DISTRVH | DISTRVH | 22 | 0xFF | raw = D[22] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DISTRVH | DISTRVH | 23 | 0xFF | raw = D[23] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DISTRVH | DISTRVH | 24 | 0xFF | raw = D[24] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DISTRVH | DISTRVH | 25 | 0xFF | raw = D[25] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DISTRVEH | DISTRVEH | 26 | 0xFF | raw = D[26] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DISTRVEH | DISTRVEH | 27 | 0xFF | raw = D[27] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DISTRVEH | DISTRVEH | 28 | 0xFF | raw = D[28] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DISTRVEH | DISTRVEH | 29 | 0xFF | raw = D[29] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Fuel Consumption For 1DC | TTRIP | 30 | 0xFF | raw = D[30] |
| 22/266B | CANFI data packet 266B | L640 | 22 26 6B | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | Fuel Consumption For 1DC | TTRIP | 31 | 0xFF | raw = D[31] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl1 Total Misfire | NMCYLOBS1 | 6 | 0xFF | raw = D[6] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl2 Total Misfire | NMCYLOBS2 | 7 | 0xFF | raw = D[7] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl3 Total Misfire | NMCYLOBS3 | 8 | 0xFF | raw = D[8] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl4 Total Misfire | NMCYLOBS4 | 9 | 0xFF | raw = D[9] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl5 Total Misfire | NMCYLOBS5 | 10 | 0xFF | raw = D[10] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl6 Total Misfire | NMCYLOBS6 | 11 | 0xFF | raw = D[11] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Injector #4 on Duration | TOUT4 | 16 | 0xFF | raw = D[16] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Injector #4 on Duration | TOUT4 | 17 | 0xFF | raw = D[17] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Average Pressure of the Fuel Tank | DPTOCLAVE | 18 | 0xFF | raw = D[18] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Average Pressure of the Fuel Tank | DPTOCLAVE | 19 | 0xFF | raw = D[19] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Average Pressure of the Fuel Tank(Hi) | DPTOCLAVEH | 20 | 0xFF | raw = D[20] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Average Pressure of the Fuel Tank(Hi) | DPTOCLAVEH | 21 | 0xFF | raw = D[21] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Average Pressure of the Fuel Tank(Hi) Fuel Cap | DPTOCLFCWH | 22 | 0xFF | raw = D[22] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Average Pressure of the Fuel Tank(Hi) Fuel Cap | DPTOCLFCWH | 23 | 0xFF | raw = D[23] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | DPTOCLLTHD | DPTOCLLTHD | 24 | 0xFF | raw = D[24] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | DPTOCLLTHD | DPTOCLLTHD | 25 | 0xFF | raw = D[25] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Tank  Pressure Pulsation (High) | CDPTOCLAVEH | 27 | 0x40 | raw = (D[27] & 0x40) >> 6 |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Tank  Pressure Pulsation | CDPTOCLAVE | 27 | 0x80 | raw = (D[27] & 0x80) >> 7 |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Tank Pressure Pulse Operation Condition | FCWBITS | 27 | 0xFF | raw = D[27] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Upper Limit of Pcs Duty | DTPCSSFTLM | 28 | 0xFF | raw = D[28] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Upper Limit of Pcs Duty | DTPCSSFTLM | 29 | 0xFF | raw = D[29] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Permit Time (A/C) | TACISOK | 30 | 0xFF | raw = D[30] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Release Counter | CDACISOK | 31 | 0xFF | raw = D[31] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Purge Flow Rate Revision Value | DPGCBS | 32 | 0xFF | raw = D[32] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Purge Flow Rate Revision Value | DPGCBS | 33 | 0xFF | raw = D[33] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Purge Flow Rate Value | QPGCF | 34 | 0xFF | raw = D[34] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | Purge Flow Rate Value | QPGCF | 35 | 0xFF | raw = D[35] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | VTC Learning | EVTCZPEND | 37 | 0x80 | raw = (D[37] & 0x80) >> 7 |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | EX VTC Status | EXVTCACT | 39 | 0x80 | raw = (D[39] & 0x80) >> 7 |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | EXVTC Sol Duty | EXDVTCSOL | 40 | 0xFF | raw = D[40] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | EX VTC Advance Angle | EXVTCABSAEA | 41 | 0xFF | raw = D[41] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | EX VTC Target Advance Angle | EXVTCCMDEA | 42 | 0xFF | raw = D[42] |
| 22/266C | CANFI data packet 266C | L640 | 22 26 6C | — | 3 | 62 26 6C + D[0..51] | 55 when appended | None in recovered handler | HDS | EX VTC Cam Shaft No Advanced | EXVTCZP | 43 | 0xFF | raw = D[43] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor Signal Plus | AFCAD | 6 | 0xFF | raw = D[6] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor Signal Minus | AFVAD | 7 | 0xFF | raw = D[7] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Sensor Impedance | AFRAC | 8 | 0xFF | raw = D[8] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Heater | DAFHT | 9 | 0xFF | raw = D[9] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Heater ON Current | IAFHTH | 10 | 0xFF | raw = D[10] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Heater ON Current | IAFHTH | 11 | 0xFF | raw = D[11] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Heater OFF Current | IAFHTL | 12 | 0xFF | raw = D[12] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | AF Heater OFF Current | IAFHTL | 13 | 0xFF | raw = D[13] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Alcohol Content Learned Value | KREFBSENAN | 29 | 0x01 | raw = (D[29] & 0x01) >> 0 |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | TOTVAP | TOTVAP | 30 | 0xFF | raw = D[30] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | KAFREF | KAFREF | 31 | 0xFF | raw = D[31] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | KAFREFX | KAFREFX | 32 | 0xFF | raw = D[32] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S S2 Output Voltage | SVO2DI | 35 | 0xFF | raw = D[35] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S Heater Duty | DSO2HT | 37 | 0xFF | raw = D[37] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | TOTVAP-B1 | TOTVAP-B1 | 38 | 0xFF | raw = D[38] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | KAFREF-B1 | KAFREF-B1 | 39 | 0xFF | raw = D[39] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | KAFREFX-B1 | KAFREFX-B1 | 40 | 0xFF | raw = D[40] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S B1 S2 Output Voltage | SVO2DI-B1 | 43 | 0xFF | raw = D[43] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S B1 Heater Duty | DSO2HT-B1 | 45 | 0xFF | raw = D[45] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | TOTVAP-B2 | TOTVAP-B2 | 46 | 0xFF | raw = D[46] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | KAFREF-B2 | KAFREF-B2 | 47 | 0xFF | raw = D[47] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | KAFREFX-B2 | KAFREFX-B2 | 48 | 0xFF | raw = D[48] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S B2 S2 Output Voltage | SVO2DI-B2 | 51 | 0xFF | raw = D[51] |
| 22/266D | CANFI data packet 266D | L640 | 22 26 6D | — | 3 | 62 26 6D + D[0..51] | 55 when appended | None in recovered handler | HDS | HO2S B2 Heater Duty | DSO2HT-B2 | 53 | 0xFF | raw = D[53] |
| 22/266E | CANFI data packet 266E | L640 | 22 26 6E | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | AF Sensor Voltage Supply | VRPVS | 9 | 0xFF | raw = D[9] |
| 22/266E | CANFI data packet 266E | L640 | 22 26 6E | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | AF Heater | DLAFHT | 10 | 0xFF | raw = D[10] |
| 22/266E | CANFI data packet 266E | L640 | 22 26 6E | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | AF Sensor B1 Mode | LAFMODE-B1 | 38 | 0xFF | raw = D[38] |
| 22/266E | CANFI data packet 266E | L640 | 22 26 6E | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | AF Sensor B1 Pump Cell | IPPHY2-B1 | 39 | 0xFF | raw = D[39] |
| 22/266E | CANFI data packet 266E | L640 | 22 26 6E | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | AF Sensor B1 VS Sell Signal | VSPHY2-B1 | 40 | 0xFF | raw = D[40] |
| 22/266E | CANFI data packet 266E | L640 | 22 26 6E | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | AF Sensor B1 Voltage Supply | VCENT2-B1 | 41 | 0xFF | raw = D[41] |
| 22/266E | CANFI data packet 266E | L640 | 22 26 6E | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | AF Sensor B1 Impedance | LAFRPVS-B1 | 42 | 0xFF | raw = D[42] |
| 22/266E | CANFI data packet 266E | L640 | 22 26 6E | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | AF Sensor B2 Mode | LAFMODE-B2 | 46 | 0xFF | raw = D[46] |
| 22/266E | CANFI data packet 266E | L640 | 22 26 6E | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | AF Sensor B2 Pump Cell | IPPHY2-B2 | 47 | 0xFF | raw = D[47] |
| 22/266E | CANFI data packet 266E | L640 | 22 26 6E | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | AF Sensor B2 VS Sell Signal | VSPHY2-B2 | 48 | 0xFF | raw = D[48] |
| 22/266E | CANFI data packet 266E | L640 | 22 26 6E | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | AF Sensor B2 Voltage Supply | VCENT2-B2 | 49 | 0xFF | raw = D[49] |
| 22/266E | CANFI data packet 266E | L640 | 22 26 6E | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | AF Sensor B2 Impedance | LAFRPVS-B2 | 50 | 0xFF | raw = D[50] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CKP No Pulse | DCRK | 4 | 0xFF | raw = D[4] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CKP Noise | NCRK | 5 | 0xFF | raw = D[5] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CMP B No Pulse | DTDC | 6 | 0xFF | raw = D[6] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CMP B Noise | NTDC | 7 | 0xFF | raw = D[7] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CMP A No Pulse | DCAM | 8 | 0xFF | raw = D[8] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CMP A Noise | NCAM | 9 | 0xFF | raw = D[9] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CMP 2 No Pulse | DTDC2 | 10 | 0xFF | raw = D[10] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CMP 2 Noise | NTDC2 | 11 | 0xFF | raw = D[11] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CMP 2 No Pulse | DCYL | 12 | 0xFF | raw = D[12] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CMP 2 Noise | NCYL | 13 | 0xFF | raw = D[13] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | ECYL1 | ECYL1 | 14 | 0xFF | raw = D[14] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | ECYL2 | ECYL2 | 15 | 0xFF | raw = D[15] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | ECRK1 | ECRK1 | 16 | 0xFF | raw = D[16] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | ECRK2 | ECRK2 | 17 | 0xFF | raw = D[17] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CKP A Noise | CFS04B | 20 | 0xFF | raw = D[20] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CKP B Noise | CFS54B | 21 | 0xFF | raw = D[21] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CMP Noise | CFS09B | 24 | 0xFF | raw = D[24] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CRKRVS | CRKRVS | 27 | 0x01 | raw = (D[27] & 0x01) >> 0 |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CKP No Pulse | DCCRK | 28 | 0xFF | raw = D[28] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CKP No Pulse | DCCRK | 29 | 0xFF | raw = D[29] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CKP Noise | NACCRK | 30 | 0xFF | raw = D[30] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CKP Noise | NACCRK | 31 | 0xFF | raw = D[31] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CMP B No Pulse | DCTDC | 32 | 0xFF | raw = D[32] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CMP B No Pulse | DCTDC | 33 | 0xFF | raw = D[33] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CMP B Noise | NACTDC | 34 | 0xFF | raw = D[34] |
| 22/266F | CANFI data packet 266F | L640 | 22 26 6F | — | 3 | 62 26 6F + D[0..35] | 39 when appended | None in recovered handler | HDS | CMP B Noise | NACTDC | 35 | 0xFF | raw = D[35] |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK23 | RLTOK23 | 6 | 0x01 | raw = (D[6] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG23 | RLTNG23 | 6 | 0x02 | raw = (D[6] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK67 | RLTOK67 | 7 | 0x01 | raw = (D[7] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG67 | RLTNG67 | 7 | 0x02 | raw = (D[7] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC67 | DEXEC67 | 7 | 0x04 | raw = (D[7] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | Cata Monitor Condition (B1) | DEXEC67S1 | 7 | 0x08 | raw = (D[7] & 0x08) >> 3 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK56A | RLTOK56A | 8 | 0x01 | raw = (D[8] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG56A | RLTNG56A | 8 | 0x02 | raw = (D[8] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK56B | RLTOK56B | 9 | 0x01 | raw = (D[9] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG56B | RLTNG56B | 9 | 0x02 | raw = (D[9] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK56C | RLTOK56C | 10 | 0x01 | raw = (D[10] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG56C | RLTNG56C | 10 | 0x02 | raw = (D[10] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK57C | RLTOK57C | 11 | 0x01 | raw = (D[11] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG57C | RLTNG57C | 11 | 0x02 | raw = (D[11] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK21L | RLTOK21L | 12 | 0x01 | raw = (D[12] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG21L | RLTNG21L | 12 | 0x02 | raw = (D[12] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK21H | RLTOK21H | 13 | 0x01 | raw = (D[13] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG21H | RLTNG21H | 13 | 0x02 | raw = (D[13] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK22L | RLTOK22L | 14 | 0x01 | raw = (D[14] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG22L | RLTNG22L | 14 | 0x02 | raw = (D[14] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK22H | RLTOK22H | 15 | 0x01 | raw = (D[15] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG22H | RLTNG22H | 15 | 0x02 | raw = (D[15] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK41C | RLTOK41C | 16 | 0x01 | raw = (D[16] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG41C | RLTNG41C | 16 | 0x02 | raw = (D[16] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK41G | RLTOK41G | 17 | 0x01 | raw = (D[17] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG41G | RLTNG41G | 17 | 0x02 | raw = (D[17] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK48S | RLTOK48S | 18 | 0x01 | raw = (D[18] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG48S | RLTNG48S | 18 | 0x02 | raw = (D[18] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK48E | RLTOK48E | 19 | 0x01 | raw = (D[19] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG48E | RLTNG48E | 19 | 0x02 | raw = (D[19] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK48F | RLTOK48F | 20 | 0x01 | raw = (D[20] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG48F | RLTNG48F | 20 | 0x02 | raw = (D[20] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK48G | RLTOK48G | 21 | 0x01 | raw = (D[21] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG48G | RLTNG48G | 21 | 0x02 | raw = (D[21] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK61A | RLTOK61A | 22 | 0x01 | raw = (D[22] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG61A | RLTNG61A | 22 | 0x02 | raw = (D[22] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC61A | DEXEC61A | 22 | 0x04 | raw = (D[22] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK61C | RLTOK61C | 23 | 0x01 | raw = (D[23] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG61C | RLTNG61C | 23 | 0x02 | raw = (D[23] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC61C | DEXEC61C | 23 | 0x04 | raw = (D[23] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC61CS | DEXEC61CS | 23 | 0x08 | raw = (D[23] & 0x08) >> 3 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK61EH | RLTOK61EH | 24 | 0x01 | raw = (D[24] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG61EH | RLTNG61EH | 24 | 0x02 | raw = (D[24] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC61EH | DEXEC61EH | 24 | 0x04 | raw = (D[24] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RDY_M61EH | RDY_M61EH | 24 | 0x08 | raw = (D[24] & 0x08) >> 3 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK63BR | RLTOK63BR | 25 | 0x01 | raw = (D[25] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG63BR | RLTNG63BR | 25 | 0x02 | raw = (D[25] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC63BR | DEXEC63BR | 25 | 0x04 | raw = (D[25] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RDY_M63BR | RDY_M63BR | 25 | 0x08 | raw = (D[25] & 0x08) >> 3 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK63BL | RLTOK63BL | 26 | 0x01 | raw = (D[26] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG63BL | RLTNG63BL | 26 | 0x02 | raw = (D[26] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC63BL | DEXEC63BL | 26 | 0x04 | raw = (D[26] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RDY_M63BL | RDY_M63BL | 26 | 0x08 | raw = (D[26] & 0x08) >> 3 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK63CB | RLTOK63CB | 27 | 0x01 | raw = (D[27] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG63CB | RLTNG63CB | 27 | 0x02 | raw = (D[27] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC63CB | DEXEC63CB | 27 | 0x04 | raw = (D[27] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RDY_M63CB | RDY_M63CB | 27 | 0x08 | raw = (D[27] & 0x08) >> 3 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK63CS | RLTOK63CS | 28 | 0x01 | raw = (D[28] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG63CS | RLTNG63CS | 28 | 0x02 | raw = (D[28] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC63CS | DEXEC63CS | 28 | 0x04 | raw = (D[28] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RDY_M63CS | RDY_M63CS | 28 | 0x08 | raw = (D[28] & 0x08) >> 3 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK63D | RLTOK63D | 29 | 0x01 | raw = (D[29] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG63D | RLTNG63D | 29 | 0x02 | raw = (D[29] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC63D | DEXEC63D | 29 | 0x04 | raw = (D[29] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RDY_M63D | RDY_M63D | 29 | 0x08 | raw = (D[29] & 0x08) >> 3 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK65B | RLTOK65B | 30 | 0x01 | raw = (D[30] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG65B | RLTNG65B | 30 | 0x02 | raw = (D[30] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK71 | RLTOK71 | 31 | 0x01 | raw = (D[31] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG71 | RLTNG71 | 31 | 0x02 | raw = (D[31] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC71 | DEXEC71 | 31 | 0x04 | raw = (D[31] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK86T | RLTOK86T | 32 | 0x01 | raw = (D[32] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG86T | RLTNG86T | 32 | 0x02 | raw = (D[32] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK86G | RLTOK86G | 33 | 0x01 | raw = (D[33] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG86G | RLTNG86G | 33 | 0x02 | raw = (D[33] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK87 | RLTOK87 | 34 | 0x01 | raw = (D[34] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG87 | RLTNG87 | 34 | 0x02 | raw = (D[34] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK10C | RLTOK10C | 35 | 0x01 | raw = (D[35] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG10C | RLTNG10C | 35 | 0x02 | raw = (D[35] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK86C | RLTOK86C | 36 | 0x01 | raw = (D[36] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG86C | RLTNG86C | 36 | 0x02 | raw = (D[36] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK302C | RLTOK302C | 37 | 0x01 | raw = (D[37] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG302C | RLTNG302C | 37 | 0x02 | raw = (D[37] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK322A | RLTOK322A | 38 | 0x01 | raw = (D[38] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG322A | RLTNG322A | 38 | 0x02 | raw = (D[38] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC322A | DEXEC322A | 38 | 0x04 | raw = (D[38] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK322B | RLTOK322B | 39 | 0x01 | raw = (D[39] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG322B | RLTNG322B | 39 | 0x02 | raw = (D[39] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC322B | DEXEC322B | 39 | 0x04 | raw = (D[39] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK05BL | RLTOK05BL | 40 | 0x01 | raw = (D[40] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG05BL | RLTNG05BL | 40 | 0x02 | raw = (D[40] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK05BH | RLTOK05BH | 41 | 0x01 | raw = (D[41] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG05BH | RLTNG05BH | 41 | 0x02 | raw = (D[41] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK13B | RLTOK13B | 42 | 0x01 | raw = (D[42] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG13B | RLTNG13B | 42 | 0x02 | raw = (D[42] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK106L | RLTOK106L | 43 | 0x01 | raw = (D[43] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG106L | RLTNG106L | 43 | 0x02 | raw = (D[43] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK106S | RLTOK106S | 44 | 0x01 | raw = (D[44] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG106S | RLTNG106S | 44 | 0x02 | raw = (D[44] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK12BF | RLTOK12BF | 45 | 0x01 | raw = (D[45] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG12BF | RLTNG12BF | 45 | 0x02 | raw = (D[45] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC12BF | DEXEC12BF | 45 | 0x04 | raw = (D[45] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK12BS | RLTOK12BS | 46 | 0x01 | raw = (D[46] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG12BS | RLTNG12BS | 46 | 0x02 | raw = (D[46] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC12BS | DEXEC12BS | 46 | 0x04 | raw = (D[46] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK80 | RLTOK80 | 47 | 0x01 | raw = (D[47] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG80 | RLTNG80 | 47 | 0x02 | raw = (D[47] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC80 | DEXEC80 | 47 | 0x04 | raw = (D[47] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK14BL | RLTOK14BL | 48 | 0x01 | raw = (D[48] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG14BL | RLTNG14BL | 48 | 0x02 | raw = (D[48] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC14BL | DEXEC14BL | 48 | 0x04 | raw = (D[48] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK14BH | RLTOK14BH | 49 | 0x01 | raw = (D[49] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG14BH | RLTNG14BH | 49 | 0x02 | raw = (D[49] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | DEXEC14BH | DEXEC14BH | 49 | 0x04 | raw = (D[49] & 0x04) >> 2 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK122 | RLTOK122 | 50 | 0x01 | raw = (D[50] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG122 | RLTNG122 | 50 | 0x02 | raw = (D[50] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK50BL | RLTOK50BL | 51 | 0x01 | raw = (D[51] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG50BL | RLTNG50BL | 51 | 0x02 | raw = (D[51] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK50BH | RLTOK50BH | 52 | 0x01 | raw = (D[52] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG50BH | RLTNG50BH | 52 | 0x02 | raw = (D[52] & 0x02) >> 1 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTOK80A | RLTOK80A | 53 | 0x01 | raw = (D[53] & 0x01) >> 0 |
| 22/2670 | CANFI data packet 2670 | HDS only | 22 26 70 | — | 3 | — | — | — | HDS | RLTNG80A | RLTNG80A | 53 | 0x02 | raw = (D[53] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK90E | RLTOK90E | 6 | 0x01 | raw = (D[6] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG90E | RLTNG90E | 6 | 0x02 | raw = (D[6] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC90E | DEXEC90E | 6 | 0x04 | raw = (D[6] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK90F | RLTOK90F | 7 | 0x01 | raw = (D[7] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG90F | RLTNG90F | 7 | 0x02 | raw = (D[7] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC90F | DEXEC90F | 7 | 0x04 | raw = (D[7] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK90F2 | RLTOK90F2 | 8 | 0x01 | raw = (D[8] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG90F2 | RLTNG90F2 | 8 | 0x02 | raw = (D[8] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK90H | RLTOK90H | 9 | 0x01 | raw = (D[9] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG90H | RLTNG90H | 9 | 0x02 | raw = (D[9] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC90H | DEXEC90H | 9 | 0x04 | raw = (D[9] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK91B | RLTOK91B | 10 | 0x01 | raw = (D[10] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG91B | RLTNG91B | 10 | 0x02 | raw = (D[10] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK91C | RLTOK91C | 11 | 0x01 | raw = (D[11] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG91C | RLTNG91C | 11 | 0x02 | raw = (D[11] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK91D | RLTOK91D | 12 | 0x01 | raw = (D[12] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG91DL | RLTNG91DL | 12 | 0x02 | raw = (D[12] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG91DH | RLTNG91DH | 12 | 0x08 | raw = (D[12] & 0x08) >> 3 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK92D | RLTOK92D | 13 | 0x01 | raw = (D[13] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG92D | RLTNG92D | 13 | 0x02 | raw = (D[13] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC92D | DEXEC92D | 13 | 0x04 | raw = (D[13] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK92E | RLTOK92E | 14 | 0x01 | raw = (D[14] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG92E | RLTNG92E | 14 | 0x02 | raw = (D[14] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK117L | RLTOK117L | 15 | 0x01 | raw = (D[15] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG117L | RLTNG117L | 15 | 0x02 | raw = (D[15] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK117H | RLTOK117H | 15 | 0x04 | raw = (D[15] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG117H | RLTNG117H | 15 | 0x08 | raw = (D[15] & 0x08) >> 3 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK117B | RLTOK117B | 16 | 0x01 | raw = (D[16] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG117B | RLTNG117B | 16 | 0x02 | raw = (D[16] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK109 | RLTOK109 | 17 | 0x01 | raw = (D[17] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG109 | RLTNG109 | 17 | 0x02 | raw = (D[17] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC109 | DEXEC109 | 17 | 0x04 | raw = (D[17] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK22EL | RLTOK22EL | 18 | 0x01 | raw = (D[18] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG22EL | RLTNG22EL | 18 | 0x02 | raw = (D[18] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK22EH | RLTOK22EH | 19 | 0x01 | raw = (D[19] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG22EH | RLTNG22EH | 19 | 0x02 | raw = (D[19] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK335AL | RLTOK335AL | 20 | 0x01 | raw = (D[20] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG335AL | RLTNG335AL | 20 | 0x02 | raw = (D[20] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK335AH | RLTOK335AH | 21 | 0x01 | raw = (D[21] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG335AH | RLTNG335AH | 21 | 0x02 | raw = (D[21] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK335BL | RLTOK335BL | 22 | 0x01 | raw = (D[22] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG335BL | RLTNG335BL | 22 | 0x02 | raw = (D[22] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK335BH | RLTOK335BH | 23 | 0x01 | raw = (D[23] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG335BH | RLTNG335BH | 23 | 0x02 | raw = (D[23] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK336SL | RLTOK336SL | 24 | 0x01 | raw = (D[24] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG336SL | RLTNG336SL | 24 | 0x02 | raw = (D[24] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC336SL | DEXEC336SL | 24 | 0x04 | raw = (D[24] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK336SH | RLTOK336SH | 25 | 0x01 | raw = (D[25] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG336SH | RLTNG336SH | 25 | 0x02 | raw = (D[25] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC336SH | DEXEC336SH | 25 | 0x04 | raw = (D[25] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK336SN | RLTOK336SN | 26 | 0x01 | raw = (D[26] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG336SN | RLTNG336SN | 26 | 0x02 | raw = (D[26] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC336SN | DEXEC336SN | 26 | 0x04 | raw = (D[26] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK17 | RLTOK17 | 27 | 0x01 | raw = (D[27] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG17 | RLTNG17 | 27 | 0x02 | raw = (D[27] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK336LS | RLTOK336LS | 28 | 0x01 | raw = (D[28] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG336LS | RLTNG336LS | 28 | 0x02 | raw = (D[28] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC336LS | DEXEC336LS | 28 | 0x04 | raw = (D[28] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK336LH | RLTOK336LH | 29 | 0x01 | raw = (D[29] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG336LH | RLTNG336LH | 29 | 0x02 | raw = (D[29] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC336LH | DEXEC336LH | 29 | 0x04 | raw = (D[29] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK336LN | RLTOK336LN | 30 | 0x01 | raw = (D[30] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG336LN | RLTNG336LN | 30 | 0x02 | raw = (D[30] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC336LN | DEXEC336LN | 30 | 0x04 | raw = (D[30] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK336HS | RLTOK336HS | 31 | 0x01 | raw = (D[31] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG336HS | RLTNG336HS | 31 | 0x02 | raw = (D[31] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC336HS | DEXEC336HS | 31 | 0x04 | raw = (D[31] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK336HL | RLTOK336HL | 32 | 0x01 | raw = (D[32] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG336HL | RLTNG336HL | 32 | 0x02 | raw = (D[32] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC336HL | DEXEC336HL | 32 | 0x04 | raw = (D[32] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK336HN | RLTOK336HN | 33 | 0x01 | raw = (D[33] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG336HN | RLTNG336HN | 33 | 0x02 | raw = (D[33] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC336HN | DEXEC336HN | 33 | 0x04 | raw = (D[33] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK336HS2 | RLTOK336HS2 | 34 | 0x01 | raw = (D[34] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG336HS2 | RLTNG336HS2 | 34 | 0x02 | raw = (D[34] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC336HS2 | DEXEC336HS2 | 34 | 0x04 | raw = (D[34] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK95B | RLTOK95B | 35 | 0x01 | raw = (D[35] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG95B | RLTNG95B | 35 | 0x02 | raw = (D[35] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC95B | DEXEC95B | 35 | 0x04 | raw = (D[35] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC95BS | DEXEC95BS | 35 | 0x08 | raw = (D[35] & 0x08) >> 3 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG95BS | RLTNG95BS | 35 | 0x80 | raw = (D[35] & 0x80) >> 7 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK96C | RLTOK96C | 36 | 0x01 | raw = (D[36] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG96C | RLTNG96C | 36 | 0x02 | raw = (D[36] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK115B | RLTOK115B | 37 | 0x01 | raw = (D[37] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG115B | RLTNG115B | 37 | 0x02 | raw = (D[37] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC115B | DEXEC115B | 37 | 0x04 | raw = (D[37] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK90W | RLTOK90W | 38 | 0x01 | raw = (D[38] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG90W | RLTNG90W | 38 | 0x02 | raw = (D[38] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK90WT | RLTOK90WT | 39 | 0x01 | raw = (D[39] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG90WT | RLTNG90WT | 39 | 0x02 | raw = (D[39] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK90ETB | RLTOK90ETB | 40 | 0x01 | raw = (D[40] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG90ETB | RLTNG90ETB | 40 | 0x02 | raw = (D[40] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOKF194C | RLTOKF194C | 41 | 0x01 | raw = (D[41] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNGF194C | RLTNGF194C | 41 | 0x02 | raw = (D[41] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK90ETA | RLTOK90ETA | 42 | 0x01 | raw = (D[42] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG90ETA | RLTNG90ETA | 42 | 0x02 | raw = (D[42] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC90GS | DEXEC90GS | 43 | 0x08 | raw = (D[43] & 0x08) >> 3 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG121B | RLTNG121B | 44 | 0x02 | raw = (D[44] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK125C | RLTOK125C | 45 | 0x01 | raw = (D[45] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG125C | RLTNG125C | 45 | 0x02 | raw = (D[45] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK26A | RLTOK26A | 46 | 0x01 | raw = (D[46] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG26A | RLTNG26A | 46 | 0x02 | raw = (D[46] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC26A | DEXEC26A | 46 | 0x04 | raw = (D[46] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK26B | RLTOK26B | 47 | 0x01 | raw = (D[47] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG26B | RLTNG26B | 47 | 0x02 | raw = (D[47] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC26B | DEXEC26B | 47 | 0x04 | raw = (D[47] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK26C | RLTOK26C | 48 | 0x01 | raw = (D[48] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG26C | RLTNG26C | 48 | 0x02 | raw = (D[48] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC26C | DEXEC26C | 48 | 0x04 | raw = (D[48] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK171R | RLTOK171R | 49 | 0x01 | raw = (D[49] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG171R | RLTNG171R | 49 | 0x02 | raw = (D[49] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK171WL | RLTOK171WL | 50 | 0x01 | raw = (D[50] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG171WL | RLTNG171WL | 50 | 0x02 | raw = (D[50] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC171WL | DEXEC171WL | 50 | 0x04 | raw = (D[50] & 0x04) >> 2 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTOK171WH | RLTOK171WH | 51 | 0x01 | raw = (D[51] & 0x01) >> 0 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | RLTNG171WH | RLTNG171WH | 51 | 0x02 | raw = (D[51] & 0x02) >> 1 |
| 22/2671 | CANFI data packet 2671 | HDS only | 22 26 71 | — | 3 | — | — | — | HDS | DEXEC171WH | DEXEC171WH | 51 | 0x04 | raw = (D[51] & 0x04) >> 2 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK68 | RLTOK68 | 6 | 0x01 | raw = (D[6] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG68 | RLTNG68 | 6 | 0x02 | raw = (D[6] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | DEXEC68 | DEXEC68 | 6 | 0x04 | raw = (D[6] & 0x04) >> 2 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | Cata Monitor Condition B2 | DEXEC68S1 | 6 | 0x08 | raw = (D[6] & 0x08) >> 3 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK41E | RLTOK41E | 7 | 0x01 | raw = (D[7] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG41E | RLTNG41E | 7 | 0x02 | raw = (D[7] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK41E2 | RLTOK41E2 | 8 | 0x01 | raw = (D[8] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG41E2 | RLTNG41E2 | 8 | 0x02 | raw = (D[8] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK41G2 | RLTOK41G2 | 9 | 0x01 | raw = (D[9] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG41G2 | RLTNG41G2 | 9 | 0x02 | raw = (D[9] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK48J | RLTOK48J | 10 | 0x01 | raw = (D[10] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG48J | RLTNG48J | 10 | 0x02 | raw = (D[10] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK48K | RLTOK48K | 11 | 0x01 | raw = (D[11] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG48K | RLTNG48K | 11 | 0x02 | raw = (D[11] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK48M | RLTOK48M | 12 | 0x01 | raw = (D[12] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG48M | RLTNG48M | 12 | 0x02 | raw = (D[12] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK48P | RLTOK48P | 13 | 0x01 | raw = (D[13] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG48P | RLTNG48P | 13 | 0x02 | raw = (D[13] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK48Q | RLTOK48Q | 14 | 0x01 | raw = (D[14] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG48Q | RLTNG48Q | 14 | 0x02 | raw = (D[14] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK48R | RLTOK48R | 15 | 0x01 | raw = (D[15] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG48R | RLTNG48R | 15 | 0x02 | raw = (D[15] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK48J2 | RLTOK48J2 | 16 | 0x01 | raw = (D[16] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG48J2 | RLTNG48J2 | 16 | 0x02 | raw = (D[16] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK48K2 | RLTOK48K2 | 17 | 0x01 | raw = (D[17] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG48K2 | RLTNG48K2 | 17 | 0x02 | raw = (D[17] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK48M2 | RLTOK48M2 | 18 | 0x01 | raw = (D[18] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG48M2 | RLTNG48M2 | 18 | 0x02 | raw = (D[18] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK48P2 | RLTOK48P2 | 19 | 0x01 | raw = (D[19] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG48P2 | RLTNG48P2 | 19 | 0x02 | raw = (D[19] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK48Q2 | RLTOK48Q2 | 20 | 0x01 | raw = (D[20] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG48Q2 | RLTNG48Q2 | 20 | 0x02 | raw = (D[20] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK48R2 | RLTOK48R2 | 21 | 0x01 | raw = (D[21] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG48R2 | RLTNG48R2 | 21 | 0x02 | raw = (D[21] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK48S2 | RLTOK48S2 | 22 | 0x01 | raw = (D[22] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG48S2 | RLTNG48S2 | 22 | 0x02 | raw = (D[22] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK62A | RLTOK62A | 23 | 0x01 | raw = (D[23] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG62A | RLTNG62A | 23 | 0x02 | raw = (D[23] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | DEXEC62A | DEXEC62A | 23 | 0x04 | raw = (D[23] & 0x04) >> 2 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK62C | RLTOK62C | 24 | 0x01 | raw = (D[24] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG62C | RLTNG62C | 24 | 0x02 | raw = (D[24] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | DEXEC62C | DEXEC62C | 24 | 0x04 | raw = (D[24] & 0x04) >> 2 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK62EH | RLTOK62EH | 25 | 0x01 | raw = (D[25] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG62EH | RLTNG62EH | 25 | 0x02 | raw = (D[25] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | DEXEC62EH | DEXEC62EH | 25 | 0x04 | raw = (D[25] & 0x04) >> 2 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK64BR | RLTOK64BR | 26 | 0x01 | raw = (D[26] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG64BR | RLTNG64BR | 26 | 0x02 | raw = (D[26] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | DEXEC64BR | DEXEC64BR | 26 | 0x04 | raw = (D[26] & 0x04) >> 2 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK64BL | RLTOK64BL | 27 | 0x01 | raw = (D[27] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG64BL | RLTNG64BL | 27 | 0x02 | raw = (D[27] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | DEXEC64BL | DEXEC64BL | 27 | 0x04 | raw = (D[27] & 0x04) >> 2 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK64CB | RLTOK64CB | 28 | 0x01 | raw = (D[28] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG64CB | RLTNG64CB | 28 | 0x02 | raw = (D[28] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | DEXEC64CB | DEXEC64CB | 28 | 0x04 | raw = (D[28] & 0x04) >> 2 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK64CS | RLTOK64CS | 29 | 0x01 | raw = (D[29] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG64CS | RLTNG64CS | 29 | 0x02 | raw = (D[29] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | DEXEC64CS | DEXEC64CS | 29 | 0x04 | raw = (D[29] & 0x04) >> 2 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK64D | RLTOK64D | 30 | 0x01 | raw = (D[30] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG64D | RLTNG64D | 30 | 0x02 | raw = (D[30] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | DEXEC64D | DEXEC64D | 30 | 0x04 | raw = (D[30] & 0x04) >> 2 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK66B | RLTOK66B | 31 | 0x01 | raw = (D[31] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG66B | RLTNG66B | 31 | 0x02 | raw = (D[31] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK21S | RLTOK21S | 32 | 0x01 | raw = (D[32] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG21S | RLTNG21S | 32 | 0x02 | raw = (D[32] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK21N | RLTOK21N | 33 | 0x01 | raw = (D[33] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG21N | RLTNG21N | 33 | 0x02 | raw = (D[33] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK114S | RLTOK114S | 34 | 0x01 | raw = (D[34] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG114S | RLTNG114S | 34 | 0x02 | raw = (D[34] & 0x02) >> 1 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTOK114N | RLTOK114N | 35 | 0x01 | raw = (D[35] & 0x01) >> 0 |
| 22/2672 | CANFI data packet 2672 | HDS only | 22 26 72 | — | 3 | — | — | — | HDS | RLTNG114N | RLTNG114N | 35 | 0x02 | raw = (D[35] & 0x02) >> 1 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cata Monitor Condition | DOCAT | 7 | 0x01 | raw = (D[7] & 0x01) >> 0 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cata Monitor Condition B1 | DOCATB1 | 7 | 0x02 | raw = (D[7] & 0x02) >> 1 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cata Monitor Condition B2 | DOCATB2 | 7 | 0x04 | raw = (D[7] & 0x04) >> 2 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOMISFIRE | DOMISFIRE | 11 | 0x01 | raw = (D[11] & 0x01) >> 0 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOPCV | DOPCV | 15 | 0x01 | raw = (D[15] & 0x01) >> 0 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOPCS | DOPCS | 19 | 0x01 | raw = (D[19] & 0x01) >> 0 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOLAFSR | DOLAFSR | 23 | 0x01 | raw = (D[23] & 0x01) >> 0 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOLAFPF | DOLAFPF | 23 | 0x02 | raw = (D[23] & 0x02) >> 1 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOLAFCIR | DOLAFCIR | 23 | 0x04 | raw = (D[23] & 0x04) >> 2 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOLAFSRB1 | DOLAFSRB1 | 27 | 0x01 | raw = (D[27] & 0x01) >> 0 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOLAFSRB2 | DOLAFSRB2 | 27 | 0x02 | raw = (D[27] & 0x02) >> 1 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOLAFPFB1 | DOLAFPFB1 | 27 | 0x04 | raw = (D[27] & 0x04) >> 2 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOLAFPFB2 | DOLAFPFB2 | 27 | 0x08 | raw = (D[27] & 0x08) >> 3 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOLAFCIRB1 | DOLAFCIRB1 | 27 | 0x10 | raw = (D[27] & 0x10) >> 4 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOLAFCIRB2 | DOLAFCIRB2 | 27 | 0x20 | raw = (D[27] & 0x20) >> 5 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOSO2CLO | DOSO2CLO | 31 | 0x01 | raw = (D[31] & 0x01) >> 0 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOSO2CHI | DOSO2CHI | 31 | 0x02 | raw = (D[31] & 0x02) >> 1 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOSO2SR | DOSO2SR | 31 | 0x04 | raw = (D[31] & 0x04) >> 2 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOSO2CLOB1 | DOSO2CLOB1 | 35 | 0x01 | raw = (D[35] & 0x01) >> 0 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOSO2CLOB2 | DOSO2CLOB2 | 35 | 0x02 | raw = (D[35] & 0x02) >> 1 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOSO2CHIB1 | DOSO2CHIB1 | 35 | 0x04 | raw = (D[35] & 0x04) >> 2 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOSO2CHIB2 | DOSO2CHIB2 | 35 | 0x08 | raw = (D[35] & 0x08) >> 3 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOSO2SRB1 | DOSO2SRB1 | 35 | 0x10 | raw = (D[35] & 0x10) >> 4 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOSO2SRB2 | DOSO2SRB2 | 35 | 0x20 | raw = (D[35] & 0x20) >> 5 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOIACLO | DOIACLO | 39 | 0x01 | raw = (D[39] & 0x01) >> 0 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOIACHI | DOIACHI | 39 | 0x02 | raw = (D[39] & 0x02) >> 1 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOCSIACPF | DOCSIACPF | 39 | 0x04 | raw = (D[39] & 0x04) >> 2 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOCSIGPF | DOCSIGPF | 39 | 0x08 | raw = (D[39] & 0x08) >> 3 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOWGS | DOWGS | 43 | 0x01 | raw = (D[43] & 0x01) >> 0 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOEGRFID | DOEGRFID | 47 | 0x01 | raw = (D[47] & 0x01) >> 0 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOEGRCPF | DOEGRCPF | 47 | 0x02 | raw = (D[47] & 0x02) >> 1 |
| 22/2673 | CANFI data packet 2673 | L640 | 22 26 73 | — | 3 | 62 26 73 + D[0..51] | 55 when appended | None in recovered handler | HDS | DOEGRPF | DOEGRPF | 47 | 0x04 | raw = (D[47] & 0x04) >> 2 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTOK90S | RLTOK90S | 6 | 0x01 | raw = (D[6] & 0x01) >> 0 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTNG90S | RLTNG90S | 6 | 0x02 | raw = (D[6] & 0x02) >> 1 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTOK90T | RLTOK90T | 7 | 0x01 | raw = (D[7] & 0x01) >> 0 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTNG90T | RLTNG90T | 7 | 0x02 | raw = (D[7] & 0x02) >> 1 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTOK90C | RLTOK90C | 8 | 0x01 | raw = (D[8] & 0x01) >> 0 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTNG90C | RLTNG90C | 8 | 0x02 | raw = (D[8] & 0x02) >> 1 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTOK91F | RLTOK91F | 9 | 0x01 | raw = (D[9] & 0x01) >> 0 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTNG91F | RLTNG91F | 9 | 0x02 | raw = (D[9] & 0x02) >> 1 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTOK94PL | RLTOK94PL | 10 | 0x01 | raw = (D[10] & 0x01) >> 0 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTNG94PL | RLTNG94PL | 10 | 0x02 | raw = (D[10] & 0x02) >> 1 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTOK94PH | RLTOK94PH | 11 | 0x01 | raw = (D[11] & 0x01) >> 0 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTNG94PH | RLTNG94PH | 11 | 0x02 | raw = (D[11] & 0x02) >> 1 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTOK94PN | RLTOK94PN | 12 | 0x01 | raw = (D[12] & 0x01) >> 0 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTNG94PN | RLTNG94PN | 12 | 0x02 | raw = (D[12] & 0x02) >> 1 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTOK94PS | RLTOK94PS | 13 | 0x01 | raw = (D[13] & 0x01) >> 0 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTNG94PS | RLTNG94PS | 13 | 0x02 | raw = (D[13] & 0x02) >> 1 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTOK94PW | RLTOK94PW | 14 | 0x01 | raw = (D[14] & 0x01) >> 0 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTNG94PW | RLTNG94PW | 14 | 0x02 | raw = (D[14] & 0x02) >> 1 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTOK94PD | RLTOK94PD | 15 | 0x01 | raw = (D[15] & 0x01) >> 0 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTNG94PD | RLTNG94PD | 15 | 0x02 | raw = (D[15] & 0x02) >> 1 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTOK124L | RLTOK124L | 16 | 0x01 | raw = (D[16] & 0x01) >> 0 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTNG124L | RLTNG124L | 16 | 0x02 | raw = (D[16] & 0x02) >> 1 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTOK124S | RLTOK124S | 17 | 0x01 | raw = (D[17] & 0x01) >> 0 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTNG124S | RLTNG124S | 17 | 0x02 | raw = (D[17] & 0x02) >> 1 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTOK90N | RLTOK90N | 18 | 0x01 | raw = (D[18] & 0x01) >> 0 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTNG90N | RLTNG90N | 18 | 0x02 | raw = (D[18] & 0x02) >> 1 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTOK92S | RLTOK92S | 19 | 0x01 | raw = (D[19] & 0x01) >> 0 |
| 22/2674 | CANFI data packet 2674 | HDS only | 22 26 74 | — | 3 | — | — | — | HDS | RLTNG92S | RLTNG92S | 19 | 0x02 | raw = (D[19] & 0x02) >> 1 |
| 22/2676 | Firmware data record 2676 | L640 | 22 26 76 | — | 3 | 62 26 76 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xEFFE6..0xF0008 | 0xFFF84A26 | D[9] | — | bit1 = B(0xFFF84A26); all other bits zero [PROVEN dossier table] |
| 22/2676 | Firmware data record 2676 | L640 | 22 26 76 | — | 3 | 62 26 76 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF0068..0xF0090 | 0xFFF84A29, 0xFFF84A32 | D[47] | — | bit1 = B(0xFFF84A32); bit2 = B(0xFFF84A29); other bits zero [PROVEN dossier table] |
| 22/2677 | Firmware data record 2677 | L640 | 22 26 77 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | — | — | — | — | — | — |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF010C..0xF015A | 0xFFF95016 | D[0..4] | — | If B(FFF95016): `C3 7F FF FF FC`; else five zeroes [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF0166..0xF0188 | 0xFFF91C8C | D[6..7] | — | BE16 min(65535, 2 * u16(FFF91C8C)) [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | helper call 0xF01BA, store 0xF01C6 | 0xFFF95016 | D[12] | — | Bits 4 and 5 both B(FFF95016); other bits zero [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | call 0xF01E0, store 0xF01F2 | 0xFFF95F32, 0xFFF95F36 | D[13] | — | Bit 4 B(FFF95F36), bit 5 B(FFF95F32); other bits zero [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | call 0xF01FC, high store 0xF0206 | 0xFFF92886 | D[15..16] | — | BE16 raw FFF92886 [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF020C, 0xF0216 | 0xFFF844B4 | D[17..18] | — | BE16 raw FFF844B4 [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF021E, 0xF0228 | 0xFFF844BE | D[19..20] | — | BE16 raw FFF844BE [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF0230, 0xF023A | 0xFFF844B8 | D[21..22] | — | BE16 raw FFF844B8 [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF0242, 0xF024C | 0xFFF844C0 | D[23..24] | — | BE16 raw FFF844C0 [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF0254, 0xF025E | 0xFFF844BA | D[25..26] | — | BE16 raw FFF844BA [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF0266, 0xF0270 | 0xFFF844AE | D[27..28] | — | BE16 raw FFF844AE [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF0278, 0xF0282 | 0xFFF844B6 | D[29..30] | — | BE16 raw FFF844B6 [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF028A, 0xF0294 | 0xFFF844C6 | D[31..32] | — | BE16 raw FFF844C6 [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF029C, 0xF02A6 | 0xFFF844C4 | D[33..34] | — | BE16 raw FFF844C4 [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF02AE, 0xF02B8 | 0xFFF844BC | D[35..36] | — | BE16 raw FFF844BC [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF02C0, 0xF02CA | 0xFFF844B2 | D[37..38] | — | BE16 raw FFF844B2 [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF02D2, 0xF02DC | 0xFFF844B0 | D[39..40] | — | BE16 raw FFF844B0 [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF02E4, 0xF02F0 | 0xFFF844C2 | D[41..42] | — | BE16 raw FFF844C2 [PROVEN dossier table] |
| 22/2678 | Firmware data record 2678 | L640 | 22 26 78 | — | 3 | 62 26 78 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF02EC..0xF02F6 | 0xFFF871F6 | D[43] | — | Raw byte FFF871F6 [PROVEN dossier table] |
| 22/2679 | Firmware data record 2679 | L640 | 22 26 79 | — | 3 | 62 26 79 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | calls 0xF035A..0xF03DE; high stores 0xF0362..0xF03E8 | 0xFFF84764 | D[6..23] | — | Nine consecutive BE16 raw words from FFF84764, 66, 68, 6A, 6C, 6E, 70, 72, 74 [PROVEN dossier table] |
| 22/2679 | Firmware data record 2679 | L640 | 22 26 79 | — | 3 | 62 26 79 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | calls 0xF03F0..0xF044A; high stores 0xF03FA..0xF0454 | 0xFFF830A4 | D[24..35] | — | Six consecutive BE16 raw words from FFF830A4, A6, A8, AA, AC, AE [PROVEN dossier table] |
| 22/2679 | Firmware data record 2679 | L640 | 22 26 79 | — | 3 | 62 26 79 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | call 0xF045C, high store 0xF0466 | 0xFFF84752 | D[36..37] | — | BE16 raw FFF84752 [PROVEN dossier table] |
| 22/2679 | Firmware data record 2679 | L640 | 22 26 79 | — | 3 | 62 26 79 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF046E, 0xF0476 | 0xFFF84754 | D[38..39] | — | BE16 raw FFF84754 [PROVEN dossier table] |
| 22/2679 | Firmware data record 2679 | L640 | 22 26 79 | — | 3 | 62 26 79 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF047E, 0xF0486 | 0xFFF84756 | D[40..41] | — | BE16 raw FFF84756 [PROVEN dossier table] |
| 22/2679 | Firmware data record 2679 | L640 | 22 26 79 | — | 3 | 62 26 79 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF0490, 0xF0498 | 0xFFF84758 | D[42..43] | — | BE16 raw FFF84758 [PROVEN dossier table] |
| 22/2679 | Firmware data record 2679 | L640 | 22 26 79 | — | 3 | 62 26 79 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF04A2, 0xF04AA | 0xFFF8475A | D[44..45] | — | BE16 raw FFF8475A [PROVEN dossier table] |
| 22/2679 | Firmware data record 2679 | L640 | 22 26 79 | — | 3 | 62 26 79 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF04B4, 0xF04BE | 0xFFF8475C | D[46..47] | — | BE16 raw FFF8475C [PROVEN dossier table] |
| 22/2679 | Firmware data record 2679 | L640 | 22 26 79 | — | 3 | 62 26 79 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF04C6, 0xF04D0 | 0xFFF8474C | D[48..49] | — | BE16 raw FFF8474C [PROVEN dossier table] |
| 22/2679 | Firmware data record 2679 | L640 | 22 26 79 | — | 3 | 62 26 79 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF04D8, 0xF04E2 | 0xFFF8474E | D[50..51] | — | BE16 raw FFF8474E [PROVEN dossier table] |
| 22/2679 | Firmware data record 2679 | L640 | 22 26 79 | — | 3 | 62 26 79 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF04EA, 0xF04F2 | 0xFFF84750 | D[52..53] | — | BE16 raw FFF84750 [PROVEN dossier table] |
| 22/267A | Firmware data record 267A | L640 | 22 26 7A | — | 3 | 62 26 7A + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF0534..0xF0570 | 0xFFF9501F | D[0..1] | — | If B(FFF9501F): `FF DC`; else `00 1C` [PROVEN dossier table] |
| 22/267A | Firmware data record 267A | L640 | 22 26 7A | — | 3 | 62 26 7A + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF0574..0xF0586 | 0xFFF9504C | D[3] | — | 30 if B(FFF9504C), else 00 [PROVEN dossier table] |
| 22/267A | Firmware data record 267A | L640 | 22 26 7A | — | 3 | 62 26 7A + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF05AC..0xF05D2 | 0xFFF8EA50 | D[6..9] | — | BE32 raw FFF8EA50, high word then low word; source loaded twice [PROVEN dossier table] |
| 22/267A | Firmware data record 267A | L640 | 22 26 7A | — | 3 | 62 26 7A + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF05D6..0xF05F0 | 0xFFF8EA54 | D[10..13] | — | BE32 raw FFF8EA54, high word then low word; source loaded twice [PROVEN dossier table] |
| 22/267A | Firmware data record 267A | L640 | 22 26 7A | — | 3 | 62 26 7A + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF05E4..0xF0600 | 0xFFF92854 | D[14..15] | — | BE16 raw FFF92854 [PROVEN dossier table] |
| 22/267A | Firmware data record 267A | L640 | 22 26 7A | — | 3 | 62 26 7A + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | call 0xF060A, store 0xF0610 | 0xFFF8475E | D[17] | — | T(s16(FFF8475E)) [PROVEN dossier table] |
| 22/267A | Firmware data record 267A | L640 | 22 26 7A | — | 3 | 62 26 7A + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF0618, 0xF061E | 0xFFF84760 | D[18] | — | T(s16(FFF84760)) [PROVEN dossier table] |
| 22/267A | Firmware data record 267A | L640 | 22 26 7A | — | 3 | 62 26 7A + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF0626, 0xF062E | 0xFFF84762 | D[19] | — | T(s16(FFF84762)) [PROVEN dossier table] |
| 22/267A | Firmware data record 267A | L640 | 22 26 7A | — | 3 | 62 26 7A + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | 0xF0642..0xF0656 | 0xFFF91AA4 | D[32..33] | — | BE16 raw FFF91AA4 [PROVEN dossier table] |
| 22/267B | CANFI data packet 267B | L640 | 22 26 7B | — | 3 | 62 26 7B + D[0..51] | 55 when appended | None in recovered handler | HDS | PURGE CORRECTION FACTOR (FOR BANK2) | KEVACTB2 | 14 | 0xFF | raw = D[14] |
| 22/267B | CANFI data packet 267B | L640 | 22 26 7B | — | 3 | 62 26 7B + D[0..51] | 55 when appended | None in recovered handler | HDS | PURGE CORRECTION FACTOR (FOR BANK2) | KEVACTB2 | 15 | 0xFF | raw = D[15] |
| 22/267B | CANFI data packet 267B | L640 | 22 26 7B | — | 3 | 62 26 7B + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Tank Pressure Sensor Rationality Monitor | CPTOC91BJD | 18 | 0xFF | raw = D[18] |
| 22/267B | CANFI data packet 267B | L640 | 22 26 7B | — | 3 | 62 26 7B + D[0..51] | 55 when appended | None in recovered handler | HDS | Equivalent Duration the Pcs Duty Control | CPTOC91BNG | 19 | 0xFF | raw = D[19] |
| 22/267C | CANFI data packet 267C | L640 | 22 26 7C | — | 3 | 62 26 7C + D[0..51] | 55 when appended | None in recovered handler | HDS | TPTCYCLE | TPTCYCLE | 6 | 0xFF | raw = D[6] |
| 22/267C | CANFI data packet 267C | L640 | 22 26 7C | — | 3 | 62 26 7C + D[0..51] | 55 when appended | None in recovered handler | HDS | TPTCYCLE | TPTCYCLE | 7 | 0xFF | raw = D[7] |
| 22/267C | CANFI data packet 267C | L640 | 22 26 7C | — | 3 | 62 26 7C + D[0..51] | 55 when appended | None in recovered handler | HDS | EVPMON | EVPMON | 11 | 0x01 | raw = (D[11] & 0x01) >> 0 |
| 22/267C | CANFI data packet 267C | L640 | 22 26 7C | — | 3 | 62 26 7C + D[0..51] | 55 when appended | None in recovered handler | HDS | DPTRLF | DPTRLF | 12 | 0xFF | raw = D[12] |
| 22/267C | CANFI data packet 267C | L640 | 22 26 7C | — | 3 | 62 26 7C + D[0..51] | 55 when appended | None in recovered handler | HDS | DPTRLF | DPTRLF | 13 | 0xFF | raw = D[13] |
| 22/267C | CANFI data packet 267C | L640 | 22 26 7C | — | 3 | 62 26 7C + D[0..51] | 55 when appended | None in recovered handler | HDS | TPTPHASE | TPTPHASE | 14 | 0xFF | raw = D[14] |
| 22/267C | CANFI data packet 267C | L640 | 22 26 7C | — | 3 | 62 26 7C + D[0..51] | 55 when appended | None in recovered handler | HDS | TPTPHASE | TPTPHASE | 15 | 0xFF | raw = D[15] |
| 22/267C | CANFI data packet 267C | L640 | 22 26 7C | — | 3 | 62 26 7C + D[0..51] | 55 when appended | None in recovered handler | HDS | KFCAPJUD | KFCAPJUD | 20 | 0xFF | raw = D[20] |
| 22/267C | CANFI data packet 267C | L640 | 22 26 7C | — | 3 | 62 26 7C + D[0..51] | 55 when appended | None in recovered handler | HDS | KFCAPJUD | KFCAPJUD | 21 | 0xFF | raw = D[21] |
| 22/267C | CANFI data packet 267C | L640 | 22 26 7C | — | 3 | 62 26 7C + D[0..51] | 55 when appended | None in recovered handler | HDS | DPTABS | DPTABS | 22 | 0xFF | raw = D[22] |
| 22/267C | CANFI data packet 267C | L640 | 22 26 7C | — | 3 | 62 26 7C + D[0..51] | 55 when appended | None in recovered handler | HDS | DPTABS | DPTABS | 23 | 0xFF | raw = D[23] |
| 22/267D | Firmware data record 267D | L640 | 22 26 7D | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | — | — | — | — | — | — |
| 22/267E | Firmware data record 267E | L640 | 22 26 7E | — | 3 | 62 26 7E + D[0..33] | 37 when appended | None in recovered handler | Firmware dossier | 0xF0AAA..0xF0B04 | 0xFFF94748 | D[0] | — | bits0/1/2/3/4/6 = nonzero 0xFFF94748/49/4A/4B/4C/4D; bits5/7 zero [PROVEN dossier table] |
| 22/267E | Firmware data record 267E | L640 | 22 26 7E | — | 3 | 62 26 7E + D[0..33] | 37 when appended | None in recovered handler | Firmware dossier | 0xF0B06..0xF0B36 | 0xFFF9474E, 0xFFF94753 | D[1] | — | bit2 = nonzero 0xFFF9474E; bit1 = nonzero 0xFFF94753; other bits zero [PROVEN dossier table] |
| 22/267E | Firmware data record 267E | L640 | 22 26 7E | — | 3 | 62 26 7E + D[0..33] | 37 when appended | None in recovered handler | Firmware dossier | 0xF0B32..0xF0B46 | 0xFFF8FC5E | D[2..3] | — | BE16 raw word 0xFFF8FC5E [PROVEN dossier table] |
| 22/267E | Firmware data record 267E | L640 | 22 26 7E | — | 3 | 62 26 7E + D[0..33] | 37 when appended | None in recovered handler | Firmware dossier | 0xF0B42..0xF0B56 | 0xFFF8FC60 | D[4..5] | — | BE16 raw word 0xFFF8FC60 [PROVEN dossier table] |
| 22/267E | Firmware data record 267E | L640 | 22 26 7E | — | 3 | 62 26 7E + D[0..33] | 37 when appended | None in recovered handler | Firmware dossier | 0xF0B52..0xF0B66 | 0xFFF8FC62 | D[6..7] | — | BE16 raw word 0xFFF8FC62 [PROVEN dossier table] |
| 22/267E | Firmware data record 267E | L640 | 22 26 7E | — | 3 | 62 26 7E + D[0..33] | 37 when appended | None in recovered handler | Firmware dossier | 0xF0B62..0xF0B76 | 0xFFF8FC64 | D[8..9] | — | BE16 raw word 0xFFF8FC64 [PROVEN dossier table] |
| 22/267E | Firmware data record 267E | L640 | 22 26 7E | — | 3 | 62 26 7E + D[0..33] | 37 when appended | None in recovered handler | Firmware dossier | 0xF0B72..0xF0B86 | 0xFFF8FC66 | D[10..11] | — | BE16 raw word 0xFFF8FC66 [PROVEN dossier table] |
| 22/267E | Firmware data record 267E | L640 | 22 26 7E | — | 3 | 62 26 7E + D[0..33] | 37 when appended | None in recovered handler | Firmware dossier | 0xF0B82..0xF0B9A | 0xFFF8FC68 | D[14..15] | — | BE16 raw word 0xFFF8FC68 [PROVEN dossier table] |
| 22/267E | Firmware data record 267E | L640 | 22 26 7E | — | 3 | 62 26 7E + D[0..33] | 37 when appended | None in recovered handler | Firmware dossier | 0xF0BB6..0xF0BCA | 0xFFF8FC70 | D[20..21] | — | BE16 raw word 0xFFF8FC70 [PROVEN dossier table] |
| 22/267E | Firmware data record 267E | L640 | 22 26 7E | — | 3 | 62 26 7E + D[0..33] | 37 when appended | None in recovered handler | Firmware dossier | 0xF0BC6..0xF0BDA | 0xFFF8FC6A | D[22..23] | — | BE16 raw word 0xFFF8FC6A [PROVEN dossier table] |
| 22/267F | CANFI data packet 267F | L640 | 22 26 7F | — | 3 | 62 26 7F + D[0..9] | 13 when appended | None in recovered handler | HDS | REQMD | REQMD | 0 | 0xFF | raw = D[0] |
| 22/267F | CANFI data packet 267F | L640 | 22 26 7F | — | 3 | 62 26 7F + D[0..9] | 13 when appended | None in recovered handler | HDS | REQMD | REQMD | 1 | 0xFF | raw = D[1] |
| 22/267F | CANFI data packet 267F | L640 | 22 26 7F | — | 3 | 62 26 7F + D[0..9] | 13 when appended | None in recovered handler | HDS | REQCMD | REQCMD | 2 | 0xFF | raw = D[2] |
| 22/267F | CANFI data packet 267F | L640 | 22 26 7F | — | 3 | 62 26 7F + D[0..9] | 13 when appended | None in recovered handler | HDS | REQCMD | REQCMD | 3 | 0xFF | raw = D[3] |
| 22/267F | CANFI data packet 267F | L640 | 22 26 7F | — | 3 | 62 26 7F + D[0..9] | 13 when appended | None in recovered handler | HDS | EXECMD | EXECMD | 4 | 0xFF | raw = D[4] |
| 22/267F | CANFI data packet 267F | L640 | 22 26 7F | — | 3 | 62 26 7F + D[0..9] | 13 when appended | None in recovered handler | HDS | EXECMD | EXECMD | 5 | 0xFF | raw = D[5] |
| 22/267F | CANFI data packet 267F | L640 | 22 26 7F | — | 3 | 62 26 7F + D[0..9] | 13 when appended | None in recovered handler | HDS | SDARJC | SDARJC | 6 | 0xFF | raw = D[6] |
| 22/2680 | CANFI data packet 2680 | L640 | 22 26 80 | — | 3 | 62 26 80 + D[0..51] | 55 when appended | None in recovered handler | HDS | Genertion Direction Value to ACG | VACG | 6 | 0xFF | raw = D[6] |
| 22/2680 | CANFI data packet 2680 | L640 | 22 26 80 | — | 3 | 62 26 80 + D[0..51] | 55 when appended | None in recovered handler | HDS | DACGF | DACGF | 7 | 0xFF | raw = D[7] |
| 22/2680 | CANFI data packet 2680 | L640 | 22 26 80 | — | 3 | 62 26 80 + D[0..51] | 55 when appended | None in recovered handler | HDS | Hight Temperature Abnormal On ACG | FACGTMP | 9 | 0x20 | raw = (D[9] & 0x20) >> 5 |
| 22/2680 | CANFI data packet 2680 | L640 | 22 26 80 | — | 3 | 62 26 80 + D[0..51] | 55 when appended | None in recovered handler | HDS | Generation Stop On ACG | FACGELC | 9 | 0x40 | raw = (D[9] & 0x40) >> 6 |
| 22/2680 | CANFI data packet 2680 | L640 | 22 26 80 | — | 3 | 62 26 80 + D[0..51] | 55 when appended | None in recovered handler | HDS | Turn Stop On ACG | FACGMEC | 9 | 0x80 | raw = (D[9] & 0x80) >> 7 |
| 22/2680 | CANFI data packet 2680 | L640 | 22 26 80 | — | 3 | 62 26 80 + D[0..51] | 55 when appended | None in recovered handler | HDS | ACG Excitation Current | IEXCIT | 10 | 0xFF | raw = D[10] |
| 22/2681 | CANFI data packet 2681 | L640 | 22 26 81 | — | 3 | 62 26 81 + D[0..51] | 55 when appended | None in recovered handler | HDS | Battery Voltage From Battery Sensor | VBPBAT | 6 | 0xFF | raw = D[6] |
| 22/2681 | CANFI data packet 2681 | L640 | 22 26 81 | — | 3 | 62 26 81 + D[0..51] | 55 when appended | None in recovered handler | HDS | Battery Voltage From Battery Sensor | VBPBAT | 7 | 0xFF | raw = D[7] |
| 22/2681 | CANFI data packet 2681 | L640 | 22 26 81 | — | 3 | 62 26 81 + D[0..51] | 55 when appended | None in recovered handler | HDS | Battery Current (Battery Sensor) | IPBAT | 8 | 0xFF | raw = D[8] |
| 22/2681 | CANFI data packet 2681 | L640 | 22 26 81 | — | 3 | 62 26 81 + D[0..51] | 55 when appended | None in recovered handler | HDS | Battery Current (Battery Sensor) | IPBAT | 9 | 0xFF | raw = D[9] |
| 22/2681 | CANFI data packet 2681 | L640 | 22 26 81 | — | 3 | 62 26 81 + D[0..51] | 55 when appended | None in recovered handler | HDS | Estimated Battery Temperature | TPBAT | 10 | 0xFF | raw = D[10] |
| 22/2681 | CANFI data packet 2681 | L640 | 22 26 81 | — | 3 | 62 26 81 + D[0..51] | 55 when appended | None in recovered handler | HDS | Estimated Battery Resistance (Battery Sensor) | RCLPBAT | 11 | 0xFF | raw = D[11] |
| 22/2681 | CANFI data packet 2681 | L640 | 22 26 81 | — | 3 | 62 26 81 + D[0..51] | 55 when appended | None in recovered handler | HDS | Voltage Detection Status | VBATSTATUS | 12 | 0xFF | raw = D[12] |
| 22/2681 | CANFI data packet 2681 | L640 | 22 26 81 | — | 3 | 62 26 81 + D[0..51] | 55 when appended | None in recovered handler | HDS | Current Detection Status | IBATSTATUS | 13 | 0xFF | raw = D[13] |
| 22/2681 | CANFI data packet 2681 | L640 | 22 26 81 | — | 3 | 62 26 81 + D[0..51] | 55 when appended | None in recovered handler | HDS | Temperature Detection Status | TBATSTATUS | 14 | 0xFF | raw = D[14] |
| 22/2681 | CANFI data packet 2681 | L640 | 22 26 81 | — | 3 | 62 26 81 + D[0..51] | 55 when appended | None in recovered handler | HDS | Nonvolatile Memory Info (Battery Sensor) | BSSNVM | 16 | 0x40 | raw = (D[16] & 0x40) >> 6 |
| 22/2681 | CANFI data packet 2681 | L640 | 22 26 81 | — | 3 | 62 26 81 + D[0..51] | 55 when appended | None in recovered handler | HDS | Survey Infomation Battery Management(1) | SOCPBAT | 18 | 0xFF | raw = D[18] |
| 22/2681 | CANFI data packet 2681 | L640 | 22 26 81 | — | 3 | 62 26 81 + D[0..51] | 55 when appended | None in recovered handler | HDS | Reset on Battery Sensor | BATSRST | 20 | 0x40 | raw = (D[20] & 0x40) >> 6 |
| 22/2681 | CANFI data packet 2681 | L640 | 22 26 81 | — | 3 | 62 26 81 + D[0..51] | 55 when appended | None in recovered handler | HDS | Survey Infomation Battery Management(2) | SOCCL | 20 | 0x80 | raw = (D[20] & 0x80) >> 7 |
| 22/2681 | CANFI data packet 2681 | L640 | 22 26 81 | — | 3 | 62 26 81 + D[0..51] | 55 when appended | None in recovered handler | HDS | Survey Infomation Battery Management(3) | BDCHGBAT | 30 | 0x80 | raw = (D[30] & 0x80) >> 7 |
| 22/2682 | CANFI data packet 2682 | L640 | 22 26 82 | — | 3 | 62 26 82 + D[0..51] | 55 when appended | 05/06 | HDS | Survey Infomation Battery Management(4) | IBSUML | 8 | 0xFF | raw = D[8] |
| 22/2682 | CANFI data packet 2682 | L640 | 22 26 82 | — | 3 | 62 26 82 + D[0..51] | 55 when appended | 05/06 | HDS | Survey Infomation Battery Management(4) | IBSUML | 9 | 0xFF | raw = D[9] |
| 22/2682 | CANFI data packet 2682 | L640 | 22 26 82 | — | 3 | 62 26 82 + D[0..51] | 55 when appended | 05/06 | HDS | Survey Infomation Battery Management(5) | BMSTATUS | 14 | 0xFF | raw = D[14] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled (City) | DISTRVCT | 6 | 0xFF | raw = D[6] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled (City) | DISTRVCT | 7 | 0xFF | raw = D[7] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled (City) | DISTRVCT | 8 | 0xFF | raw = D[8] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled (City) | DISTRVCT | 9 | 0xFF | raw = D[9] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled (Highway) | DISTRVHW | 10 | 0xFF | raw = D[10] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled (Highway) | DISTRVHW | 11 | 0xFF | raw = D[11] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled (Highway) | DISTRVHW | 12 | 0xFF | raw = D[12] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled (Highway) | DISTRVHW | 13 | 0xFF | raw = D[13] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption (Stopping: Idling Condition Status or Idling Stop Status) | UGASSUMST | 14 | 0xFF | raw = D[14] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption (Stopping: Idling Condition Status or Idling Stop Status) | UGASSUMST | 15 | 0xFF | raw = D[15] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption (Stopping: Idling Condition Status or Idling Stop Status) | UGASSUMST | 16 | 0xFF | raw = D[16] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption (Stopping: Idling Condition Status or Idling Stop Status) | UGASSUMST | 17 | 0xFF | raw = D[17] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption (City) | UGASSUMCT | 18 | 0xFF | raw = D[18] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption (City) | UGASSUMCT | 19 | 0xFF | raw = D[19] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption (City) | UGASSUMCT | 20 | 0xFF | raw = D[20] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption (City) | UGASSUMCT | 21 | 0xFF | raw = D[21] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption (Highway) | UGASSUMHW | 22 | 0xFF | raw = D[22] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption (Highway) | UGASSUMHW | 23 | 0xFF | raw = D[23] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption (Highway) | UGASSUMHW | 24 | 0xFF | raw = D[24] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption (Highway) | UGASSUMHW | 25 | 0xFF | raw = D[25] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Time (Stopping: Idling Condition Status or Idling Stop Status) | RUNTMST | 26 | 0xFF | raw = D[26] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Time (Stopping: Idling Condition Status or Idling Stop Status) | RUNTMST | 27 | 0xFF | raw = D[27] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Time (Stopping: Idling Condition Status or Idling Stop Status) | RUNTMST | 28 | 0xFF | raw = D[28] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Time (Stopping: Idling Condition Status or Idling Stop Status) | RUNTMST | 29 | 0xFF | raw = D[29] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time (City) | RUNTMCT | 30 | 0xFF | raw = D[30] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time (City) | RUNTMCT | 31 | 0xFF | raw = D[31] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time (City) | RUNTMCT | 32 | 0xFF | raw = D[32] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time (City) | RUNTMCT | 33 | 0xFF | raw = D[33] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time(Highway) | RUNTMHW | 34 | 0xFF | raw = D[34] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time(Highway) | RUNTMHW | 35 | 0xFF | raw = D[35] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time(Highway) | RUNTMHW | 36 | 0xFF | raw = D[36] |
| 22/2683 | CANFI data packet 2683 | L640 | 22 26 83 | — | 3 | 62 26 83 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time(Highway) | RUNTMHW | 37 | 0xFF | raw = D[37] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled Under ECON Control (City) | DISTRVCTE | 6 | 0xFF | raw = D[6] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled Under ECON Control (City) | DISTRVCTE | 7 | 0xFF | raw = D[7] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled Under ECON Control (City) | DISTRVCTE | 8 | 0xFF | raw = D[8] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled Under ECON Control (City) | DISTRVCTE | 9 | 0xFF | raw = D[9] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled Under ECON Control (Highway) | DISTRVHWE | 10 | 0xFF | raw = D[10] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled Under ECON Control (Highway) | DISTRVHWE | 11 | 0xFF | raw = D[11] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled Under ECON Control (Highway) | DISTRVHWE | 12 | 0xFF | raw = D[12] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Distance Traveled Under ECON Control (Highway) | DISTRVHWE | 13 | 0xFF | raw = D[13] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption Under ECON Control (City) | UGASSUMCTE | 14 | 0xFF | raw = D[14] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption Under ECON Control (City) | UGASSUMCTE | 15 | 0xFF | raw = D[15] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption Under ECON Control (City) | UGASSUMCTE | 16 | 0xFF | raw = D[16] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption Under ECON Control (City) | UGASSUMCTE | 17 | 0xFF | raw = D[17] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption Under ECON Control (Highway) | UGASSUMHWE | 18 | 0xFF | raw = D[18] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption Under ECON Control (Highway) | UGASSUMHWE | 19 | 0xFF | raw = D[19] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption Under ECON Control (Highway) | UGASSUMHWE | 20 | 0xFF | raw = D[20] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Consumption Under ECON Control (Highway) | UGASSUMHWE | 21 | 0xFF | raw = D[21] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time Under ECON Control (City) | RUNTMCTE | 22 | 0xFF | raw = D[22] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time Under ECON Control (City) | RUNTMCTE | 23 | 0xFF | raw = D[23] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time Under ECON Control (City) | RUNTMCTE | 24 | 0xFF | raw = D[24] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time Under ECON Control (City) | RUNTMCTE | 25 | 0xFF | raw = D[25] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time Under ECON Control (Highway) | RUNTMHWE | 26 | 0xFF | raw = D[26] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time Under ECON Control (Highway) | RUNTMHWE | 27 | 0xFF | raw = D[27] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time Under ECON Control (Highway) | RUNTMHWE | 28 | 0xFF | raw = D[28] |
| 22/2684 | CANFI data packet 2684 | L640 | 22 26 84 | — | 3 | 62 26 84 + D[0..51] | 55 when appended | None in recovered handler | HDS | Integrated Value of Engine Run Time Under ECON Control (Highway) | RUNTMHWE | 29 | 0xFF | raw = D[29] |
| 22/2685 | CANFI data packet 2685 | L640 | 22 26 85 | — | 3 | 62 26 85 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl Crank Speed #1 | MFTRQCYL1 | 6 | 0xFF | raw = D[6] |
| 22/2685 | CANFI data packet 2685 | L640 | 22 26 85 | — | 3 | 62 26 85 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl Crank Speed #2 | MFTRQCYL2 | 7 | 0xFF | raw = D[7] |
| 22/2685 | CANFI data packet 2685 | L640 | 22 26 85 | — | 3 | 62 26 85 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl Crank Speed #3 | MFTRQCYL3 | 8 | 0xFF | raw = D[8] |
| 22/2685 | CANFI data packet 2685 | L640 | 22 26 85 | — | 3 | 62 26 85 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl Crank Speed #4 | MFTRQCYL4 | 9 | 0xFF | raw = D[9] |
| 22/2685 | CANFI data packet 2685 | L640 | 22 26 85 | — | 3 | 62 26 85 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl Crank Speed #5 | MFTRQCYL5 | 10 | 0xFF | raw = D[10] |
| 22/2685 | CANFI data packet 2685 | L640 | 22 26 85 | — | 3 | 62 26 85 + D[0..51] | 55 when appended | None in recovered handler | HDS | Cyl Crank Speed #6 | MFTRQCYL6 | 11 | 0xFF | raw = D[11] |
| 22/2685 | CANFI data packet 2685 | L640 | 22 26 85 | — | 3 | 62 26 85 + D[0..51] | 55 when appended | None in recovered handler | HDS | Misfire Driving Cycle | CDCMFA | 12 | 0xFF | raw = D[12] |
| 22/2686 | CANFI data packet 2686 | L640 | 22 26 86 | — | 3 | 62 26 86 + D[0..51] | 55 when appended | None in recovered handler | HDS | LAF Sensor Lean Side Deviation Learned | KAFFC | 6 | 0xFF | raw = D[6] |
| 22/2686 | CANFI data packet 2686 | L640 | 22 26 86 | — | 3 | 62 26 86 + D[0..51] | 55 when appended | None in recovered handler | HDS | LAF Sensor Lean Side Deviation Learned (Bank1) | KAFFC-B1 | 7 | 0xFF | raw = D[7] |
| 22/2686 | CANFI data packet 2686 | L640 | 22 26 86 | — | 3 | 62 26 86 + D[0..51] | 55 when appended | None in recovered handler | HDS | LAF Sensor Learned | KAFFC-B2 | 8 | 0xFF | raw = D[8] |
| 22/2686 | CANFI data packet 2686 | L640 | 22 26 86 | — | 3 | 62 26 86 + D[0..51] | 55 when appended | None in recovered handler | HDS | LAF sensor learning(Bank1) | VLFFCINI | 13 | 0x01 | raw = (D[13] & 0x01) >> 0 |
| 22/2686 | CANFI data packet 2686 | L640 | 22 26 86 | — | 3 | 62 26 86 + D[0..51] | 55 when appended | None in recovered handler | HDS | LAF sensor learning(Bank2) | VLFFCINIB2 | 13 | 0x02 | raw = (D[13] & 0x02) >> 1 |
| 22/2688 | CANFI data packet 2688 | L640 | 22 26 88 | — | 3 | 62 26 88 + D[0..51] | 55 when appended | None in recovered handler | HDS | After Fueling Driving Cycle  #90G | CDC90GDACT | 6 | 0xFF | raw = D[6] |
| 22/2688 | CANFI data packet 2688 | L640 | 22 26 88 | — | 3 | 62 26 88 + D[0..51] | 55 when appended | None in recovered handler | HDS | After Fueling Driving Cycle  #90G | CDC90GOK | 7 | 0xFF | raw = D[7] |
| 22/2688 | CANFI data packet 2688 | L640 | 22 26 88 | — | 3 | 62 26 88 + D[0..51] | 55 when appended | None in recovered handler | HDS | After Fueling Driving Cycle  #90H | CDC90HDACT | 8 | 0xFF | raw = D[8] |
| 22/2688 | CANFI data packet 2688 | L640 | 22 26 88 | — | 3 | 62 26 88 + D[0..51] | 55 when appended | None in recovered handler | HDS | After Fueling Driving Cycle  #90H | CDC90HOK | 9 | 0xFF | raw = D[9] |
| 22/2688 | CANFI data packet 2688 | L640 | 22 26 88 | — | 3 | 62 26 88 + D[0..51] | 55 when appended | None in recovered handler | HDS | PROOK90H | PROOK90H | 19 | 0x01 | raw = (D[19] & 0x01) >> 0 |
| 22/2688 | CANFI data packet 2688 | L640 | 22 26 88 | — | 3 | 62 26 88 + D[0..51] | 55 when appended | None in recovered handler | HDS | PROFSD90H | PROFSD90H | 19 | 0x02 | raw = (D[19] & 0x02) >> 1 |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time | RUNTMISOUT | 14 | 0xFF | raw = D[14] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time | RUNTMISOUT | 15 | 0xFF | raw = D[15] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time | RUNTMISOUT | 16 | 0xFF | raw = D[16] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time | RUNTMISOUT | 17 | 0xFF | raw = D[17] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by User Operation. | RUNTMISUSR | 18 | 0xFF | raw = D[18] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by User Operation. | RUNTMISUSR | 19 | 0xFF | raw = D[19] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by User Operation. | RUNTMISUSR | 20 | 0xFF | raw = D[20] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by User Operation. | RUNTMISUSR | 21 | 0xFF | raw = D[21] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Air Conditioner. | RUNTMISAC | 22 | 0xFF | raw = D[22] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Air Conditioner. | RUNTMISAC | 23 | 0xFF | raw = D[23] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Air Conditioner. | RUNTMISAC | 24 | 0xFF | raw = D[24] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Air Conditioner. | RUNTMISAC | 25 | 0xFF | raw = D[25] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Battery Management | RUNTMISBM | 26 | 0xFF | raw = D[26] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Battery Management | RUNTMISBM | 27 | 0xFF | raw = D[27] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Battery Management | RUNTMISBM | 28 | 0xFF | raw = D[28] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Battery Management | RUNTMISBM | 29 | 0xFF | raw = D[29] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Electric Brake Vacuum Pressure Management. | RUNTMISMP | 30 | 0xFF | raw = D[30] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Electric Brake Vacuum Pressure Management. | RUNTMISMP | 31 | 0xFF | raw = D[31] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Electric Brake Vacuum Pressure Management. | RUNTMISMP | 32 | 0xFF | raw = D[32] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Electric Brake Vacuum Pressure Management. | RUNTMISMP | 33 | 0xFF | raw = D[33] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Water Temperature Condition. | RUNTMISTW | 34 | 0xFF | raw = D[34] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Water Temperature Condition. | RUNTMISTW | 35 | 0xFF | raw = D[35] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Water Temperature Condition. | RUNTMISTW | 36 | 0xFF | raw = D[36] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by Water Temperature Condition. | RUNTMISTW | 37 | 0xFF | raw = D[37] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by DC-DC Converter. | RUNTMISDC | 38 | 0xFF | raw = D[38] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by DC-DC Converter. | RUNTMISDC | 39 | 0xFF | raw = D[39] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by DC-DC Converter. | RUNTMISDC | 40 | 0xFF | raw = D[40] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by DC-DC Converter. | RUNTMISDC | 41 | 0xFF | raw = D[41] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by EPS System. | RUNTMISEPS | 42 | 0xFF | raw = D[42] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by EPS System. | RUNTMISEPS | 43 | 0xFF | raw = D[43] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by EPS System. | RUNTMISEPS | 44 | 0xFF | raw = D[44] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition by EPS System. | RUNTMISEPS | 45 | 0xFF | raw = D[45] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time When Speed Record Condition is not Correct | RUNTMISRUN | 46 | 0xFF | raw = D[46] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time When Speed Record Condition is not Correct | RUNTMISRUN | 47 | 0xFF | raw = D[47] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time When Speed Record Condition is not Correct | RUNTMISRUN | 48 | 0xFF | raw = D[48] |
| 22/2689 | CANFI data packet 2689 | L640 | 22 26 89 | — | 3 | 62 26 89 + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time When Speed Record Condition is not Correct | RUNTMISRUN | 49 | 0xFF | raw = D[49] |
| 22/268A | Firmware data record 268A | L640 | 22 26 8A | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | — | — | — | — | — | — |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | Firmware | Engine Idle Stop Mode Control | — | 7 | — | value = (D[7] >> 7) & 1 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Engine Idle Stop Mode Control | ISSTAT | 7 | 0x80 | raw = (D[7] & 0x80) >> 7 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (AT/CVT: Precondition) | ISINFTM | 9 | 0x01 | raw = (D[9] & 0x01) >> 0 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (PCU) | ISINFPCU | 9 | 0x02 | raw = (D[9] & 0x02) >> 1 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (DC-DC Converter) | ISINFDCDC | 9 | 0x04 | raw = (D[9] & 0x04) >> 2 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Brake System) | ISINFVBM | 9 | 0x08 | raw = (D[9] & 0x08) >> 3 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Battery Management System) | ISINFBAT | 9 | 0x10 | raw = (D[9] & 0x10) >> 4 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (HVAC) | ISINFAC | 9 | 0x20 | raw = (D[9] & 0x20) >> 5 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (ABS/VSA Unit) | ISINFVSA | 9 | 0x40 | raw = (D[9] & 0x40) >> 6 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (EPS Unit) | ISINFEPS | 9 | 0x80 | raw = (D[9] & 0x80) >> 7 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Barometric Air Pressure) | ISINFPA | 11 | 0x08 | raw = (D[11] & 0x08) >> 3 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Drive mode) | ISINFDMD | 11 | 0x10 | raw = (D[11] & 0x10) >> 4 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Seat Belt Unfastened) | ISINFSBSW | 11 | 0x20 | raw = (D[11] & 0x20) >> 5 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Hood Open) | ISINFHSW | 11 | 0x40 | raw = (D[11] & 0x40) >> 6 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Idle Stop Cancel Switch) | ISINFCSW | 11 | 0x80 | raw = (D[11] & 0x80) >> 7 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Vehicle Stop Judgment) | ISINFSTJD | 13 | 0x02 | raw = (D[13] & 0x02) >> 1 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Starting Assist Brake) | ISINFISAB | 13 | 0x04 | raw = (D[13] & 0x04) >> 2 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit(AT/CVT: Transition Condition) | ISINFTMTRG | 13 | 0x08 | raw = (D[13] & 0x08) >> 3 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Inclined State) | ISINFSLOPE | 13 | 0x10 | raw = (D[13] & 0x10) >> 4 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Operating Condition) | ISINFTRG | 13 | 0x20 | raw = (D[13] & 0x20) >> 5 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Driving History) | ISINFRUN | 13 | 0x40 | raw = (D[13] & 0x40) >> 6 |
| 22/268B | Engine Idle Stop Mode Control | L640 | 22 26 8B | — | 3 | 62 26 8B + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Precondition) | ISINFSTB | 13 | 0x80 | raw = (D[13] & 0x80) >> 7 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | Firmware | DC-DC Converter Information(Cst Output) | — | 51 | — | value = (D[51] >> 7) & 1 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit(Low Battery OCV) | ISINHBOCV | 7 | 0x01 | raw = (D[7] & 0x01) >> 0 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit(Large battery internal resistance) | ISINH12VRI | 7 | 0x02 | raw = (D[7] & 0x02) >> 1 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Battery Charging) | ISINFBATCH | 7 | 0x04 | raw = (D[7] & 0x04) >> 2 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | 12 Volt Battery Performance Degradation | BATTPERF | 9 | 0x20 | raw = (D[9] & 0x20) >> 5 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Survey Infomation Battery Management(7) | BATTPOR | 9 | 0x80 | raw = (D[9] & 0x80) >> 7 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Battery Deterioration) | ISINFBADBT | 9 | 0x80 | raw = (D[9] & 0x80) >> 7 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | 12 Volt Battery Internal Resistance Max History | RIPBBATMAX | 11 | 0xFF | raw = D[11] |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Low Battery Voltage) | ISINHDODR | 13 | 0x20 | raw = (D[13] & 0x20) >> 5 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (EDLC) | ISINHUCAP | 13 | 0x40 | raw = (D[13] & 0x40) >> 6 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Inhibit (Hood Open History) | ISINHHDOP | 13 | 0x80 | raw = (D[13] & 0x80) >> 7 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | BBC -ACG Cooperation Request | ACGCAPHRM | 31 | 0x02 | raw = (D[31] & 0x02) >> 1 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Contactor OFF Failure | CON309NOK | 31 | 0x40 | raw = (D[31] & 0x40) >> 6 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Contactor ON Failure | CON309MOK | 31 | 0x80 | raw = (D[31] & 0x80) >> 7 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | 12 Volt Battery Performance Degradation Status | BATTST | 32 | 0xFF | raw = D[32] |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Low Voltage Capacitor | VCAPL | 39 | 0x40 | raw = (D[39] & 0x40) >> 6 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Charge And Discharge (Ultracapacitor) | CHGCMDCAP | 40 | 0xFF | raw = D[40] |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Target Charging Voltage (Ultracapacitor) | TRGCHGCAP | 41 | 0xFF | raw = D[41] |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Target Discharging Voltage (Ultracapacitor) | TRGDCHGCAP | 42 | 0xFF | raw = D[42] |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Drive Instruction Value (Ultracapacitor) | CONCMDCAP | 43 | 0xFF | raw = D[43] |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | Capacitor Voltage Received (BBC) | VCAP | 44 | 0xFF | raw = D[44] |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | DC-DC Converter Unit State | DC2STAT | 47 | 0x02 | raw = (D[47] & 0x02) >> 1 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | DC-DC Converter Input Error 2 | DC2ERIN2 | 47 | 0x04 | raw = (D[47] & 0x04) >> 2 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | DC-DC Converter Input Error 1 | DC2ERIN1 | 47 | 0x08 | raw = (D[47] & 0x08) >> 3 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | DC-DC Converter Output Error 2 | DC2EROP2 | 47 | 0x10 | raw = (D[47] & 0x10) >> 4 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | DC-DC Converter Output Error 1 | DC2EROP1 | 47 | 0x20 | raw = (D[47] & 0x20) >> 5 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | DC-DC Converter Internal Error | DC2ERIN | 47 | 0x80 | raw = (D[47] & 0x80) >> 7 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | DC-DC Converter Cst Error | DC2ERCST | 49 | 0x40 | raw = (D[49] & 0x40) >> 6 |
| 22/268C | DC-DC Converter Information(Cst Output) | L640 | 22 26 8C | — | 3 | 62 26 8C + D[0..51] | 55 when appended | None in recovered handler | HDS | DC-DC Converter Information(Cst Output) | DC2CSTFI | 51 | 0x80 | raw = (D[51] & 0x80) >> 7 |
| 22/268D | CANFI data packet 268D | L640 | 22 26 8D | — | 3 | 62 26 8D + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time (Transmission) | RUNTMISTM | 6 | 0xFF | raw = D[6] |
| 22/268D | CANFI data packet 268D | L640 | 22 26 8D | — | 3 | 62 26 8D + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time (Transmission) | RUNTMISTM | 7 | 0xFF | raw = D[7] |
| 22/268D | CANFI data packet 268D | L640 | 22 26 8D | — | 3 | 62 26 8D + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time (Transmission) | RUNTMISTM | 8 | 0xFF | raw = D[8] |
| 22/268D | CANFI data packet 268D | L640 | 22 26 8D | — | 3 | 62 26 8D + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time (Transmission) | RUNTMISTM | 9 | 0xFF | raw = D[9] |
| 22/268D | CANFI data packet 268D | L640 | 22 26 8D | — | 3 | 62 26 8D + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time (Transmission Judged) | RUNTMISCLM | 10 | 0xFF | raw = D[10] |
| 22/268D | CANFI data packet 268D | L640 | 22 26 8D | — | 3 | 62 26 8D + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time (Transmission Judged) | RUNTMISCLM | 11 | 0xFF | raw = D[11] |
| 22/268D | CANFI data packet 268D | L640 | 22 26 8D | — | 3 | 62 26 8D + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time (Transmission Judged) | RUNTMISCLM | 12 | 0xFF | raw = D[12] |
| 22/268D | CANFI data packet 268D | L640 | 22 26 8D | — | 3 | 62 26 8D + D[0..51] | 55 when appended | None in recovered handler | HDS | Idle Stop Prohibition Integration Time (Transmission Judged) | RUNTMISCLM | 13 | 0xFF | raw = D[13] |
| 22/268E | CANFI data packet 268E | L640 | 22 26 8E | — | 3 | 62 26 8E + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Pressure Direct Injection System | PFDIO | 6 | 0xFF | raw = D[6] |
| 22/268E | CANFI data packet 268E | L640 | 22 26 8E | — | 3 | 62 26 8E + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Pressure Direct Injection System | PFDIO | 7 | 0xFF | raw = D[7] |
| 22/268E | CANFI data packet 268E | L640 | 22 26 8E | — | 3 | 62 26 8E + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Pressure Converted From PF Sensor | PFDIREL | 8 | 0xFF | raw = D[8] |
| 22/268E | CANFI data packet 268E | L640 | 22 26 8E | — | 3 | 62 26 8E + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Pressure Converted From PF Sensor | PFDIREL | 9 | 0xFF | raw = D[9] |
| 22/268E | CANFI data packet 268E | L640 | 22 26 8E | — | 3 | 62 26 8E + D[0..51] | 55 when appended | None in recovered handler | HDS | Relief Valve | PFOVR | 11 | 0x40 | raw = (D[11] & 0x40) >> 6 |
| 22/268E | CANFI data packet 268E | L640 | 22 26 8E | — | 3 | 62 26 8E + D[0..51] | 55 when appended | None in recovered handler | HDS | Relief Valve | RVLVOPN | 11 | 0x80 | raw = (D[11] & 0x80) >> 7 |
| 22/268E | CANFI data packet 268E | L640 | 22 26 8E | — | 3 | 62 26 8E + D[0..51] | 55 when appended | None in recovered handler | HDS | Fuel Pressure Converted From PF Sensor | PFDI | 12 | 0xFF | raw = D[12] |
| 22/268E | CANFI data packet 268E | L640 | 22 26 8E | — | 3 | 62 26 8E + D[0..51] | 55 when appended | None in recovered handler | HDS | Boost Voltage for Direct Injection | VCHGINPHY | 46 | 0xFF | raw = D[46] |
| 22/268E | CANFI data packet 268E | L640 | 22 26 8E | — | 3 | 62 26 8E + D[0..51] | 55 when appended | None in recovered handler | HDS | Boost Voltage for Direct Injection | VCHGINPHY | 47 | 0xFF | raw = D[47] |
| 22/268E | CANFI data packet 268E | L640 | 22 26 8E | — | 3 | 62 26 8E + D[0..51] | 55 when appended | None in recovered handler | HDS | Downstream Voltage of the Injector Relay | VBINJPHY | 48 | 0xFF | raw = D[48] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | Entry of ACGF Duty Outputs Value | DACGFW | 6 | 0xFF | raw = D[6] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | Entry of ACGF Duty Outputs Value | DACGFW | 7 | 0xFF | raw = D[7] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | Secondary O2 Outputs Heater Voltage Value | VSO2HTW | 8 | 0xFF | raw = D[8] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | Secondary O2 Outputs Heater Voltage Value | VSO2HTW | 9 | 0xFF | raw = D[9] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | Fuel Learning | ISINFFMA | 11 | 0x04 | raw = (D[11] & 0x04) >> 2 |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | Knocking Signal Input Which Was Processed | NLBSH | 12 | 0xFF | raw = D[12] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | OFMSNDKH1 | OFMSNDKH1 | 16 | 0xFF | raw = D[16] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | OFMSNDKH1 | OFMSNDKH1 | 17 | 0xFF | raw = D[17] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | OFMSNDKH2 | OFMSNDKH2 | 18 | 0xFF | raw = D[18] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | OFMSNDKH2 | OFMSNDKH2 | 19 | 0xFF | raw = D[19] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | LUTSKZYL0 | LUTSKZYL0 | 20 | 0xFF | raw = D[20] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | LUTSKZYL0 | LUTSKZYL0 | 21 | 0xFF | raw = D[21] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | LUTSKZYL3 | LUTSKZYL3 | 22 | 0xFF | raw = D[22] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | LUTSKZYL3 | LUTSKZYL3 | 23 | 0xFF | raw = D[23] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | LUTSKZYL1 | LUTSKZYL1 | 24 | 0xFF | raw = D[24] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | LUTSKZYL1 | LUTSKZYL1 | 25 | 0xFF | raw = D[25] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | LUTSKZYL2 | LUTSKZYL2 | 26 | 0xFF | raw = D[26] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | LUTSKZYL2 | LUTSKZYL2 | 27 | 0xFF | raw = D[27] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | WKRATST | WKRATST | 28 | 0xFF | raw = D[28] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | FTEAD | FTEAD | 29 | 0xFF | raw = D[29] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | FTEAD | FTEAD | 30 | 0xFF | raw = D[30] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | TRQDIFADP | TRQDIFADP | 31 | 0xFF | raw = D[31] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | TRQDIFADP | TRQDIFADP | 32 | 0xFF | raw = D[32] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | OSCAV | OSCAV | 33 | 0xFF | raw = D[33] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | OSCAV | OSCAV | 34 | 0xFF | raw = D[34] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | Cylinder1 individual lambda deviation | FIBEFA1 | 37 | 0xFF | raw = D[37] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | Cylinder2 individual lambda deviation | FIBEFA2 | 38 | 0xFF | raw = D[38] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | Cylinder3 individual lambda deviation | FIBEFA3 | 49 | 0xFF | raw = D[49] |
| 22/268F | CANFI data packet 268F | HDS only | 22 26 8F | — | 3 | — | — | — | HDS | Cylinder4 individual lambda deviation | FIBEFA4 | 50 | 0xFF | raw = D[50] |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Tank Internal Pressure | PTANKSLD | 6 | 0xFF | raw = D[6] |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Tank Internal Pressure | PTANKSLD | 7 | 0xFF | raw = D[7] |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Leak Detection of ELCM | ELCMCOND | 9 | 0x01 | raw = (D[9] & 0x01) >> 0 |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Vacuum Pump Driver (Diag Signal) of ELCM | ELCMPMPR | 9 | 0x04 | raw = (D[9] & 0x04) >> 2 |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Vacuum Pump Turning on Order Value of ELCM | ELCMPMP | 9 | 0x08 | raw = (D[9] & 0x08) >> 3 |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | CCV Drive Circuit of ELCM | CCVR | 9 | 0x10 | raw = (D[9] & 0x10) >> 4 |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | CCV Turning on Order Value of ELCM | CCV | 9 | 0x20 | raw = (D[9] & 0x20) >> 5 |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Drive Circuit of FTCV | FTCVR | 9 | 0x40 | raw = (D[9] & 0x40) >> 6 |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Fuel Vapor Containment Valve | FTCV | 9 | 0x80 | raw = (D[9] & 0x80) >> 7 |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Absolute Pressure of ELCM Pressure Sensor | PELCM | 10 | 0xFF | raw = D[10] |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Absolute Pressure of ELCM Pressure Sensor | PELCM | 11 | 0xFF | raw = D[11] |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Mode Status of ELCM Leak Detection | ELCMSTATUS | 12 | 0xFF | raw = D[12] |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Lid Open Close Condition | LIDMSW | 14 | 0x10 | raw = (D[14] & 0x10) >> 4 |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Drive Circuit of Lid Open Solenoid Value | LIDSOLR | 14 | 0x20 | raw = (D[14] & 0x20) >> 5 |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Lid Open Solenoid Value | LIDSOL | 14 | 0x40 | raw = (D[14] & 0x40) >> 6 |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Lid Open Switch | LIDOPSW | 14 | 0x80 | raw = (D[14] & 0x80) >> 7 |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Heater Temperature | HTRTW | 15 | 0xFF | raw = D[15] |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Heater Temperature | HTRTW | 16 | 0xFF | raw = D[16] |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Aircon 3 State Valve Condition(Meter - F-CAN) | HTRVLVSTS | 17 | 0xFF | raw = D[17] |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Aircon 3 State Valve Malfunction(Meter - F-CAN) | HTRVLVFAIL | 19 | 0x80 | raw = (D[19] & 0x80) >> 7 |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Purge Control Solenoid (Pcs2) Duty | DPCS2 | 38 | 0xFF | raw = D[38] |
| 22/2690 | CANFI data packet 2690 | HDS only | 22 26 90 | — | 3 | — | — | — | HDS | Wake Up Requirements Signal | MTWUCBHIST | 47 | 0x80 | raw = (D[47] & 0x80) >> 7 |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | HEV System Start-Up Complete | HEVSTBY | 7 | 0x40 | raw = (D[7] & 0x40) >> 6 |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | System Ready | SYSRDY | 7 | 0x80 | raw = (D[7] & 0x80) >> 7 |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | Vehicle Operation Status | HEVOPSTAT | 8 | 0xFF | raw = D[8] |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | Target Speed of Electric Water Pump | EWPO | 28 | 0xFF | raw = D[28] |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | Target Speed of Electric Water Pump | EWPO | 29 | 0xFF | raw = D[29] |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | Speed of Electric Water Pump | EWPREL | 30 | 0xFF | raw = D[30] |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | Speed of Electric Water Pump | EWPREL | 31 | 0xFF | raw = D[31] |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | Duty Drive of Electric Water Pump | DEWP | 32 | 0xFF | raw = D[32] |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | Target Engine Speed Output | NEOBJ | 33 | 0xFF | raw = D[33] |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | Target Engine Speed Output | NEOBJ | 34 | 0xFF | raw = D[34] |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | 1TDC Generator Motor Pulse | GENPLSTDC | 35 | 0xFF | raw = D[35] |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | 1TDC Generator Motor Pulse | GENPLSTDC | 36 | 0xFF | raw = D[36] |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | Accumlation Time of Engoine Abeyance | EOFFTMR | 37 | 0xFF | raw = D[37] |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | Accumlation Time of Engoine Abeyance | EOFFTMR | 38 | 0xFF | raw = D[38] |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | VTEC Control Changes To Hi V/T | VTECSTAT | 40 | 0x10 | raw = (D[40] & 0x10) >> 4 |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | Fuel Cut By ECVT Mode | ECVTFC | 40 | 0x40 | raw = (D[40] & 0x40) >> 6 |
| 22/2691 | CANFI data packet 2691 | HDS only | 22 26 91 | — | 3 | — | — | — | HDS | Engine Start By Aircon System | ACENGONRQ | 40 | 0x80 | raw = (D[40] & 0x80) >> 7 |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | ECVT Mode Target Battery Power | PWBOBJECVT | 6 | 0xFF | raw = D[6] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | ECVT Mode Target Battery Power | PWBOBJECVT | 7 | 0xFF | raw = D[7] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | O/D Mode Target Battery Power | PWBOBJLU | 8 | 0xFF | raw = D[8] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | O/D Mode Target Battery Power | PWBOBJLU | 9 | 0xFF | raw = D[9] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Battery Power | BATPW | 10 | 0xFF | raw = D[10] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Battery Power | BATPW | 11 | 0xFF | raw = D[11] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Crankshaft Target Torque | TQECCMD | 12 | 0xFF | raw = D[12] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Crankshaft Target Torque | TQECCMD | 13 | 0xFF | raw = D[13] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Traction Motor Torque Order Value | TQMOTCMD | 14 | 0xFF | raw = D[14] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Traction Motor Torque Order Value | TQMOTCMD | 15 | 0xFF | raw = D[15] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Generator Motor Torque Order Value | TQGENCMD | 16 | 0xFF | raw = D[16] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Generator Motor Torque Order Value | TQGENCMD | 17 | 0xFF | raw = D[17] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Target Engine Output Value | PWEOBJ | 18 | 0xFF | raw = D[18] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Target Engine Output Value | PWEOBJ | 19 | 0xFF | raw = D[19] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Crankshaft Estimated Torque | TQCRKENG | 20 | 0xFF | raw = D[20] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Crankshaft Estimated Torque | TQCRKENG | 21 | 0xFF | raw = D[21] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Avoidance Control by P/T Vibration | PTRSNLMT | 23 | 0x08 | raw = (D[23] & 0x08) >> 3 |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Evades Continuation Operation of P/T Vibration | PTRSNEVLMP | 23 | 0x10 | raw = (D[23] & 0x10) >> 4 |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Engine Stall by Deterioration of Power Generation | GENSTL | 23 | 0x20 | raw = (D[23] & 0x20) >> 5 |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Possible Condition of Power Generation | GENOK | 23 | 0x40 | raw = (D[23] & 0x40) >> 6 |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Impossible Condition of Power Generation | GENNG | 23 | 0x80 | raw = (D[23] & 0x80) >> 7 |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | System Start Up Status(Hybrid) | SYSACTSTAT | 30 | 0xFF | raw = D[30] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Drive Device Status(Hybrid) | SYSDRVSTAT | 31 | 0xFF | raw = D[31] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Drive Device Status(HEV System) | RDYDRVSTAT | 32 | 0xFF | raw = D[32] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | EV Running Time of Latest | EVTIMELST | 38 | 0xFF | raw = D[38] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | EV Running Time of Latest | EVTIMELST | 39 | 0xFF | raw = D[39] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | EV Disabled State Status | EVPRHSTAT | 40 | 0xFF | raw = D[40] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | EV Disabled State Status | EVPRHSTAT | 41 | 0xFF | raw = D[41] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Engine Start Request Status | ENGSRQSTAT | 42 | 0xFF | raw = D[42] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Engine Start Request Status | ENGSRQSTAT | 43 | 0xFF | raw = D[43] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Target Torque (Drive Motor or Generator Motor) | TQMOTCMDG | 46 | 0xFF | raw = D[46] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Target Torque (Drive Motor or Generator Motor) | TQMOTCMDG | 47 | 0xFF | raw = D[47] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Target Torque (Motor Speed) | NMOTCMDG | 48 | 0xFF | raw = D[48] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Target Torque (Motor Speed) | NMOTCMDG | 49 | 0xFF | raw = D[49] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Motor Control Direction Mode | MOTCMDGMD | 50 | 0xFF | raw = D[50] |
| 22/2692 | CANFI data packet 2692 | HDS only | 22 26 92 | — | 3 | — | — | — | HDS | Change Status ( ENG and EV) | ENGEVSTAT | 51 | 0xFF | raw = D[51] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Intake Air Sensor | INTAAD | 6 | 0xFF | raw = D[6] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Intake Air Sensor | INTAPHY | 7 | 0xFF | raw = D[7] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Intake Temperature When System Start Up | INTASYSOK | 8 | 0xFF | raw = D[8] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Intake Temperature of First Time After Engine Start | INTAINI | 9 | 0xFF | raw = D[9] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Intake Temperature of First Time After Engine Start(Min) | INTAMIN | 10 | 0xFF | raw = D[10] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Intake Temperature of First Time After Engine Start(Max) | INTAMAX | 11 | 0xFF | raw = D[11] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Target Torque (Idle Speed) | TQTRGSLW | 22 | 0xFF | raw = D[22] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Target Torque (Idle Speed) | TQTRGSLW | 23 | 0xFF | raw = D[23] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Idle Device Torque | TQFRCSLW | 24 | 0xFF | raw = D[24] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Idle Device Torque | TQFRCSLW | 25 | 0xFF | raw = D[25] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Engine Torque Target (Ignition Timing) | TQFSTTM | 26 | 0xFF | raw = D[26] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Engine Torque Target (Ignition Timing) | TQFSTTM | 27 | 0xFF | raw = D[27] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Engine Torque Target (Th Control) | TQSLWTM | 28 | 0xFF | raw = D[28] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Engine Torque Target (Th Control) | TQSLWTM | 29 | 0xFF | raw = D[29] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Estimated Crank End Engine Torque | TQCRKENCAI | 30 | 0xFF | raw = D[30] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Estimated Crank End Engine Torque | TQCRKENCAI | 31 | 0xFF | raw = D[31] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Target Crank End Torque Value | TQSELCT | 32 | 0xFF | raw = D[32] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Target Crank End Torque Value | TQSELCT | 33 | 0xFF | raw = D[33] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Target Idle Torque Correction Learning | KTQFRCN | 34 | 0xFF | raw = D[34] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Target Idle Torque Correction Learning | KTQFRCN | 35 | 0xFF | raw = D[35] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Idle Engine Speed F/B Correction Torque | TQIFB | 36 | 0xFF | raw = D[36] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Idle Engine Speed F/B Correction Torque | TQIFB | 37 | 0xFF | raw = D[37] |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Target Idle Torque (Learning Value Calculation) | KTQNCAL | 39 | 0x10 | raw = (D[39] & 0x10) >> 4 |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Target Idle Torque (This D / C Learning Terminated) | KTQEND | 39 | 0x20 | raw = (D[39] & 0x20) >> 5 |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Idle Learning (Torque) | KTQEND0 | 39 | 0x40 | raw = (D[39] & 0x40) >> 6 |
| 22/2693 | CANFI data packet 2693 | HDS only | 22 26 93 | — | 3 | — | — | — | HDS | Target Idle Torque (Learning Permission) | KTQCND | 39 | 0x80 | raw = (D[39] & 0x80) >> 7 |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Knock Retard Cyl1 | KNRTD1 | 7 | 0xFF | raw = D[7] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Knock Retard Cyl2 | KNRTD2 | 8 | 0xFF | raw = D[8] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Knock Retard Cyl3 | KNRTD3 | 9 | 0xFF | raw = D[9] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Knock Retard Cyl4 | KNRTD4 | 10 | 0xFF | raw = D[10] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Desired Engine Flywheel Torque | TORQDSRD | 11 | 0xFF | raw = D[11] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Actual Engine Flywheel Torque | TORQACT | 12 | 0xFF | raw = D[12] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Injector Heater Duty | INJHTRDUTY | 13 | 0xFF | raw = D[13] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Fuel Injector Heaters Temperature | INJTEMP | 14 | 0xFF | raw = D[14] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Fuel Injector Heaters Temperature | INJTEMP | 15 | 0xFF | raw = D[15] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | QTECACCT | QTECACCT | 16 | 0xFF | raw = D[16] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Injector Heater Activation | INJHTRON | 17 | 0x01 | raw = (D[17] & 0x01) >> 0 |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | INJHTOK | INJHTOK | 17 | 0x02 | raw = (D[17] & 0x02) >> 1 |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Torque Converter Turbine Speed | NTURB | 18 | 0xFF | raw = D[18] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Torque Converter Turbine Speed | NTURB | 19 | 0xFF | raw = D[19] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | IGP Voltage | IGP | 20 | 0xFF | raw = D[20] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | LT Knock Retard | KIGKNLONG | 21 | 0xFF | raw = D[21] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | A/C Blower Voltage | BLOWERV | 22 | 0xFF | raw = D[22] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Rear Defog Relay | RRDEFOG | 23 | 0x01 | raw = (D[23] & 0x01) >> 0 |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Front Deice | FRDEICE | 23 | 0x02 | raw = (D[23] & 0x02) >> 1 |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Front Wiper Speed | WIPERSPD | 24 | 0xFF | raw = D[24] |
| 22/2694 | CANFI data packet 2694 | HDS only | 22 26 94 | — | 3 | — | — | — | HDS | Front Lighting Status | HLIGHTS | 25 | 0xFF | raw = D[25] |
| 22/2695 | CANFI data packet 2695 | HDS only | 22 26 95 | — | 3 | — | — | — | HDS | ATF Temperature of The Rear Motor in TMU | TDIFFAW | 32 | 0xFF | raw = D[32] |
| 22/2695 | CANFI data packet 2695 | HDS only | 22 26 95 | — | 3 | — | — | — | HDS | ATF Temperature of The Rear Motor in TMU | TDIFFAW | 33 | 0xFF | raw = D[33] |
| 22/2695 | CANFI data packet 2695 | HDS only | 22 26 95 | — | 3 | — | — | — | HDS | EOP Rotation Speed Command Value in TMU | RFEOPAW | 36 | 0xFF | raw = D[36] |
| 22/2695 | CANFI data packet 2695 | HDS only | 22 26 95 | — | 3 | — | — | — | HDS | EOP Rotation Speed Command Value in TMU | RFEOPAW | 37 | 0xFF | raw = D[37] |
| 22/2697 | CANFI data packet 2697 | HDS only | 22 26 97 | — | 3 | — | — | — | HDS | Injector Heater on Duty | DINJHT | 6 | 0xFF | raw = D[6] |
| 22/2697 | CANFI data packet 2697 | HDS only | 22 26 97 | — | 3 | — | — | — | HDS | Injector Heater Power | PWINJHT | 7 | 0xFF | raw = D[7] |
| 22/2698 | CANFI data packet 2698 | HDS only | 22 26 98 | — | 3 | — | — | — | HDS | CNG Control Unit Battery Voltage | CNGVB | 6 | 0xFF | raw = D[6] |
| 22/2698 | CANFI data packet 2698 | HDS only | 22 26 98 | — | 3 | — | — | — | HDS | CNG Control Unit IG1 Voltage | CNGVIG1 | 7 | 0xFF | raw = D[7] |
| 22/2698 | CANFI data packet 2698 | HDS only | 22 26 98 | — | 3 | — | — | — | HDS | CNG PRESSURE REGULATER SHUT OFF VALVE | CNGCVLVR | 11 | 0x40 | raw = (D[11] & 0x40) >> 6 |
| 22/2698 | CANFI data packet 2698 | HDS only | 22 26 98 | — | 3 | — | — | — | HDS | CNG TANK SHUT OFF VALVE | CNGCVLVT | 11 | 0x80 | raw = (D[11] & 0x80) >> 7 |
| 22/2698 | CANFI data packet 2698 | HDS only | 22 26 98 | — | 3 | — | — | — | HDS | CNG Tank Internal Combustion Pressure Sensor | CNGPF0AD | 14 | 0xFF | raw = D[14] |
| 22/2698 | CANFI data packet 2698 | HDS only | 22 26 98 | — | 3 | — | — | — | HDS | CNG PF0 Sensor | CNGPF0 | 15 | 0xFF | raw = D[15] |
| 22/2698 | CANFI data packet 2698 | HDS only | 22 26 98 | — | 3 | — | — | — | HDS | CNG Injection Rail Internal Pressure Sensor | CNGPF2AD | 16 | 0xFF | raw = D[16] |
| 22/2698 | CANFI data packet 2698 | HDS only | 22 26 98 | — | 3 | — | — | — | HDS | CNG PF2 Sensor | CNGPF2A | 17 | 0xFF | raw = D[17] |
| 22/2698 | CANFI data packet 2698 | HDS only | 22 26 98 | — | 3 | — | — | — | HDS | CNG Injection Rail Internal Temp Sensor | CNGTF2AD | 18 | 0xFF | raw = D[18] |
| 22/2698 | CANFI data packet 2698 | HDS only | 22 26 98 | — | 3 | — | — | — | HDS | CNG Injection Rail Temperature | CNGTF2 | 19 | 0xFF | raw = D[19] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Freezing Information | FRZEWG | 7 | 0x40 | raw = (D[7] & 0x40) >> 6 |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Learned Information | KWGEND | 7 | 0x80 | raw = (D[7] & 0x80) >> 7 |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Voltage From Lift Sensor | WGLIFT | 8 | 0xFF | raw = D[8] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Actual Lift | WGLIFTPHY | 9 | 0xFF | raw = D[9] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Actual Lift | WGLIFTPHY | 10 | 0xFF | raw = D[10] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Target Lift | WGLCMD | 11 | 0xFF | raw = D[11] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Target Lift | WGLCMD | 12 | 0xFF | raw = D[12] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Battery Voltage | VBACT | 13 | 0xFF | raw = D[13] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Learned Value | KWGL | 14 | 0xFF | raw = D[14] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Learned Value | KWGL | 15 | 0xFF | raw = D[15] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Output Duty | DEWG | 16 | 0xFF | raw = D[16] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | AEVSTT | AEVSTT | 23 | 0x10 | raw = (D[23] & 0x10) >> 4 |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | Turbocharger Bypass Control Valve Status | EABVSTT | 23 | 0x40 | raw = (D[23] & 0x40) >> 6 |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | Intake Air High Temperature History | TQSAVEIC | 23 | 0x80 | raw = (D[23] & 0x80) >> 7 |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | NAEV1 | NAEV1 | 24 | 0xFF | raw = D[24] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | NAEV2 | NAEV2 | 25 | 0xFF | raw = D[25] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | MAP Sensor | MAP2 | 26 | 0xFF | raw = D[26] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Freezing Information Bank2 | FRZEWGB2 | 31 | 0x40 | raw = (D[31] & 0x40) >> 6 |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Learned Information  Bank2 | KWGENDB2 | 31 | 0x80 | raw = (D[31] & 0x80) >> 7 |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Voltage From Lift Sensor Bank2 | WGLIFTB2 | 32 | 0xFF | raw = D[32] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Actual Lift Bank2 | WGLIFTPHYB2 | 33 | 0xFF | raw = D[33] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Actual Lift Bank2 | WGLIFTPHYB2 | 34 | 0xFF | raw = D[34] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Learned Value Bank2 | KWGLB2 | 35 | 0xFF | raw = D[35] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Learned Value Bank2 | KWGLB2 | 36 | 0xFF | raw = D[36] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | EWG Output Duty Bank2 | DEWGB2 | 37 | 0xFF | raw = D[37] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | Electric Low Temperature Coolant Pump Speed | EWPICREV | 47 | 0xFF | raw = D[47] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | Electric Low Temperature Coolant Pump Speed | EWPICREV | 48 | 0xFF | raw = D[48] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | %%%AEV1 valve actual angle | AEVAACT1 | 49 | 0xFF | raw = D[49] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | %%%AEV2 valve actual angle | AEVAACT2 | 50 | 0xFF | raw = D[50] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | %%%AEV1 valve command angle | AEVARD1 | 51 | 0xFF | raw = D[51] |
| 22/2699 | CANFI data packet 2699 | HDS only | 22 26 99 | — | 3 | — | — | — | HDS | %%%AEV2 valve command angle | AEVARD2 | 52 | 0xFF | raw = D[52] |
| 22/269A | CANFI data packet 269A | HDS only | 22 26 9A | — | 3 | — | — | — | HDS | Torque Monitor(Acceletor Pedal Position) | TQMAPREQ | 6 | 0xFF | raw = D[6] |
| 22/269A | CANFI data packet 269A | HDS only | 22 26 9A | — | 3 | — | — | — | HDS | Torque Monitor(The Fast Torque Value) | TQMCMDENGFA | 7 | 0xFF | raw = D[7] |
| 22/269A | CANFI data packet 269A | HDS only | 22 26 9A | — | 3 | — | — | — | HDS | Torque Monitor(The Slow Torque Value) | TQMCMDENGSL | 8 | 0xFF | raw = D[8] |
| 22/269A | CANFI data packet 269A | HDS only | 22 26 9A | — | 3 | — | — | — | HDS | Tqrque Monitor(Accelerate Hazard Judging) | TQMACCHZD | 9 | 0xFF | raw = D[9] |
| 22/269A | CANFI data packet 269A | HDS only | 22 26 9A | — | 3 | — | — | — | HDS | Torque Monitor(Crank End Engine Torque) | TQMCRKENG | 10 | 0xFF | raw = D[10] |
| 22/269A | CANFI data packet 269A | HDS only | 22 26 9A | — | 3 | — | — | — | HDS | Torque Monitor(Accessories Friction) | TQMFRCLOAD | 11 | 0xFF | raw = D[11] |
| 22/269A | CANFI data packet 269A | HDS only | 22 26 9A | — | 3 | — | — | — | HDS | Torque Monitor(Engine Net Torque) | TQMESTFM | 12 | 0xFF | raw = D[12] |
| 22/269A | CANFI data packet 269A | HDS only | 22 26 9A | — | 3 | — | — | — | HDS | TORQUE MONITOR(TAGET/ESTIMATED TORQUE) | TQMINTGACCFM | 13 | 0xFF | raw = D[13] |
| 22/269A | CANFI data packet 269A | HDS only | 22 26 9A | — | 3 | — | — | — | HDS | Torque Monitor(OBS Torque Monitor) | TQMVEHTGSELF | 14 | 0xFF | raw = D[14] |
| 22/269A | CANFI data packet 269A | HDS only | 22 26 9A | — | 3 | — | — | — | HDS | Torque Monitor(OBS Torque Monitor) | TQMVEHTGSELF | 15 | 0xFF | raw = D[15] |
| 22/269A | CANFI data packet 269A | HDS only | 22 26 9A | — | 3 | — | — | — | HDS | Torque Monitor(Tm Ratio) | TQMRATDODFLT | 16 | 0xFF | raw = D[16] |
| 22/269B | CANFI data packet 269B | HDS only | 22 26 9B | — | 3 | — | — | — | HDS | CMP A No Pulse Bank2 | DCAMB2 | 14 | 0xFF | raw = D[14] |
| 22/269B | CANFI data packet 269B | HDS only | 22 26 9B | — | 3 | — | — | — | HDS | CMP A Noise Bank2 | NCAMB2 | 15 | 0xFF | raw = D[15] |
| 22/269C | CANFI data packet 269C | HDS only | 22 26 9C | — | 3 | — | — | — | HDS | Fuel factor study value of No1 cylinder | KAFCYLPAIC1 | 6 | 0xFF | raw = D[6] |
| 22/269C | CANFI data packet 269C | HDS only | 22 26 9C | — | 3 | — | — | — | HDS | Fuel factor study value of No2 cylinder | KAFCYLPAIC2 | 7 | 0xFF | raw = D[7] |
| 22/269C | CANFI data packet 269C | HDS only | 22 26 9C | — | 3 | — | — | — | HDS | Fuel factor study value of No3 cylinder | KAFCYLPAIC3 | 8 | 0xFF | raw = D[8] |
| 22/269C | CANFI data packet 269C | HDS only | 22 26 9C | — | 3 | — | — | — | HDS | Fuel factor study value of No4 cylinder | KAFCYLPAIC4 | 9 | 0xFF | raw = D[9] |
| 22/269C | CANFI data packet 269C | HDS only | 22 26 9C | — | 3 | — | — | — | HDS | Fuel factor study value of No5 cylinder | KAFCYLPAIC5 | 10 | 0xFF | raw = D[10] |
| 22/269C | CANFI data packet 269C | HDS only | 22 26 9C | — | 3 | — | — | — | HDS | Fuel factor study value of No6 cylinder | KAFCYLPAIC6 | 11 | 0xFF | raw = D[11] |
| 22/269D | CANFI data packet 269D | HDS only | 22 26 9D | — | 3 | — | — | — | HDS | VTC Sol Duty Bank2 | DVTCSOLB2 | 6 | 0xFF | raw = D[6] |
| 22/269D | CANFI data packet 269D | HDS only | 22 26 9D | — | 3 | — | — | — | HDS | VTC Status (Bank2) | VTCACTB2 | 10 | 0x80 | raw = (D[10] & 0x80) >> 7 |
| 22/269D | CANFI data packet 269D | HDS only | 22 26 9D | — | 3 | — | — | — | HDS | EXVTC Sol Duty Bank2 | EXDVTCSOLB2 | 14 | 0xFF | raw = D[14] |
| 22/269D | CANFI data packet 269D | HDS only | 22 26 9D | — | 3 | — | — | — | HDS | EX VTC Advance Angle Bank2 | EXVTCABSAEAB2 | 15 | 0xFF | raw = D[15] |
| 22/269D | CANFI data packet 269D | HDS only | 22 26 9D | — | 3 | — | — | — | HDS | EX VTC Status (Bank2) | EXVTCACTB2 | 18 | 0x80 | raw = (D[18] & 0x80) >> 7 |
| 22/269D | CANFI data packet 269D | HDS only | 22 26 9D | — | 3 | — | — | — | HDS | Motor Duty Bank2 | MDUTYFB2 | 22 | 0xFF | raw = D[22] |
| 22/269D | CANFI data packet 269D | HDS only | 22 26 9D | — | 3 | — | — | — | HDS | TC Bypass Sol.V. Return Bank2 | ABVSRB2 | 29 | 0x40 | raw = (D[29] & 0x40) >> 6 |
| 22/269D | CANFI data packet 269D | HDS only | 22 26 9D | — | 3 | — | — | — | HDS | Air Bypass Sol.V. Bank2 | ABVSB2 | 29 | 0x80 | raw = (D[29] & 0x80) >> 7 |
| 22/269D | CANFI data packet 269D | HDS only | 22 26 9D | — | 3 | — | — | — | HDS | MAF Sensor Bank2 | AFMB2 | 30 | 0xFF | raw = D[30] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYMLG1 | CTYMLG1 | 6 | 0xFF | raw = D[6] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYMLG1 | CTYMLG1 | 7 | 0xFF | raw = D[7] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HMLG1 | HMLG1 | 8 | 0xFF | raw = D[8] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HMLG1 | HMLG1 | 9 | 0xFF | raw = D[9] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYSAVGAS1 | CTYSAVGAS1 | 10 | 0xFF | raw = D[10] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYSAVGAS1 | CTYSAVGAS1 | 11 | 0xFF | raw = D[11] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HSAVGAS1 | HSAVGAS1 | 12 | 0xFF | raw = D[12] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HSAVGAS1 | HSAVGAS1 | 13 | 0xFF | raw = D[13] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLTM1 | IDLTM1 | 14 | 0xFF | raw = D[14] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLTM1 | IDLTM1 | 15 | 0xFF | raw = D[15] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCRUNTM1 | DCRUNTM1 | 16 | 0xFF | raw = D[16] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCRUNTM1 | DCRUNTM1 | 17 | 0xFF | raw = D[17] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCAVEVSP1 | DCAVEVSP1 | 18 | 0xFF | raw = D[18] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLSTPTM1 | IDLSTPTM1 | 19 | 0xFF | raw = D[19] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLSTPTM1 | IDLSTPTM1 | 20 | 0xFF | raw = D[20] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLUGAS1 | IDLUGAS1 | 21 | 0xFF | raw = D[21] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLUGAS1 | IDLUGAS1 | 22 | 0xFF | raw = D[22] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCOVRALGRD1 | DCOVRALGRD1 | 23 | 0xFF | raw = D[23] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ACCELGRD1 | ACCELGRD1 | 24 | 0xFF | raw = D[24] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | BRKGRD1 | BRKGRD1 | 25 | 0xFF | raw = D[25] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLGRD1 | IDLGRD1 | 26 | 0xFF | raw = D[26] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ACCELMSG1 | ACCELMSG1 | 27 | 0xFF | raw = D[27] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | BRKMSG1 | BRKMSG1 | 28 | 0xFF | raw = D[28] |
| 22/26F0 | CANFI data packet 26F0 | L640 | 22 26 F0 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLMSG1 | IDLMSG1 | 29 | 0xFF | raw = D[29] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYMLG2 | CTYMLG2 | 6 | 0xFF | raw = D[6] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYMLG2 | CTYMLG2 | 7 | 0xFF | raw = D[7] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HMLG2 | HMLG2 | 8 | 0xFF | raw = D[8] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HMLG2 | HMLG2 | 9 | 0xFF | raw = D[9] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYSAVGAS2 | CTYSAVGAS2 | 10 | 0xFF | raw = D[10] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYSAVGAS2 | CTYSAVGAS2 | 11 | 0xFF | raw = D[11] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HSAVGAS2 | HSAVGAS2 | 12 | 0xFF | raw = D[12] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HSAVGAS2 | HSAVGAS2 | 13 | 0xFF | raw = D[13] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLTM2 | IDLTM2 | 14 | 0xFF | raw = D[14] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLTM2 | IDLTM2 | 15 | 0xFF | raw = D[15] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCRUNTM2 | DCRUNTM2 | 16 | 0xFF | raw = D[16] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCRUNTM2 | DCRUNTM2 | 17 | 0xFF | raw = D[17] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCAVEVSP2 | DCAVEVSP2 | 18 | 0xFF | raw = D[18] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLSTPTM2 | IDLSTPTM2 | 19 | 0xFF | raw = D[19] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLSTPTM2 | IDLSTPTM2 | 20 | 0xFF | raw = D[20] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLUGAS2 | IDLUGAS2 | 21 | 0xFF | raw = D[21] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLUGAS2 | IDLUGAS2 | 22 | 0xFF | raw = D[22] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCOVRALGRD2 | DCOVRALGRD2 | 23 | 0xFF | raw = D[23] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ACCELGRD2 | ACCELGRD2 | 24 | 0xFF | raw = D[24] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | BRKGRD2 | BRKGRD2 | 25 | 0xFF | raw = D[25] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLGRD2 | IDLGRD2 | 26 | 0xFF | raw = D[26] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ACCELMSG2 | ACCELMSG2 | 27 | 0xFF | raw = D[27] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | BRKMSG2 | BRKMSG2 | 28 | 0xFF | raw = D[28] |
| 22/26F1 | CANFI data packet 26F1 | L640 | 22 26 F1 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLMSG2 | IDLMSG2 | 29 | 0xFF | raw = D[29] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYMLG3 | CTYMLG3 | 6 | 0xFF | raw = D[6] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYMLG3 | CTYMLG3 | 7 | 0xFF | raw = D[7] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HMLG3 | HMLG3 | 8 | 0xFF | raw = D[8] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HMLG3 | HMLG3 | 9 | 0xFF | raw = D[9] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYSAVGAS3 | CTYSAVGAS3 | 10 | 0xFF | raw = D[10] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYSAVGAS3 | CTYSAVGAS3 | 11 | 0xFF | raw = D[11] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HSAVGAS3 | HSAVGAS3 | 12 | 0xFF | raw = D[12] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HSAVGAS3 | HSAVGAS3 | 13 | 0xFF | raw = D[13] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLTM3 | IDLTM3 | 14 | 0xFF | raw = D[14] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLTM3 | IDLTM3 | 15 | 0xFF | raw = D[15] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCRUNTM3 | DCRUNTM3 | 16 | 0xFF | raw = D[16] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCRUNTM3 | DCRUNTM3 | 17 | 0xFF | raw = D[17] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCAVEVSP3 | DCAVEVSP3 | 18 | 0xFF | raw = D[18] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLSTPTM3 | IDLSTPTM3 | 19 | 0xFF | raw = D[19] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLSTPTM3 | IDLSTPTM3 | 20 | 0xFF | raw = D[20] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLUGAS3 | IDLUGAS3 | 21 | 0xFF | raw = D[21] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLUGAS3 | IDLUGAS3 | 22 | 0xFF | raw = D[22] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCOVRALGRD3 | DCOVRALGRD3 | 23 | 0xFF | raw = D[23] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ACCELGRD3 | ACCELGRD3 | 24 | 0xFF | raw = D[24] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | BRKGRD3 | BRKGRD3 | 25 | 0xFF | raw = D[25] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLGRD3 | IDLGRD3 | 26 | 0xFF | raw = D[26] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ACCELMSG3 | ACCELMSG3 | 27 | 0xFF | raw = D[27] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | BRKMSG3 | BRKMSG3 | 28 | 0xFF | raw = D[28] |
| 22/26F2 | CANFI data packet 26F2 | L640 | 22 26 F2 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLMSG3 | IDLMSG3 | 29 | 0xFF | raw = D[29] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYMLG4 | CTYMLG4 | 6 | 0xFF | raw = D[6] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYMLG4 | CTYMLG4 | 7 | 0xFF | raw = D[7] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HMLG4 | HMLG4 | 8 | 0xFF | raw = D[8] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HMLG4 | HMLG4 | 9 | 0xFF | raw = D[9] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYSAVGAS4 | CTYSAVGAS4 | 10 | 0xFF | raw = D[10] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYSAVGAS4 | CTYSAVGAS4 | 11 | 0xFF | raw = D[11] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HSAVGAS4 | HSAVGAS4 | 12 | 0xFF | raw = D[12] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HSAVGAS4 | HSAVGAS4 | 13 | 0xFF | raw = D[13] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLTM4 | IDLTM4 | 14 | 0xFF | raw = D[14] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLTM4 | IDLTM4 | 15 | 0xFF | raw = D[15] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCRUNTM4 | DCRUNTM4 | 16 | 0xFF | raw = D[16] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCRUNTM4 | DCRUNTM4 | 17 | 0xFF | raw = D[17] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCAVEVSP4 | DCAVEVSP4 | 18 | 0xFF | raw = D[18] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLSTPTM4 | IDLSTPTM4 | 19 | 0xFF | raw = D[19] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLSTPTM4 | IDLSTPTM4 | 20 | 0xFF | raw = D[20] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLUGAS4 | IDLUGAS4 | 21 | 0xFF | raw = D[21] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLUGAS4 | IDLUGAS4 | 22 | 0xFF | raw = D[22] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCOVRALGRD4 | DCOVRALGRD4 | 23 | 0xFF | raw = D[23] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ACCELGRD4 | ACCELGRD4 | 24 | 0xFF | raw = D[24] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | BRKGRD4 | BRKGRD4 | 25 | 0xFF | raw = D[25] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLGRD4 | IDLGRD4 | 26 | 0xFF | raw = D[26] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ACCELMSG4 | ACCELMSG4 | 27 | 0xFF | raw = D[27] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | BRKMSG4 | BRKMSG4 | 28 | 0xFF | raw = D[28] |
| 22/26F3 | CANFI data packet 26F3 | L640 | 22 26 F3 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLMSG4 | IDLMSG4 | 29 | 0xFF | raw = D[29] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYMLG5 | CTYMLG5 | 6 | 0xFF | raw = D[6] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYMLG5 | CTYMLG5 | 7 | 0xFF | raw = D[7] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HMLG5 | HMLG5 | 8 | 0xFF | raw = D[8] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HMLG5 | HMLG5 | 9 | 0xFF | raw = D[9] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYSAVGAS5 | CTYSAVGAS5 | 10 | 0xFF | raw = D[10] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | CTYSAVGAS5 | CTYSAVGAS5 | 11 | 0xFF | raw = D[11] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HSAVGAS5 | HSAVGAS5 | 12 | 0xFF | raw = D[12] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | HSAVGAS5 | HSAVGAS5 | 13 | 0xFF | raw = D[13] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLTM5 | IDLTM5 | 14 | 0xFF | raw = D[14] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLTM5 | IDLTM5 | 15 | 0xFF | raw = D[15] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCRUNTM5 | DCRUNTM5 | 16 | 0xFF | raw = D[16] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCRUNTM5 | DCRUNTM5 | 17 | 0xFF | raw = D[17] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCAVEVSP5 | DCAVEVSP5 | 18 | 0xFF | raw = D[18] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLSTPTM5 | IDLSTPTM5 | 19 | 0xFF | raw = D[19] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLSTPTM5 | IDLSTPTM5 | 20 | 0xFF | raw = D[20] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLUGAS5 | IDLUGAS5 | 21 | 0xFF | raw = D[21] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLUGAS5 | IDLUGAS5 | 22 | 0xFF | raw = D[22] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | DCOVRALGRD5 | DCOVRALGRD5 | 23 | 0xFF | raw = D[23] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ACCELGRD5 | ACCELGRD5 | 24 | 0xFF | raw = D[24] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | BRKGRD5 | BRKGRD5 | 25 | 0xFF | raw = D[25] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLGRD5 | IDLGRD5 | 26 | 0xFF | raw = D[26] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | ACCELMSG5 | ACCELMSG5 | 27 | 0xFF | raw = D[27] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | BRKMSG5 | BRKMSG5 | 28 | 0xFF | raw = D[28] |
| 22/26F4 | CANFI data packet 26F4 | L640 | 22 26 F4 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | IDLMSG5 | IDLMSG5 | 29 | 0xFF | raw = D[29] |
| 22/3000 | fixed_ROM_identity_or_version_block_TBD | L640 | 22 30 00 | — | 3 | 62 30 00 + D[0..9] | 13 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/3001 | fixed_ROM_feature_or_version_triplet_TBD | L640 | 22 30 01 | — | 3 | 62 30 01 + D[0..2] | 6 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d00..d02 | — | D[0..2] | — | DF 00 2F [PROVEN] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d03..d05 | — | D[3..5] | — | 00 00 00 [PROVEN] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d06 | 0xFFF94E3A | D[6] | — | U8[0xFFF94E3A] [PROVEN OBD PID0D/CAN 40C page7 speed cache; producer TBD] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d07 | 0xFFF91818 | D[7] | — | low8(min(255,trunc0(S16[0xFFF91818]/40))) [PROVEN; exact listing has upper clamp only, no explicit lower clamp] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d08 | — | D[8] | — | 00 [PROVEN] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d09 | 0xFFF90F7E | D[9] | — | 0x000E3AB0(S16[0xFFF90F7E]) [PROVEN transform; barometric-state display unit TBD] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d10 | 0xFFF8F6FE | D[10] | — | low8(trunc0(S16[0xFFF8F6FE]/4)) [PROVEN MAP raw ADC-A AN8/ADR8 reduction] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d11 | 0xFFF90F9C | D[11] | — | 0x000E3AB0(S16[0xFFF90F9C]) [PROVEN transform; CORROBORATED processed-MAP domain, exact byte meaning TBD] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d12 | 0xFFF8F714 | D[12] | — | low8(trunc0(S16[0xFFF8F714]/4)) [PROVEN transform; physical channel TBD] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d13 | 0xFFF90CE0 | D[13] | — | t=U32(U16[0xFFF90CE0]*0x18BCD); h=high32(t*0x1A904A93); q=(h+((t-h)>>1))>>22; min(q,255) [PROVEN exact integer transform; physical domain TBD] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d14..d23 | — | D[14..23] | — | all zero [PROVEN] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d24 | 0xFFF912A0 | D[24] | — | sat_u8(trunc0(S16[0xFFF912A0]/40)) [PROVEN engine RPM /40] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d25 | — | D[25] | — | 00 [PROVEN] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d26 | 0xFFF91054 | D[26] | — | sat_u8(trunc0(S16[0xFFF91054]/80)) [PROVEN transform; meaning TBD] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d27 | 0xFFF911DA | D[27] | — | sat_u8(trunc0(S16[0xFFF911DA]/80)) [PROVEN transform; meaning TBD] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d28 | — | D[28] | — | 19 [PROVEN] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d29 | 0xFFF942FD, 0xFFF947D4, 0xFFF95AC8 | D[29] | — | bit4=0xFFF95AC8; bit3=0xFFF947D4; bit0=0xFFF942FD [PROVEN; flag meanings TBD] |
| 22/3004 | live_powertrain_sensor_snapshot_mixed_verified_and_TBD_fields | L640 | 22 30 04 | — | 3 | 62 30 04 + D[0..53] | 57 when appended | None in recovered handler | Firmware dossier | Data d30..d53 | — | D[30..53] | — | all zero [PROVEN] |
| 22/3008 | cached_or_persisted_3004_style_snapshot_TBD | L640 | 22 30 08 | — | 3 | 62 30 08 + D[0..53] | 57 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/300C | transformed_runtime_word_plus_ROM_04_TBD | L640 | 22 30 0C | — | 3 | 62 30 0C + D[0..2] | 6 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | ACM Control Relay | ACMRLY | 7 | 0x40 | raw = (D[7] & 0x40) >> 6 |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | ACMRQR | ACMRQR | 9 | 0x08 | raw = (D[9] & 0x08) >> 3 |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | ACMCSS | ACMCSS | 9 | 0x40 | raw = (D[9] & 0x40) >> 6 |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | ACM Unit Supply Voltage | IG1ADACM | 14 | 0xFF | raw = D[14] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | ACM Unit Supply Voltage | IG1ADACM | 15 | 0xFF | raw = D[15] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | ACM Actuator Supply Voltage | VBACM | 16 | 0xFF | raw = D[16] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | ACM Actuator Supply Voltage | VBACM | 17 | 0xFF | raw = D[17] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | Engine Speed | NEACM | 18 | 0xFF | raw = D[18] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | Engine Speed | NEACM | 19 | 0xFF | raw = D[19] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | Fr ACM Sol Min Current | IACMFL | 22 | 0xFF | raw = D[22] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | Fr ACM Sol Min Current | IACMFL | 23 | 0xFF | raw = D[23] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | Fr ACM Sol Max Current | IACMFH | 24 | 0xFF | raw = D[24] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | Fr ACM Sol Max Current | IACMFH | 25 | 0xFF | raw = D[25] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | Rr ACM Sol Min Current | IACMRL | 26 | 0xFF | raw = D[26] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | Rr ACM Sol Min Current | IACMRL | 27 | 0xFF | raw = D[27] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | Rr ACM Sol Max Current | IACMRH | 28 | 0xFF | raw = D[28] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | Rr ACM Sol Max Current | IACMRH | 29 | 0xFF | raw = D[29] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | Fr ACM Sol Current | IACMFT | 30 | 0xFF | raw = D[30] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | Fr ACM Sol Current | IACMFT | 31 | 0xFF | raw = D[31] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | Rr ACM Sol Current | IACMRT | 32 | 0xFF | raw = D[32] |
| 22/3014 | CANFI data packet 3014 | HDS only | 22 30 14 | — | 3 | — | — | — | HDS | Rr ACM Sol Current | IACMRT | 33 | 0xFF | raw = D[33] |
| 22/C180 | CANFI data packet C180 | HDS only | 22 C1 80 | — | 3 | — | — | — | HDS | RFP Equipped Data | AFPEQUIPPED | 1 | 0xFF | raw = D[1] |
| 22/C180 | CANFI data packet C180 | HDS only | 22 C1 80 | — | 3 | — | — | — | HDS | RFP Equipped Data | RFPEQUIPPED | 1 | 0xFF | raw = D[1] |
| 22/C181 | CANFI data packet C181 | HDS only | 22 C1 81 | — | 3 | — | — | — | HDS | RFP Force Customize | RFPCUSTOM | 1 | 0xFF | raw = D[1] |
| 22/C181 | CANFI data packet C181 | HDS only | 22 C1 81 | — | 3 | — | — | — | HDS | RFP Force Command | RFPFORCECOMMAND | 2 | 0xFF | raw = D[2] |
| 22/C181 | CANFI data packet C181 | HDS only | 22 C1 81 | — | 3 | — | — | — | HDS | RFP Force Current | RFPACT | 3 | 0xFF | raw = D[3] |
| 22/C181 | CANFI data packet C181 | HDS only | 22 C1 81 | — | 3 | — | — | — | HDS | Sports Mode Preset | SPORTMODE | 4 | 0xFF | raw = D[4] |
| 22/E401 | CANFI data packet E401 | HDS only | 22 E4 01 | — | 3 | — | — | — | HDS | D/C Count | NESTART | 0 | 0xFF | raw = D[0] |
| 22/E401 | CANFI data packet E401 | HDS only | 22 E4 01 | — | 3 | — | — | — | HDS | D/C Count | NESTART | 1 | 0xFF | raw = D[1] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 0 | 0xFF | raw = D[0] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | The Valid Data Length in Bytes Included in IBATMONOUT Parameters | IBATMONOUT2Dh | 0 | 0xFF | raw = D[0] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 1 | 0xFF | raw = D[1] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | The Value Specifies IBATMONOUT Parameter Format Type | IBATMONOUT01h | 1 | 0xFF | raw = D[1] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 2 | 0xFF | raw = D[2] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Four before the latest - current history - IG OFF | Imon4-1 | 2 | 0xFF | raw = D[2] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 3 | 0x03 | raw = (D[3] & 0x03) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 3 | 0xFC | raw = (D[3] & 0xFC) >> 2 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Four before the latest - current history - 1hr later | Imon4-2 | 3 | 0xFC | raw = (D[3] & 0xFC) >> 2 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 4 | 0x0F | raw = (D[4] & 0x0F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 4 | 0xF0 | raw = (D[4] & 0xF0) >> 4 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Four before the latest - current history - 2hrs later | Imon4-3 | 4 | 0xF0 | raw = (D[4] & 0xF0) >> 4 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 5 | 0x3F | raw = (D[5] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 5 | 0xC0 | raw = (D[5] & 0xC0) >> 6 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Four before the latest - current history - **hrs later | Imon4-4 | 5 | 0xC0 | raw = (D[5] & 0xC0) >> 6 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 6 | 0xFF | raw = D[6] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Four before the latest - current history - Duration | Duration4 | 7 | 0xFF | raw = D[7] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 7 | 0xFF | raw = D[7] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Four before the latest - current history - Duration | Duration4 | 8 | 0x3F | raw = (D[8] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 8 | 0x3F | raw = (D[8] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Four before the latest - current history - Discharge | Discharge4 | 9 | 0xFF | raw = D[9] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 9 | 0xFF | raw = D[9] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Four before the latest - current history - Discharge | Discharge4 | 10 | 0xFF | raw = D[10] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 10 | 0xFF | raw = D[10] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 11 | 0xFF | raw = D[11] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Three before the latest - current history - IG OFF | Imon3-1 | 11 | 0xFF | raw = D[11] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 12 | 0x03 | raw = (D[12] & 0x03) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 12 | 0xFC | raw = (D[12] & 0xFC) >> 2 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Three before the latest - current history - 1hr later | Imon3-2 | 12 | 0xFC | raw = (D[12] & 0xFC) >> 2 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 13 | 0x0F | raw = (D[13] & 0x0F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 13 | 0xF0 | raw = (D[13] & 0xF0) >> 4 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Three before the latest - current history - 2hrs later | Imon3-3 | 13 | 0xF0 | raw = (D[13] & 0xF0) >> 4 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 14 | 0x3F | raw = (D[14] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 14 | 0xC0 | raw = (D[14] & 0xC0) >> 6 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Three before the latest - current history - **hrs later | Imon3-4 | 14 | 0xC0 | raw = (D[14] & 0xC0) >> 6 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 15 | 0xFF | raw = D[15] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Three before the latest - current history - Duration | Duration3 | 16 | 0xFF | raw = D[16] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 16 | 0xFF | raw = D[16] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Three before the latest - current history - Duration | Duration3 | 17 | 0x3F | raw = (D[17] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 17 | 0x3F | raw = (D[17] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Three before the latest - current history - Discharge | Discharge3 | 18 | 0xFF | raw = D[18] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 18 | 0xFF | raw = D[18] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Three before the latest - current history - Discharge | Discharge3 | 19 | 0xFF | raw = D[19] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 19 | 0xFF | raw = D[19] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 20 | 0xFF | raw = D[20] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Two before the latest - current history - IG OFF | Imon2-1 | 20 | 0xFF | raw = D[20] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 21 | 0x03 | raw = (D[21] & 0x03) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 21 | 0xFC | raw = (D[21] & 0xFC) >> 2 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Two before the latest - current history - 1hr later | Imon2-2 | 21 | 0xFC | raw = (D[21] & 0xFC) >> 2 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 22 | 0x0F | raw = (D[22] & 0x0F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 22 | 0xF0 | raw = (D[22] & 0xF0) >> 4 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Two before the latest - current history - 2hrs later | Imon2-3 | 22 | 0xF0 | raw = (D[22] & 0xF0) >> 4 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 23 | 0x3F | raw = (D[23] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 23 | 0xC0 | raw = (D[23] & 0xC0) >> 6 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Two before the latest - current history - **hrs later | Imon2-4 | 23 | 0xC0 | raw = (D[23] & 0xC0) >> 6 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 24 | 0xFF | raw = D[24] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Two before the latest - current history - Duration | Duration2 | 25 | 0xFF | raw = D[25] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 25 | 0xFF | raw = D[25] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Two before the latest - current history - Duration | Duration2 | 26 | 0x3F | raw = (D[26] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 26 | 0x3F | raw = (D[26] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Two before the latest - current history - Discharge | Discharge2 | 27 | 0xFF | raw = D[27] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 27 | 0xFF | raw = D[27] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Two before the latest - current history - Discharge | Discharge2 | 28 | 0xFF | raw = D[28] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 28 | 0xFF | raw = D[28] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 29 | 0xFF | raw = D[29] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | One before the latest - current history - IG OFF | Imon1-1 | 29 | 0xFF | raw = D[29] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 30 | 0x03 | raw = (D[30] & 0x03) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 30 | 0xFC | raw = (D[30] & 0xFC) >> 2 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | One before the latest - current history - 1hr later | Imon1-2 | 30 | 0xFC | raw = (D[30] & 0xFC) >> 2 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 31 | 0x0F | raw = (D[31] & 0x0F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 31 | 0xF0 | raw = (D[31] & 0xF0) >> 4 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | One before the latest - current history - 2hrs later | Imon1-3 | 31 | 0xF0 | raw = (D[31] & 0xF0) >> 4 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 32 | 0x3F | raw = (D[32] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 32 | 0xC0 | raw = (D[32] & 0xC0) >> 6 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | One before the latest - current history - **hrs later | Imon1-4 | 32 | 0xC0 | raw = (D[32] & 0xC0) >> 6 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 33 | 0xFF | raw = D[33] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | One before the latest - current history - Duration | Duration1 | 34 | 0xFF | raw = D[34] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 34 | 0xFF | raw = D[34] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | One before the latest - current history - Duration | Duration1 | 35 | 0x3F | raw = (D[35] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 35 | 0x3F | raw = (D[35] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | One before the latest - current history - Discharge | Discharge1 | 36 | 0xFF | raw = D[36] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 36 | 0xFF | raw = D[36] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | One before the latest - current history - Discharge | Discharge1 | 37 | 0xFF | raw = D[37] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 37 | 0xFF | raw = D[37] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 38 | 0xFF | raw = D[38] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Latest - current history - IG OFF | Imon0-1 | 38 | 0xFF | raw = D[38] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 39 | 0x03 | raw = (D[39] & 0x03) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 39 | 0xFC | raw = (D[39] & 0xFC) >> 2 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Latest - current history - 1hr later | Imon0-2 | 39 | 0xFC | raw = (D[39] & 0xFC) >> 2 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 40 | 0x0F | raw = (D[40] & 0x0F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 40 | 0xF0 | raw = (D[40] & 0xF0) >> 4 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Latest - current history - 2hrs later | Imon0-3 | 40 | 0xF0 | raw = (D[40] & 0xF0) >> 4 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 41 | 0x3F | raw = (D[41] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 41 | 0xC0 | raw = (D[41] & 0xC0) >> 6 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Latest - current history  - **hrs later | Imon0-4 | 41 | 0xC0 | raw = (D[41] & 0xC0) >> 6 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 42 | 0xFF | raw = D[42] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Latest - current history - Duration | Duration0 | 43 | 0xFF | raw = D[43] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 43 | 0xFF | raw = D[43] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Latest - current history - Duration | Duration0 | 44 | 0x3F | raw = (D[44] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 44 | 0x3F | raw = (D[44] & 0x3F) >> 0 |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Latest - current history - Discharge | Discharge0 | 45 | 0xFF | raw = D[45] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 45 | 0xFF | raw = D[45] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Latest - current history - Discharge | Discharge0 | 46 | 0xFF | raw = D[46] |
| 22/E402 | CANFI data packet E402 | L640 | 22 E4 02 | — | 3 | 62 da | 2 | 05/06 | HDS | Battery running out analysis | IBATMONOUT | 46 | 0xFF | raw = D[46] |
| 22/E40E | Firmware data record E40E | L640 | 22 E4 0E | — | 3 | 62 da | 2 | 05/06 | — | — | — | — | — | — |
| 22/E40F | Firmware data record E40F | L640 | 22 E4 0F | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | — | — | — | — | — | — |
| 22/E411 | CANFI data packet E411 | L640 | 22 E4 11 | — | 3 | 62 da | 2 | None in recovered handler | HDS | Ignition Cycle Counter(Engine Start) | IGCYCLE | 0 | 0xFF | raw = D[0] |
| 22/E411 | CANFI data packet E411 | L640 | 22 E4 11 | — | 3 | 62 da | 2 | None in recovered handler | HDS | Ignition Cycle Counter(Engine Start) | IGCYCLE | 1 | 0xFF | raw = D[1] |
| 22/E412 | Firmware data record E412 | L640 | 22 E4 12 | — | 3 | 62 E4 12 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF84564 | 0xFFF844EA | D[0] | — | FFF844EA [PROVEN dossier table] |
| 22/E412 | Firmware data record E412 | L640 | 22 E4 12 | — | 3 | 62 E4 12 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF84566 | 0xFFF844EC | D[2] | — | FFF844EC [PROVEN dossier table] |
| 22/E412 | Firmware data record E412 | L640 | 22 E4 12 | — | 3 | 62 E4 12 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF844FC | 0xFFF844E6 | D[4] | — | FFF844E6 [PROVEN dossier table] |
| 22/E412 | Firmware data record E412 | L640 | 22 E4 12 | — | 3 | 62 E4 12 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF844FE | 0xFFF844E8 | D[6] | — | FFF844E8 [PROVEN dossier table] |
| 22/E412 | Firmware data record E412 | L640 | 22 E4 12 | — | 3 | 62 E4 12 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF844EE | 0xFFF844F8 | D[10] | — | FFF844F8 [PROVEN dossier table] |
| 22/E412 | Firmware data record E412 | L640 | 22 E4 12 | — | 3 | 62 E4 12 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF844F0 | 0xFFF844FA | D[12] | — | FFF844FA [PROVEN dossier table] |
| 22/E412 | Firmware data record E412 | L640 | 22 E4 12 | — | 3 | 62 E4 12 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF84570 | 0xFFF844F2 | D[14] | — | FFF844F2 [PROVEN dossier table] |
| 22/E412 | Firmware data record E412 | L640 | 22 E4 12 | — | 3 | 62 E4 12 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF84572 | 0xFFF844F4 | D[16] | — | FFF844F4 [PROVEN dossier table] |
| 22/E412 | Firmware data record E412 | L640 | 22 E4 12 | — | 3 | 62 E4 12 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF84568 | 0xFFF844F2 | D[18] | — | FFF844F2 [PROVEN dossier table] |
| 22/E412 | Firmware data record E412 | L640 | 22 E4 12 | — | 3 | 62 E4 12 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF845CA | 0xFFF845C8 | D[38] | — | FFF845C8 [PROVEN dossier table] |
| 22/E413 | Firmware data record E413 | L640 | 22 E4 13 | — | 3 | 62 E4 13 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF84584 | 0xFFF84508 | D[0] | — | FFF84508 [PROVEN dossier table] |
| 22/E413 | Firmware data record E413 | L640 | 22 E4 13 | — | 3 | 62 E4 13 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF84586 | 0xFFF8450A | D[2] | — | FFF8450A [PROVEN dossier table] |
| 22/E413 | Firmware data record E413 | L640 | 22 E4 13 | — | 3 | 62 E4 13 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF84590 | 0xFFF84504 | D[4] | — | FFF84504 [PROVEN dossier table] |
| 22/E413 | Firmware data record E413 | L640 | 22 E4 13 | — | 3 | 62 E4 13 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF84592 | 0xFFF84506 | D[6] | — | FFF84506 [PROVEN dossier table] |
| 22/E413 | Firmware data record E413 | L640 | 22 E4 13 | — | 3 | 62 E4 13 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF84594 | 0xFFF84530 | D[8] | — | FFF84530 [PROVEN dossier table] |
| 22/E413 | Firmware data record E413 | L640 | 22 E4 13 | — | 3 | 62 E4 13 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF84598 | 0xFFF845B0 | D[18] | — | FFF845B0 [PROVEN dossier table] |
| 22/E413 | Firmware data record E413 | L640 | 22 E4 13 | — | 3 | 62 E4 13 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF845B4 | 0xFFF84574 | D[20] | — | FFF84574 [PROVEN dossier table] |
| 22/E413 | Firmware data record E413 | L640 | 22 E4 13 | — | 3 | 62 E4 13 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | FFF845B6 | 0xFFF84576 | D[22] | — | FFF84576 [PROVEN dossier table] |
| 22/E414 | Firmware data record E414 | L640 | 22 E4 14 | — | 3 | 62 E4 14 + D[0..63] | 67 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d0..d1 | 0xFFF845EC | D[0..1] | — | BE16 u16[FFF845EC] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d2..d3 | 0xFFF845EE | D[2..3] | — | BE16 u16[FFF845EE] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d4..d5 | 0xFFF845E8 | D[4..5] | — | BE16 u16[FFF845E8] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d6..d7 | 0xFFF845EA | D[6..7] | — | BE16 u16[FFF845EA] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d20..d21 | 0xFFF845D8 | D[20..21] | — | BE16 u16[FFF845D8] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d22..d23 | 0xFFF845DA | D[22..23] | — | BE16 u16[FFF845DA] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d24..d25 | 0xFFF845DC | D[24..25] | — | BE16 u16[FFF845DC] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d26..d27 | 0xFFF845DE | D[26..27] | — | BE16 u16[FFF845DE] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d28..d29 | 0xFFF845E0 | D[28..29] | — | BE16 u16[FFF845E0] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d30..d31 | 0xFFF845E2 | D[30..31] | — | BE16 u16[FFF845E2] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d32..d33 | 0xFFF84534 | D[32..33] | — | BE16 u16[FFF84534] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d34..d35 | 0xFFF84536 | D[34..35] | — | BE16 u16[FFF84536] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d36..d37 | 0xFFF84514 | D[36..37] | — | BE16 u16[FFF84514] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d38..d39 | 0xFFF84516 | D[38..39] | — | BE16 u16[FFF84516] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d40..d41 | 0xFFF84518 | D[40..41] | — | BE16 u16[FFF84518] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d42..d43 | 0xFFF8451A | D[42..43] | — | BE16 u16[FFF8451A] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d44..d45 | 0xFFF8456C | D[44..45] | — | BE16 u16[FFF8456C] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | Data d46..d47 | 0xFFF8456E | D[46..47] | — | BE16 u16[FFF8456E] [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | padding; sentinel interpretation UNKNOWN | — | D[8..19] | — | twelve constant FF bytes [PROVEN dossier table] |
| 22/E415 | Firmware data record E415 | L640 | 22 E4 15 | — | 3 | 62 E4 15 + D[0..63] | 67 when appended | None in recovered handler | Firmware dossier | padding; sentinel interpretation UNKNOWN | — | D[48..63] | — | sixteen constant FF bytes [PROVEN dossier table] |
| 22/E416 | CANFI data packet E416 | HDS only | 22 E4 16 | — | 3 | — | — | — | HDS | Ignition Cycle Counter(System Ready) | IGCYCLE2 | 0 | 0xFF | raw = D[0] |
| 22/E416 | CANFI data packet E416 | HDS only | 22 E4 16 | — | 3 | — | — | — | HDS | Ignition Cycle Counter(System Ready) | IGCYCLE2 | 1 | 0xFF | raw = D[1] |
| 22/E416 | CANFI data packet E416 | HDS only | 22 E4 16 | — | 3 | — | — | — | HDS | EVAP0.02inch Canister Leak (Canister Leak) | CDRB90C | 4 | 0xFF | raw = D[4] |
| 22/E416 | CANFI data packet E416 | HDS only | 22 E4 16 | — | 3 | — | — | — | HDS | EVAP0.02inch Canister Leak (Canister Leak) | CDRB90C | 5 | 0xFF | raw = D[5] |
| 22/E416 | CANFI data packet E416 | HDS only | 22 E4 16 | — | 3 | — | — | — | HDS | Purge flow Check | CDRB90S | 8 | 0xFF | raw = D[8] |
| 22/E416 | CANFI data packet E416 | HDS only | 22 E4 16 | — | 3 | — | — | — | HDS | Purge flow Check | CDRB90S | 9 | 0xFF | raw = D[9] |
| 22/E416 | CANFI data packet E416 | HDS only | 22 E4 16 | — | 3 | — | — | — | HDS | EVAP0.02inch Canister Leak (Tank Leak ) | CDRB90T | 12 | 0xFF | raw = D[12] |
| 22/E416 | CANFI data packet E416 | HDS only | 22 E4 16 | — | 3 | — | — | — | HDS | EVAP0.02inch Canister Leak (Tank Leak ) | CDRB90T | 13 | 0xFF | raw = D[13] |
| 22/E416 | CANFI data packet E416 | HDS only | 22 E4 16 | — | 3 | — | — | — | HDS | Purge Flow2 / Pcs Open | CDRB90W2 | 16 | 0xFF | raw = D[16] |
| 22/E416 | CANFI data packet E416 | HDS only | 22 E4 16 | — | 3 | — | — | — | HDS | Purge Flow2 / Pcs Open | CDRB90W2 | 17 | 0xFF | raw = D[17] |
| 22/E416 | CANFI data packet E416 | HDS only | 22 E4 16 | — | 3 | — | — | — | HDS | Pcs2 Open Malfunction | CDRB99A | 22 | 0xFF | raw = D[22] |
| 22/E416 | CANFI data packet E416 | HDS only | 22 E4 16 | — | 3 | — | — | — | HDS | Pcs2 Open Malfunction | CDRB99A | 23 | 0xFF | raw = D[23] |
| 22/E41F | Firmware data record E41F | L640 | 22 E4 1F | — | 3 | 62 E4 1F + D[0..63] | 67 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E500 | Firmware data record E500 | L640 | 22 E5 00 | — | 3 | 62 E5 00 + D[0..31] | 35 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E501 | Firmware data record E501 | L640 | 22 E5 01 | — | 3 | 62 E5 01 + D[0..31] | 35 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E50A | Firmware data record E50A | L640 | 22 E5 0A | — | 3 | 62 E5 0A + D[0..95] | 99 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E50B | Firmware data record E50B | L640 | 22 E5 0B | — | 3 | 62 E5 0B + D[0..95] | 99 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E50C | Firmware data record E50C | L640 | 22 E5 0C | — | 3 | 62 E5 0C + D[0..95] | 99 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E50D | Firmware data record E50D | L640 | 22 E5 0D | — | 3 | 62 E5 0D + D[0..95] | 99 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E50E | Firmware data record E50E | L640 | 22 E5 0E | — | 3 | 62 E5 0E + D[0..95] | 99 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E50F | Firmware data record E50F | L640 | 22 E5 0F | — | 3 | 62 E5 0F + D[0..95] | 99 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E5FF | CANFI data packet E5FF | L640 | 22 E5 FF | — | 3 | 62 E5 FF + D[0..0] | 4 when appended | None in recovered handler | HDS | DBW Stuck Status | RQTHCLN | 0 | 0xFF | raw = D[0] |
| 22/E600 | Firmware data record E600 | L640 | 22 E6 00 | — | 3 | 62 E6 00 + D[0..1] | 5 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E601 | Firmware data record E601 | L640 | 22 E6 01 | — | 3 | 62 E6 01 + D[0..1] | 5 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E602 | Firmware data record E602 | L640 | 22 E6 02 | — | 3 | 62 E6 02 + D[0..2] | 6 when appended | None in recovered handler | Firmware dossier | Data d00..d01 | 0xFFF912A0 | D[0..1] | — | BE16(U16[0xFFF912A0] << 2) [PROVEN; same encoding as standard OBD PID0C, physical RPM=word/4] |
| 22/E602 | Firmware data record E602 | L640 | 22 E6 02 | — | 3 | 62 E6 02 + D[0..2] | 6 when appended | None in recovered handler | Firmware dossier | Data d02 | 0xFFF95AC8 | D[2] | — | 0xFFF95AC8!=0 ? 01 : 00 [PROVEN source/boolean; nonzero-normalized engine_idle_stop_mode_control, existing source meaning] |
| 22/E800 | Firmware data record E800 | L640 | 22 E8 00 | — | 3 | 62 E8 00 + D[0..11] | 15 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E801 | Firmware data record E801 | L640 | 22 E8 01 | — | 3 | 62 E8 01 + D[0..0] | 4 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E802 | CANFI data packet E802 | L640 | 22 E8 02 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | REOL | REOL | 0 | 0xFF | raw = D[0] |
| 22/E80E | Firmware data record E80E | L640 | 22 E8 0E | — | 3 | 62 E8 0E + D[0..7] | 11 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E813 | CANFI data packet E813 | L640 | 22 E8 13 | — | 3 | 62 E8 13 + D[0..63] | 67 when appended | 05/06 | HDS | REOL2 | REOL2 | 0 | 0xFF | raw = D[0] |
| 22/E814 | CANFI data packet E814 | L640 | 22 E8 14 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | AFCL | AFCL | 0 | 0xFF | raw = D[0] |
| 22/E816 | CANFI data packet E816 | L640 | 22 E8 16 | — | 3 | 7F 22 31 (ordinary lone/all-empty request) | 3 | Not applicable; no usable positive operation | HDS | FCOACH | FCOACH | 255 | 0xFF | raw = D[255] |
| 22/E81E | Firmware data record E81E | L640 | 22 E8 1E | — | 3 | 62 E8 1E + D[0..9] | 13 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/E81F | CANFI data packet E81F | L640 | 22 E8 1F | — | 3 | 62 E8 1F + D[0..63] | 67 when appended | 05/06 | HDS | Idle Stop Starter Counter | ISINFSRCNT | 2 | 0xFF | raw = D[2] |
| 22/E81F | CANFI data packet E81F | L640 | 22 E8 1F | — | 3 | 62 E8 1F + D[0..63] | 67 when appended | 05/06 | HDS | Idle Stop Starter Counter | ISINFSRCNT | 3 | 0xFF | raw = D[3] |
| 22/E81F | CANFI data packet E81F | L640 | 22 E8 1F | — | 3 | 62 E8 1F + D[0..63] | 67 when appended | 05/06 | HDS | Idle Stop Starter Counter | ISINFSRCNT | 4 | 0xFF | raw = D[4] |
| 22/E823 | CANFI data packet E823 | HDS only | 22 E8 23 | — | 3 | — | — | — | HDS | Pcs2 Forces Operation | FADPCS2 | 0 | 0xFF | raw = D[0] |
| 22/E82C | CANFI data packet E82C | HDS only | 22 E8 2C | — | 3 | — | — | — | HDS | AD Inhibit Status | BAT2TRU | 0 | 0xFF | raw = D[0] |
| 22/F100 | CANFI data packet F100 | L640 | 22 F1 00 | — | 3 | 62 F1 00 + D[0..3] | 7 when appended | None in recovered handler | HDS | Number of rewrite events | NREWR | 2 | 0xFF | raw = D[2] |
| 22/F100 | CANFI data packet F100 | L640 | 22 F1 00 | — | 3 | 62 F1 00 + D[0..3] | 7 when appended | None in recovered handler | HDS | Number of erasing process | NERAS | 3 | 0xFF | raw = D[3] |
| 22/F110 | CANFI data packet F110 | L640 | 22 F1 10 | — | 3 | 62 F1 10 + D[0..16] | 20 when appended | None in recovered handler | HDS | PARTNO | PARTNO | 0 | 0xFF | raw = D[0] |
| 22/F112 | Firmware data record F112 | L640 | 22 F1 12 | — | 3 | 62 F1 12 + D[0..30] | 34 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/F113 | Firmware data record F113 | L640 | 22 F1 13 | — | 3 | 62 F1 13 + D[0..16] | 20 when appended | None in recovered handler | Firmware dossier | 0xF3990, 0xF399A | — | D[0] | — | Constant 04 [PROVEN dossier table] |
| 22/F113 | Firmware data record F113 | L640 | 22 F1 13 | — | 3 | 62 F1 13 + D[0..16] | 20 when appended | None in recovered handler | Firmware dossier | captured once at 0xF399C; split calls 0xF39AA/0xF39B6; high-byte stores 0xF39B2/0xF39BE | 0xFFF8C19C | D[1..4] | — | BE32 raw word at 0xFFF8C19C [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | written at 0xF3A3A | — | D[0] | — | Constant 40 [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3CD4 | 0xFFF87F08 | D[1..4] | — | BE32 raw FFF87F08 [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3CE0 | 0xFFF87F0C | D[5..8] | — | BE32 raw FFF87F0C [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3CE4 | 0xFFF87F10 | D[9..12] | — | BE32 raw FFF87F10 [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3CE8 | 0xFFF87F14 | D[13..16] | — | BE32 raw FFF87F14 [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3CEC | 0xFFF87F18 | D[17..20] | — | BE32 raw FFF87F18 [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3CF0 | 0xFFF87F1C | D[21..24] | — | BE32 raw FFF87F1C [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3CF4 | 0xFFF87F20 | D[25..28] | — | BE32 raw FFF87F20 [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3CF8 | 0xFFF87F24 | D[29..32] | — | BE32 raw FFF87F24 [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3CFC | 0xFFF87F28 | D[33..36] | — | BE32 raw FFF87F28 [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3D00 | 0xFFF87F2C | D[37..40] | — | BE32 raw FFF87F2C [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3D04 | 0xFFF87F30 | D[41..44] | — | BE32 raw FFF87F30 [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3D08 | 0xFFF87F34 | D[45..48] | — | BE32 raw FFF87F34 [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3D0C | 0xFFF87F38 | D[49..52] | — | BE32 raw FFF87F38 [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3D10 | 0xFFF87F3C | D[53..56] | — | BE32 raw FFF87F3C [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3D14 | 0xFFF87F40 | D[57..60] | — | BE32 raw FFF87F40 [PROVEN dossier table] |
| 22/F114 | Firmware data record F114 | L640 | 22 F1 14 | — | 3 | 62 F1 14 + D[0..64] | 68 when appended | None in recovered handler | Firmware dossier | 0xF3D18 | 0xFFF87F44 | D[61..64] | — | BE32 raw FFF87F44 [PROVEN dossier table] |
| 22/F181 | Firmware data record F181 | L640 | 22 F1 81 | — | 3 | 62 F1 81 + D[0..15] | 19 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/F190 | vehicle_identifier_payload | L640 | 22 F1 90 | — | 3 | 62 F1 90 + D[0..20] | 24 when appended | None in recovered handler | HDS | VIN | VIN | 0 | 0xFF | raw = D[0] |
| 22/F806 | Firmware data record F806 | L640 | 22 F8 06 | — | 3 | 62 F8 06 + D[0..3] | 7 when appended | None in recovered handler | — | — | — | — | — | — |
| 22/FD00 | exposes three calibrated SecurityAccess constants in session 61 | L640 | 22 FD 00 | — | 3 | 62 FD 00 00 90 13 83 10 42 | 9 | None in recovered handler | — | — | — | — | — | — |
