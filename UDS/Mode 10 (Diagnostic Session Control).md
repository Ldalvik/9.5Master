# Mode 10 (Diagnostic Session Control)

| Command | Name | Source | Header | Payload | Request bytes | Response layout | Response bytes | SecurityAccess mode | Field source | Field name | Field ID | Offset / bit | Mask | Parse / decode |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 10/01 | DiagnosticSessionControl defaultSession | L640 | 10 01 | — | 2 | 50 01 | 2 | None in recovered handler | — | — | — | — | — | — |
| 10/02 | DiagnosticSessionControl programmingSession | L640 | 10 02 | — | 2 | 7F 10 78 (pending/deferred) | 3 | 01/02 | — | — | — | — | — | — |
| 10/03 | DiagnosticSessionControl extendedSession | L640 | 10 03 | — | 2 | 50 03 | 2 | None in recovered handler | — | — | — | — | — | — |
| 10/4F | Honda session 4F | L640 | 10 4F | — | 2 | 50 4F | 2 | 41/42 | — | — | — | — | — | — |
| 10/60 | Honda proprietary session 60 | L640 | 10 60 | — | 2 | 50 60 | 2 | 61/62 | — | — | — | — | — | — |
| 10/61 | Honda proprietary session 61 | L640 | 10 61 | — | 2 | 50 61 | 2 | 61/62 | — | — | — | — | — | — |
