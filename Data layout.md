# Data layout
## Persistent storage
`status` - `0` means uninit (cannot be observer in the wild), `1` means no scheduled messages, `2` means there are schedule messages.
`uniq_bits` - just random number, we vary it to get different addresses
```
status(ui8), seqno(ui32), pubkey(ui256), uniq_bits(ui16), next_call_time(ui32), dict(time->messages)
```
