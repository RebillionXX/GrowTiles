# Lock tile extra data

Values:
- unsigned byte -> **lock flags**
- unsigned int -> world owner userid
- unsigned int -> count of people with access
- **access_data** - data of people with access 
- unsigned int - negative of world's beats per minute(BPM) (for world locks)

Content of **lock flags**
- 0x10 - FLAGS_MUSIC_NOTES_DISABLE
- 0x20 - FLAGS_MUSIC_NOTES_INVISIBLE
- 0x80 - FLAGS_RAINBOW_TRAIL (for Royal Lock) | FLAGS_ONLY_BUILDING (for Builder's Lock)

**access_data** structure
- unsigned int -> userid of people with access
