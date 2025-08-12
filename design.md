
# Design implementation
## OS setup
- Keyboard layout: Norwegian (no dead keys)
- Compose key: AltGr + LeftCtrl

## Base-layer
```
1   2   3   4   5   6   7   8   9   0   ?   \       # Column reference


-   -   -   -   -   -   -   -   -   -   -   -       # Original
-   -   -   -   -   -   -   -   -   -   -   ¨


-   -   -   -   -   -   -   -   -   -   -   -       # New
-   -   -   -   -   -   -   -   -   -   -   ~
```

### Notes
- First row is a reference to make the columns easier to read.
- `-` means that the key is unchanged.
- Permanently removed: ¨


## Shift layer
```
|   1   2   3   4   5   6   7   8   9   0   ?   \       # Reference


-   -   -   -   ¤   -   -   -   -   -   -   -   -       # Original
-   -   -   -   -   -   -   -   -   -   -   -   -
cps -   -   -   -   -   -   -   -   -   -   -   -


-   -   -   -   $   -   -   -   -   -   -   -   -       # New
-   -   -   -   -   -   -   -   -   -   -   -   -
esc -   -   -   -   -   -   -   -   -   -   -   -
```

### Notes
- Permanently removes: ¤


## Programming base layer
```
1   2   3   4   5   6   7   8   9   0   ?   \       # Reference


-   -   -   -   -   -   -   -   -   -   -   -       # Original
-   -   -   -   -   -   -   -   -   -   -   -
-   -   -   -   -   -   -   -   -   ø   æ   -


-   -   -   -   -   -   -   -   -   -   -   -       # New
-   -   -   -   -   -   -   -   -   -   -   -
-   -   -   -   -   -   -   -   -   {   }   -
```
### Notes
- Toggle layer by tapping LeftShift and RightShift at the same time
- TODO: Find a nice remap for å

## Programing shift layer
```
1   2   3   4   5   6   7   8   9   0   ?   \       # Reference


-   -   -   -   -   -   -   -   -   -   -   -       # Original
-   -   -   -   -   -   -   -   -   -   -   -
-   -   -   -   -   -   -   -   -   Ø   Æ   -


-   -   -   -   -   -   -   -   -   -   -   -       # New
-   -   -   -   -   -   -   -   -   -   -   -
-   -   -   -   -   -   -   -   -   [   ]   -
```

### Notes
- TODO: Find a nice remap for Å

## d+f layer
```
1       2       3       4       5       6       7       8       9       0       ?       # Reference

-       -       -       -       -       -       -       -       -       -       -       # Layer
-       -       -       -       -       del     home    insert  end     -       -
shift   ctrl    -       -       -       left    down    up      right   -       -
-       -       -       -       -       -       PgDn    PgUp    -       -       -
```

### Notes
 - The Layer is triggered by taping `d` and `f` at the same time and then holding the keys.
 - The layer can also be triggered if `a` and/or `s` is pressed together with `f`. The `d` can be omitted in this case.

## capslock layer
```
6       7       8       9       0       ?           # Reference


-       -       -       -       -       -           # Layer
-       C-f1    C-f2    C-f3    C-f4    -
-       C-f5    C-f6    C-f7    C-f8    -
-       C-f9    C-f10   C-f11   C-f12   -
```

### Notes
- Capslock behaves normally, unless it is used in conjunction with keys in this layer.


-------------------------------


# Design requirements

## Philosophy
- Keyboard should be backward compatible with the Norwegian layout as much as possible.
- It is better to create new layers than to remap keys.

## Problematic keys
Need to find an easier way to use:
- [x] Programming characters 
    - [x] $
    - [x] { }
    - [x] [ ]
    - [x] ` 
    - [x] ^
    - [x] ~ 
- [x] Edit keys
    - [x] Insert key
    - [x] Delete key
- [x] Navigation keys
    - [x] Home key
    - [x] End key
    - [x] Page Up key
    - [x] Page Down key
    - [x] Arrow keys
    - [x] esc key
- [ ] Media keys
    - [ ] play/pause key 
    - [ ] stop key
    - [ ] previous key
    - [ ] next keyl

## Additional requirements
- [x] ctrl+alt should map to AltGr for certain keys
- [x] It should be possible to access to è, é, ô

## Unicode characters
It would be nice to have easy access to:
- [ ] em-dash (—), en-dash (–)
- [ ] Trademark symbol (™)

# To be considered
- Create a numpad layer on the home row?
- Writing Norwegian in vim might be annoying as that would probably require frequent switching between programming mode and Norwegian mode. Consider solving this problem.

# TODO
- Create a kde widget that displays if the keyboard is in programming mode or not.

<style>
    /* Ensure no automatic line breaks in the code chunks */
    code {
        white-space : pre !important;
    }
</style>