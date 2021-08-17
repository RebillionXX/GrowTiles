### Tile data description

- ushort - foreground item id
- ushort - background item id
- ushort - parent block index used for lock, fish tank port etc...
- ushort - tile flags

Content of tile flags
- 0x0001 - FLAGS_TILEEXTRA
- 0x0020 - FLAGS_FLIPPED
- 0x0040 - FLAGS_OPEN
- 0x0080 - FLAGS_PUBLIC
- 0x0200 - FLAGS_SILENCED
- 0x0400 - FLAGS_WATER
- 0x1000 - FLAGS_FIRE
- 0x2000 - FLAGS_RED
- 0x4000 - FLAGS_GREEN
- 0x8000 - FLAGS_BLUE

if **FLAGS_TILEEXTRA** bit is on there'll be 1 additional byte which is **extra tile type** this data might be followed by **extra tile data**

you can read more information about [extra tile data](extra_tile_data/README.md).
