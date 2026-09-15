# Mode 19 (Read DTC Information)

| Command | Name | Source | Header | Payload | Request bytes | Response layout | Response bytes | SecurityAccess mode | Field source | Field name | Field ID | Offset / bit | Mask | Parse / decode |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 19/01 | ReportNumberOfDTCByStatusMask | L640 | 19 01 | MASK | 3 | 59 01 CE 01 | 4 | None in recovered handler | — | — | — | — | — | — |
| 19/02 | ReportDTCByStatusMask | L640 | 19 02 | MASK | 3 | 59 02 CE | 3 | None in recovered handler | — | — | — | — | — | — |
| 19/0A | ReportSupportedDTC | L640 | 19 0A | — | 2 | 59 0A CE | 3 | None in recovered handler | — | — | — | — | — | — |
