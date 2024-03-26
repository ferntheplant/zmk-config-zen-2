# Keymap

## Alpha Layout

I am not switching from QWERTY so I am comfortable using different keyboards for gaming and at others' desks.

## Thumb cluster logic
 
- Can't have `CMD` on mod-tap key since I need to tap it for windows and hold for mac
- Can't have `BSPC` be mod-tap since I hold it to delete multiple chars
- `CTRL` used frequently in terminals/windows so put it in thumb cluster mod tap
- `ALT` used frequently with Zellij so put it in thumb cluster mod tap
- `TAB` used frequently so put it in thumb cluster
- `SPACE` used *most* freuqnetly so put it on *main* thumb key
- `ESC` used frequently with vim so put it in thumb cluster

Theoretically `ENTER` could go elsewhere and doesn't need to be on thumb

## Main matrix logic

Here is a list of keys I need on my keyboard not in my thumb cluster

|keys|count|included?|
|-|-|-|
|alphas|26|x|
|1234567890|10|x|
|!@#$%^&*()|10|x|
|left down up right|4|x|
|home end|2|x|
|/?|2|x|
|,. <> ;:|6|x|
|-_ [] \ &#124; |6|x|
|=+ {}|4|x|
|'" `~ =|4|x|
|F1 through F10|10|x|
|PREV PLAY NEXT|3|x|
|Vol+ Vol-|2|x|
|F11 F12|2| |
|BT0 BT1 BT2 BTC|4|x|
|Fkeys shift|1|x|

total = 96 symbols

I want to use maximum 3 layers so I have 90 main matrix keys across all layers. This implies at least 6 symbols must be shifted within a layer.

I only shift 4 on base layer (to match default QWERTY) meaning 2 symbols must be dropped

TODO: add F11 and F12 just in case!!!

## Keymap layout in code

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