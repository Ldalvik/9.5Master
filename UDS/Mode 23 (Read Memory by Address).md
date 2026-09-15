# Mode 23 (Read Memory by Address)

| Command | Name | Source | Header | Payload | Request bytes | Response layout | Response bytes | SecurityAccess mode | Field source | Field name | Field ID | Offset / bit | Mask | Parse / decode |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 23/ALFID=0X14 | bounded 1-4 byte memory read | L640 | 23 14 | A3 A2 A1 A0 SIZE | 7 | 63 DATA[SIZE] | 1 + SIZE (2..5) | 41/42 | — | — | — | — | — | — |
