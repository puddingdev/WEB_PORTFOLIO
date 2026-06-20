# CLAUDE.md — Portfolio (Pudding / Arnon Phansuwan)

## Project Overview

Portfolio website ของ Arnon Phansuwan (Pudding) สำหรับสมัครงาน AI Game Designer Junior/Intern

ปัจจุบันเป็น **single-file static HTML prototype** (`prototype.html`) ที่รันได้เลยโดยไม่ต้องมี build step

## File Structure

```
web_Portfolio/
├── prototype.html     ← ไฟล์หลัก (HTML + CSS + JS ทั้งหมดอยู่ในนี้)
├── imageME2.png       ← รูปโปรไฟล์ (PNG, bg removed)
├── CLAUDE.md          ← ไฟล์นี้
├── README.md
└── linkต่างๆ.txt     ← รวม links อ้างอิงทั้งหมด
```

## Tech Stack

- **Vanilla HTML / CSS / JavaScript** — ไม่มี framework, ไม่มี build step
- Deploy ได้โดยตรงบน Vercel (static)

## Sections & Content

| Section | รายละเอียด |
|---------|-----------|
| Hero | ชื่อ, badge, tagline, ปุ่ม GitHub / Drive / Email, รูปโปรไฟล์ |
| About | Who I Am (bio), Tech Stack (skills grouped), Achievements |
| Projects | Filter tabs + Cards grid + Modal detail |
| Contact | Links footer (dark purple gradient) |

## Project Data (JavaScript)

ข้อมูลโปรเจคทั้งหมดอยู่ใน `<script>` ท้ายไฟล์ ในตัวแปร `projects` object:

```js
const projects = {
  'soul-chess': { ... },
  'cursed':     { ... },
  'magician':   { ... },
  'papalaxy':   { ... },
  'pos-pud':    { ... },
  'scoop-loki': { ... },
  'cafe-pos':   { ... }
}
```

**เพิ่มโปรเจคใหม่:** เพิ่ม entry ใน `projects` object + เพิ่ม card HTML ใน `#projects` section

## Filter Categories (data-cat)

| cat value | Tab ที่โชว์ |
|-----------|------------|
| `game-logic` | Game Design & Logic |
| `fullstack` | Full-Stack Web |
| `saas` | SaaS / Tools |
| `wip` | (ปรากฏใน All เท่านั้น ตอนนี้) |

Card หนึ่งใบมีได้หลาย cat เช่น `data-cat="game-logic fullstack wip"`

## Color Palette (Soft Purple Theme)

```css
--purple:       #7C3AED   /* primary */
--purple-mid:   #9333EA
--purple-light: #EDE9FE   /* borders, chip bg */
--purple-pale:  #F5F3FF   /* page bg, section bg */
--purple-dark:  #5B21B6   /* hover, footer */
--purple-muted: #C4B5FD   /* chip borders */
```

## Links (จาก linkต่างๆ.txt)

| ตัวแปร JS | URL |
|-----------|-----|
| `DRIVE_MAIN` | Google Drive (Portfolio หลัก) |
| `DRIVE_CHESS` | Soul Chess Drive |
| `DRIVE_CURSED` | Cursed Project Drive |
| `DRIVE_MAGIC` | Magician Drive |
| `DRIVE_BOARD` | Board Game Design Drive |
| `TABLETOPIA` | Papalaxy on Tabletopia |

## Owner Info

- **Name:** Arnon Phansuwan (Pudding)
- **Email:** anonpansuwanxxx@gmail.com
- **GitHub:** github.com/puddingdev
- **Role targeting:** AI Game Designer Junior / Intern
