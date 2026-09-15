# Mode 27 (Security Access)

| Command | Name | Source | Header | Payload | Request bytes | Response layout | Response bytes | SecurityAccess mode | Field source | Field name | Field ID | Offset / bit | Mask | Parse / decode |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 27/01 | level 01/02 seed; FFF94775 | L640 | 27 01 | — | 2 | 67 01 SEED_BE16 | 4 | 01/02 seed | Firmware | Seed | FFF90C82 | response bytes 2..3 | FFFF | uint16 big-endian |
| 27/02 | level 01/02 key | L640 | 27 02 | KEY_BE16 | 4 | 67 02 | 2 | 01/02 key | Firmware | Submitted key | — | request bytes 2..3 | FFFF | K=((S+0x9DD6) XOR ((S*0x8FFF) mod 0xFEDC)) & 0xFFFF when FFF95028=0; otherwise ROM parameters 0x0090,0x1383,0x1042 |
| 27/03 | level 03/04 seed; FFF95077!=0; FFF94778 | L640 | 27 03 | — | 2 | 67 03 SEED_BE16 | 4 | 03/04 seed | Firmware | Seed | FFF90C84 | response bytes 2..3 | FFFF | uint16 big-endian |
| 27/04 | level 03/04 key; FFF95077!=0 | L640 | 27 04 | KEY_BE16 | 4 | 67 04 | 2 | 03/04 key | Firmware | Submitted key | — | request bytes 2..3 | FFFF | K=(ROL16(S+0xC073,1)+ROR16(S+0x123E,3)) & 0xFFFF |
| 27/05 | generic seed plus tag 07; FFF9477B | L640 | 27 05 | — | 2 | 67 05 SEED_BE16 07 | 5 | 05/06 seed | Firmware | Seed | FFF90C86 | response bytes 2..3 | FFFF | uint16 big-endian |
| 27/05 | generic seed plus tag 07; FFF9477B | L640 | 27 05 | — | 2 | 67 05 SEED_BE16 07 | 5 | 05/06 seed | Firmware | Tag | FFF94780 | response byte 4 / request byte 4 | FF | constant 0x07 |
| 27/06 | generic key plus exact tag | L640 | 27 06 | KEY_BE16 07 | 5 | 67 06 | 2 | 05/06 key | Firmware | Submitted key | — | request bytes 2..3 | FFFF | K=(ROL16(S+0x2A15,2)*ROR16(S+0x8F9E,1)+0x6FB0) & 0xFFFF |
| 27/41 | master seed plus tag 15; FFF9477E | L640 | 27 41 | — | 2 | 67 41 SEED_BE32 15 | 7 | 41/42 seed | Firmware | Seed | FFF8CCA4 | response bytes 2..5 | FFFFFFFF | uint32 big-endian |
| 27/41 | master seed plus tag 15; FFF9477E | L640 | 27 41 | — | 2 | 67 41 SEED_BE32 15 | 7 | 41/42 seed | Firmware | Tag | FFF94781 | response byte 6 / request byte 6 | FF | constant 0x15 |
| 27/42 | master key plus exact tag | L640 | 27 42 | KEY_BE32 15 | 7 | 67 42 | 2 | 41/42 key | Firmware | Submitted key | — | request bytes 2..5 | FFFFFFFF | K=(S XOR ROR32(S+0xAA64D267,3) XOR ((S>>16)*(S&0xFFFF)) + 0xF9849207) mod 2^32; XOR terms precede final add |
| 27/61 | post-hook 0x000FC368 proprietary authorization level; FFF88DBA | L640 | 27 61 | — | 2 | 67 61 SEED_BE16 | 4 | 61/62 seed | Firmware | Seed | FFF88D90 | response bytes 2..3 | FFFF | uint16 big-endian |
| 27/62 | post-hook 0x000FC368 proprietary authorization key | L640 | 27 62 | KEY_BE16 | 4 | 67 62 | 2 | 61/62 key | Firmware | Submitted key | — | request bytes 2..3 | FFFF | K=((S*0x21)>>2) & 0xFFFF; calculated zero is rejected |
