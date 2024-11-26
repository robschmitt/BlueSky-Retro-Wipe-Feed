# BlueSky Retro Wipe Feed

This document details the keywords used to populate the Retro Wipe custom feed on BlueSky.

## Feed URL

https://bsky.app/profile/schmitthot.bsky.social/feed/aaagrynbw4kt6

## The regex

```
\b(commodore|commodore\samiga|atari|zx\s?spectrum|zx-81|trs-80|apple\s?ii|vic-20|c64|tandy|ibm\s?pc|msx|amstrad|crt\smonitor|floppy\sdrive|floppy\sdisk|dot\s?matrix|8-bit|16-bit|retro\s?computing|personal\s?computer|vga|ega|cga|gw-basic|qbasic|quickbasic|commodore\s?basic|atari\s?basic|sinclair\s?basic|msx\s?basic|applesoft\s?basic|bbc\s?basic|ti\s?basic|turbo\s?basic)\b[^-]
```

## Description of the regex

This regex is designed to match words or phrases related to retro computing systems, components, and programming languages. Here's a detailed breakdown of what it matches:

---

### **General Structure**
1. **`\b`**:
   - Ensures the match starts at a word boundary, so it won't match terms that are part of longer words (e.g., `commodore` won't match in `commodores`).
   
2. **Alternatives (Terms Listed)**:
   - Matches any of the specific terms listed, which include:
     - Retro computer systems and brands (e.g., Commodore, ZX Spectrum, Atari).
     - Specific hardware components (e.g., CRT monitor, floppy disk).
     - Retro computing-related terms (e.g., 8-bit, 16-bit, retro computing).
     - Popular BASIC programming language variations (e.g., GW-BASIC, QBasic, Sinclair BASIC).

3. **`\b` at the End**:
   - Ensures the match ends at a word boundary to prevent matching terms as part of larger words.

4. **`[^-]`**:
   - Ensures the match is **not immediately followed by a hyphen**. For example, `ega` in `ega-based` will not match.

---

### **Categories of Terms Matched**

1. **Retro Computers and Systems**:
   - `commodore`, `commodore amiga`
   - `atari`
   - `zx spectrum`, `zx-81`
   - `trs-80`
   - `apple ii`
   - `vic-20`
   - `c64`
   - `tandy`
   - `ibm pc`
   - `msx`, `amstrad`

2. **Hardware Components**:
   - `crt monitor`
   - `floppy drive`, `floppy disk`
   - `dot matrix`
   - `vga`, `ega`, `cga`

3. **Retro Computing Terms**:
   - `8-bit`, `16-bit`
   - `retro computing`
   - `personal computer`

4. **Programming Languages and BASIC Variations**:
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
  - Example: `commodores` or `cgaextension` will not match because of the word boundary `\b`.
