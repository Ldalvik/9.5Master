# Mode 2E (Write DID)

| Command | Name | Source | Header | Payload | Request bytes | Response layout | Response bytes | SecurityAccess mode | Field source | Field name | Field ID | Offset / bit | Mask | Parse / decode |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 2E/E800 | accepted_pending_redundant_image_staging | L640 | 2E E8 00 | DATA... | 15 | 7F 2E 78 (pending/deferred) | 3 | 05/06 | — | — | — | — | — | — |
| 2E/E801 | accepted_diagnostic_scalar_storage_readback | L640 | 2E E8 01 | DATA... | 4 | 6E E8 01 | 3 | None in recovered handler | — | — | — | — | — | — |
| 2E/E802 | FI_WRITE_REOL | HDS only | 2E E8 02 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2E/E803 | negative_only | L640 | 2E E8 03 | DATA... | &gt;=4 | [PROVEN] none. NRC behavior: 0x31 | UNKNOWN | Not applicable; no usable positive operation | — | — | — | — | — | — |
| 2E/E804 | verified_monitor_configuration_effect | L640 | 2E E8 04 | DATA... | 4 | 6E E8 04 | 3 | None in recovered handler | — | — | — | — | — | — |
| 2E/E805 | verified_monitor_configuration_effect | L640 | 2E E8 05 | DATA... | 4 | 6E E8 05 | 3 | None in recovered handler | — | — | — | — | — | — |
| 2E/E80E | accepted_diagnostic_buffer_storage_readback | L640 | 2E E8 0E | DATA... | 11 | 6E E8 0E | 3 | None in recovered handler | — | — | — | — | — | — |
| 2E/E810 | accepted_diagnostic_storage_and_readback | L640 | 2E E8 10 | DATA... | 11 | 6E E8 10 | 3 | None in recovered handler | — | — | — | — | — | — |
| 2E/E811 | negative_only | L640 | 2E E8 11 | DATA... | &gt;=4 | [PROVEN] none. NRC behavior: 0x31 | UNKNOWN | Not applicable; no usable positive operation | — | — | — | — | — | — |
| 2E/E812 | accepted_diagnostic_state_only | L640 | 2E E8 12 | DATA... | 4 | 6E E8 12 | 3 | None in recovered handler | — | — | — | — | — | — |
| 2E/E813 | verified_application_calculation_input_physical_domain_TBD | L640 | 2E E8 13 | DATA... | 67 | 6E E8 13 | 3 | 05/06 | — | — | — | — | — | — |
| 2E/E814 | FI_WRITE_AFCL | HDS only | 2E E8 14 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2E/E816 | FI_WRITE_FCOACH | HDS only | 2E E8 16 | UNKNOWN | NOT REVIEWED | — | — | — | — | — | — | — | — | — |
| 2E/E81E | verified_diagnostic_routine_configuration_and_readback | L640 | 2E E8 1E | DATA... | 13 | 6E E8 1E | 3 | 05/06 | — | — | — | — | — | — |
| 2E/E81F | verified_diagnostic_snapshot_storage_readback | L640 | 2E E8 1F | DATA... | 67 | 6E E8 1F | 3 | 05/06 | — | — | — | — | — | — |
| 2E/F190 | accepted_pending_identifier_staging_readback_CAN_OBD_overlap | L640 | 2E F1 90 | DATA... | 24 | 7F 2E 78 (pending/deferred) | 3 | 05/06 | — | — | — | — | — | — |
