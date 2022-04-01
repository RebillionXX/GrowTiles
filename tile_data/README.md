### Tile data description

- unsigned short -> foreground id
- unsigned short -> background id
- unsigned short -> parent block index used for lock, fish tank port and etc...
- unsigned short -> tile flags
if **TILEFLAGS_LOCKED** bti is on there'll be 1 additional unsigned short
   - unsigned short -> parent block index

Content of tile flags
 - (0x1)    | TILEFLAG_TILEEXTRA = 1 << 0
 - (0x2)    | TILEFLAG_LOCKED = 1 << 1
 - (0x10)   | TILEFLAG_SEED = 1 << 4
 - (0x20)   | TILEFLAG_FLIPPED = 1 << 5
 - (0x40)   | TILEFLAG_OPEN = 1 << 6
 - (0x80)   | TILEFLAG_PUBLIC = 1 << 7
 - (0x200)  | TILEFLAG_SILENCED = 1 << 9
 - (0x400)  | TILEFLAG_WATER = 1 << 10
 - (0x1000) | TILEFLAG_FIRE = 1 << 12
 - (0x2000) | TILEFLAG_RED = 1 << 13
 - (0x4000) | TILEFLAG_BLUE = 1 << 14
 - (0x8000) | TILEFLAG_GREEN = 1 << 15

if **TILEFLAG_TILEEXTRA** bit is on there'll be 1 additional byte which is **extra tile type** this data might be followed by **extra tile data**

you can read more information about [extra tile data](extra_tile_data/README.md).
