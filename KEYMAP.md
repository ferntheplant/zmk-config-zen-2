# Keylayout

Here is a list of keys I need on my keyboard not in my thumb cluster (reserved for mods + enter + spc/bspc + tab + esc)

|keys|count|included?|
|-|-|-|
|alphas|26|x|
|1234567890|10|x|
|!@#$%^&*()|10|x|
|left down up right|4|x|
|home end|2|x|
|/?|2|x|
|,. <> ;:|6|x|
|-_ [] \&#124 |6|x|
|=+ {}|4|x|
|'" `~ =|4|x|
|F1 through F10|10|x|
|PREV PLAY NEXT|3|x|
|Vol+ Vol-|2 x|
|F11 F12|2| |
|BT0 BT1 BT2 BTC|4|x|
|Fkeys shift|1|x|

total = 96 symbols
3 layers = 90 keys
=> At least 6 symbols must be shifted
But I only shift 4 on base layer meaning 2 symbols must be dropped
TODO: add F11 and F12 just in case!!!

```c
// -----------------------------------------------------------------------------------------
// | Q   | W   | E   | R   | T   |   | Y   | U   | I   | O   | P    |
// | A   | S   | D   | F   | G   |   | H   | J   | K   | L   | ;:   |
// |SFT Z| X   | C   | V   | B   |   | N   | M   | ,<  | .>  |SFT /?|
//             | CMD |L2 ES|CT SP|   |AL EN|L1 TB| BSPC|

// -----------------------------------------------------------------------------------------
// | 1   | 2   | 3   | 4   | 5   |   | 6   | 7   | 8   | 9   | 0   |
// | !   | @   | #   | $   | %   |   | ^   | &   | *   | (   | )   |
// | -   | _   | =   | +   | \   |   | |   | [   | ]   | {   | }   |
//             | CMD |L2 ES|CT SP|   |AL EN| HOLD| BSPC|

// -----------------------------------------------------------------------------------------
// | F1  | F2  | F3  | F4  | F5  |   | F6  | F7  | F8  | F9  | F10 |
// | HOME| END | PREV| PLAY| NEXT|   | LFT | DWN | UP  | RGT | Vol+|
// | SFT | BT0 | BT1 | BT2 | BT_C|   | '   | "   | `   | ~   | Vol-|
//             | CMD | HOLD|CT SP|   |AL EN|L1 TB| BSPC|
```