# 9.5Master
Reverse engineering resources for 9.5th gen Honda (2016/2017)


# Mode 0x27 41/42
Master SecurityAccess mode constants for ALL V6 and 2.4L 2016-2017 ECU's (no hybrid)

```
SS = 32-bit seed, big endian
KK = calculated 32-bit key, big-endian
TT = 2.4L = 0x15, V6 = 0x0C
```

```
Tester → ECU: 10 03
ECU → Tester: 50 03 ...

Tester → ECU: 27 41
ECU → Tester: 67 41 SS SS SS SS TT

Tester → ECU: 27 42 KK KK KK KK TT
ECU → Tester: 67 42
```

```C
/* 2.4L, tag 0x15 */
uint32_t key_24(uint32_t s)
{
    uint32_t x = s + 0xAA64D267;
    return (s ^ (x >> 3 | x << 29) ^ (s >> 16) * (s & 0xFFFF)) + 0xF9849207;
}

/* V6, tag 0x0C */
uint32_t key_v6(uint32_t s)
{
    uint32_t x = s + 0x2584E18A;
    return (s ^ (x >> 2 | x << 30) ^ (s >> 16) * (s & 0xFFFF)) + 0xBE463505;
}
```
