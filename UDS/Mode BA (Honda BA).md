# Mode BA (Honda BA)

| Command | Name | Source | Header | Payload | Request bytes | Response layout | Response bytes | SecurityAccess mode | Field source | Field name | Field ID | Offset / bit | Mask | Parse / decode |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| BA/90 | Read closed persistent record set | L640 | BA 90 | <RECORD_ID_BE16> | 4 | BA read response; exact record-specific layout | VARIABLE | BA authorization state | — | — | — | — | — | — |
| BA/91 | Write closed persistent record set | L640 | BA 91 | <RECORD_ID_BE16> <DATA[...]> | VARIABLE | BA write positive response | UNKNOWN | BA authorization state | — | — | — | — | — | — |
| BA/F4 | Validate fixed 20-byte execution descriptor and set FFF88D9B | L640 | BA F4 | <EXACT_DESCRIPTOR_POINTERS_TO_FFF80030..FFF80043> | UNKNOWN | BA F4 success | UNKNOWN | Exact pointer/checksum/magic validation | — | — | — | — | — | — |
| BA/F5 | Validate FFF90000..FFF95FFF and request-supplied marker | L640 | BA F5 | <ENTRYPOINT_BE32> <MARKER_POINTER_BE32> <EXPECTED_MARKER[4]> | UNKNOWN | BA F5 success | UNKNOWN | BA authorization; F4 dependency | — | — | — | — | — | — |
