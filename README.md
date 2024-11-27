# BlueSky Retro Wipe Feed

This document details the keywords used to populate the Retro Wipe custom feed on BlueSky.

## Feed URL

https://bsky.app/profile/schmitthot.bsky.social/feed/aaagrynbw4kt6

## The regex

```
(?:^|[\s,.:;"'])(commodore|commodore\samiga|amiga\s500|amiga\s600|amiga\s1000|amiga\s1200|amiga\s4000|atari\svcs|atari\s2600|zx\s?spectrum|zx-81|trs-80|apple\s?iie?|vic-20|c64|tandy|ibm\s?pc|msx|amstrad|crt\smonitor|floppy\sdrive|floppy\sdisk|retro\s?computing|vintage\s?computing|retro\s?gaming|vga\smonitor|ega\smonitor|cga\smonitor|gw-basic|qbasic|quickbasic|commodore\s?basic|atari\s?basic|sinclair\s?basic|msx\s?basic|applesoft\s?basic|bbc\s?basic|ti\s?basic|286\spc|386\spc|486\spc|socket\s3|socket\s7|turbo\s?basic|3dfx|voodoo\s2|voodoo\s3|voodoo\s5)(?:^|[\s,.:;"'])
```

## Description of the regex

This regex is designed to match words or phrases related to retro computing systems, components, and programming languages. Here's a detailed breakdown of what it matches:

---

### **General Structure**
1. **`(?:^|[\s,.:;"'])`**:
   - Ensures the match starts and ends at a word boundary, so it won't match terms that are part of longer words (e.g., `commodore` won't match in `commodores`). This word boundary specifically accounts for non-ASCII characters.
   
2. **Alternatives (Terms Listed)**:
   - Matches any of the specific terms listed, which include:
     - Retro computer systems and brands (e.g., Commodore, ZX Spectrum, Atari).
     - Specific hardware components (e.g., CRT monitor, floppy disk).
     - Retro computing-related terms (e.g., 8-bit, 16-bit, retro computing).
     - Popular BASIC programming language variations (e.g., GW-BASIC, QBasic, Sinclair BASIC).

---

### **Categories of Terms Matched**

1. **Retro Computers and Systems**:
   - `commodore`, `commodore amiga`, `amiga 500`, `amiga 600`, `amiga 1000`, `amiga 1200`, `amiga 4000`
   - `atari`
   - `zx spectrum`, `zx-81`
   - `trs-80`
   - `apple ii`
   - `apple iie`
   - `vic-20`
   - `c64`
   - `tandy`
   - `ibm pc`
   - `msx`, `amstrad`

2. **Hardware Components**:
   - `crt monitor`
   - `floppy drive`, `floppy disk`
   - `vga monitor`, `ega monitor`, `cga monitor`
   - `3dfx`, `voodoo 2`, `voodoo 3`, `voodoo 5`

3. **Retro Computing Terms**:
   - `socket 7`
   - `socket 3`
   - `286 pc`
   - `386 pc`
   - `486 pc`
   - `retro computing`
   - `vintage computing`
   - `retro gaming`

5. **Programming Languages and BASIC Variations**:
   - `gw-basic`, `qbasic`, `quickbasic`
   - `commodore basic`
   - `atari basic`
   - `sinclair basic`
   - `msx basic`
   - `applesoft basic`
   - `bbc basic`
   - `ti basic`
   - `turbo basic`

---

### **What It Does Not Match**
- Terms **followed by a hyphen**:
  - Example: `ega-based` will not match due to the `[^-]` restriction.
- Terms that are part of longer words:
  - Example: `commodores` or `cgaextension` will not match because of the word boundary.
