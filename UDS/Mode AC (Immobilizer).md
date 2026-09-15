# Mode AC (Immobilizer)


| Command | Name | Source | Header | Payload | Request bytes | Response layout | Response bytes | SecurityAccess mode | Field source | Field name | Field ID | Offset / bit | Mask | Parse / decode |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| AC/00 | ReadSAI (immobilizer/S-NET) | L640 | AC 00 | — | 2 | EC 00 &lt;FFF9507C&gt; | 3 | None; capability gate FFF95077 only | Firmware | SAI | FFF9507C | response byte 2 | FF | uint8 |
| AC/01 | Read live immobilizer state | L640 | AC 01 | — | 2 | EC 01 &lt;STATUS&gt; | 3 | None; capability gate FFF95077 only | Firmware | Live immobilizer state | FFF94DEF | response byte 2 | FF | uint8; FF on demonstrated error condition |
| AC/02 | Set special/registration state control | L640 | AC 02 | — | 2 | EC 02 00 | 3 | 03/04 | Firmware | Status | — | response byte 2 | FF | constant 00 on positive response |
| AC/03 | ReadImocdCodeService - read 3-byte IMOCD from record 0x8100 | L640 | AC 03 | — | 2 | EC 03 &lt;STATUS&gt; &lt;FFF84999&gt; &lt;FFF8499A&gt; &lt;FFF8499B&gt; | 6 | 03/04 | Firmware | Status | — | response byte 2 | FF | uint8; FF denotes error form |
| AC/03 | ReadImocdCodeService - read 3-byte IMOCD from record 0x8100 | L640 | AC 03 | — | 2 | EC 03 &lt;STATUS&gt; &lt;FFF84999&gt; &lt;FFF8499A&gt; &lt;FFF8499B&gt; | 6 | 03/04 | Firmware | IMOCD | record 0x8100 / FFF84999..FFF8499B | response bytes 3..5 | FFFFFF | uint24 big-endian |
