# Keymap

## Alpha Layout

I am not switching from QWERTY so I am comfortable using different keyboards for gaming and at others' desks.

I'd also prefer to keep symbols nearby their default row-staggered QWERTY locations.

## Thumb cluster logic
 
- Can't have `CMD` on mod-tap key since I need to tap it for windows and hold for mac
- Can't have `BSPC` be mod-tap since I hold it to delete multiple chars
- `CTRL` used frequently in terminals/windows so put it in thumb cluster mod tap
- `ALT` used frequently with Zellij so put it in thumb cluster mod tap
- `TAB` used frequently so put it in thumb cluster
- `SPACE` used *most* freuqnetly so put it on *main* thumb key
- `ESC` used frequently with vim so put it in thumb cluster
- `SHFT` used frequently so put it in thumb cluster

## Main matrix logic

Here is a list of symbols I need on my keyboard

|symbols|count|included?|
|-|-|-|
|ctrl alt cmd shft|4|x|
|spc esc tab|3|x|
|bspc entr|2|x|
|alphas|26|x|
|1234567890|10|x|
|!@#$%^&*()|10|x|
|left down up right|4|x|
|home end pgup pgdn|4|x|
|/?|2|x|
|<>|2| |
|,. ;:|4|x|
|-_ [] \ &#124; |6|x| <--! funny ampersand is pipe | -->
|=+ {}|4|x|
|'" `~|4|x|

|rare symbols|count|included?|
|-|-|-|
|F1 through F10|10|x|
|PREV PLAY NEXT|3|x|
|Vol+ Vol- Mute|3|x|
|F11 F12|2|x|
|BT0 BT1 BT2 BT3 BTC|5|x|

|bonus symbols|count|included?|
|-|-|-|
|ins del|2|x|
|caps print|2|x|

total = 108 symbols
total common = 85
total rare = 23
total bonus = 4 (not included in total)

I want to use maximum 3 layers for common symbols. So I have 108 keys across all layers. However in each layer 1 key is used to enter the layer via holding so it's actually 106 keys. Furthermore I want `SHFT`, `CTRL`, `CMD` and `ALT` accessible from all layers so I lose 4 keys from each of the non-base layers for a new total of 98 keys.

Rare symbols will go on a 4th layer on their own. The 23 rare symbols all fit on the core 30 key matrix without touching thumb clusters.

In total (assuming identical thumb clusters on all layers) I have 120 main matrix keys. Assuming a fixed thumb cluster including `CTRL`, `ALT`, `SHFT`, `CMD`, `SPC`, `ESC`, `TAB`, `L1`, and `L2` then I have 101 remaining symbols to put across my 120 keys leaving 19 leftover keys. The 'rare" layer has 7 leftovers leaving 12 leftovers on my primary layers for "bonus symbols".

## Keymap layout in code

```c
// L0 = BASE (base)
// -----------------------------------------------------------------------------------------
// | Q   | W   | E   | R   | T   |   | Y   | U   | I   | O   | P   |
// | A   | S   | D   | F   | G   |   | H   | J   | K   | L   | BSPC|
// | Z   | X   | C   | V   | B   |   | N   | M   | ,   | .   | ENTR|
//             | CMD |L1 ES|CT SP|   | SHFT|L2 TB| ALT |

// L1 = LEFT (symbol)
// -----------------------------------------------------------------------------------------
// | !   | @   | #   | $   | %   |   | ^   | &   | *   | (   | )   |
// | \   | -   | =   | '   | `   |   | ;   | /   | <   | [   | ]   |
// | |   | _   | +   | "   | ~   |   | :   | ?   | >   | {   | }   |
//             | CMD |L1 ES|CT SP|   | SHFT|L2 TB| ALT |

// L2 = RIGHT (nav)
// -----------------------------------------------------------------------------------------
// | 1   | 2   | 3   | 4   | 5   |   | 6   | 7   | 8   | 9   | 0   |
// | CAPS|     |     | INS | DEL |   | LFT | DWN | UP  | RGT |     |
// |PRINT|     |     |     |     |   | HOME| PGDN| PGUP| END |     |
//             | CMD |L1 ES|CT SP|   | SHFT|L2 TB| ALT |

// L3 = BOTH (rare)
// -----------------------------------------------------------------------------------------
// | F1  | F2  | F3  | F4  | F5  |   | BT0 | BT1 | BT2 | BT3 | BTC |
// | F6  | F7  | F8  | F9  | F10 |   | PREV| PLAY| NEXT|     |     |
// | F11 | F12 |     |     |     |   | MUTE| VOL-| VOL+|     |     |
//             | CMD |L1 ES|CT SP|   | SHFT|L2 TB| ALT |
```
