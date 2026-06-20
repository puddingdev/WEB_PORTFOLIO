Featured Project: SOUL CHESS (Chess Battle)

Genre: Strategic Turn-Based PvP / Real-Time Multiplayer Board Game

Platform: PC / Web Content

Core Technology: Next.js 15, TypeScript, Supabase (Real-Time Database Integration)

Live Demo Link: soul-chess-alpha.vercel.app

GitHub Repo: github.com/puddingdev/soul-chess.git (Private Repository)

💡 Concept Overview

การคิดและดัดแปลงสถาปัตยกรรมกระดานหมากรุกคลาสสิก ให้กลายเป็นเกมวางแผน PvP บนสมรภูมิที่มีความลึกและใช้กลยุทธ์สูงขึ้น โดยนำระบบสิทธิพิเศษของหมากแต่ละคลาส, ธาตุประจำยูนิต, และระบบการสะสมสถานะผิดปกติมาผสมผสานในสเกลแผนที่ขนาดใหญ่เพื่อสร้าง Dynamic Combat

⚙️ Core System Design Specifications

1. Board & Unit Architecture (สถาปัตยกรรมกระดานและยูนิต)

Board Grid Size: ออกแบบตารางพื้นที่ขนาดใหญ่พิเศษ $14 \times 14$ ช่อง เพื่อรองรับการควบคุมพื้นที่ในวงกว้าง (Area Control) และการวางกับดักแบบเรียลไทม์

Unit Configuration: ยูนิตแบ่งเป็นฝั่งละ $16$ ตัว โดยประกอบด้วย 8 Distinct Unit Classes (8 ประเภทหมาก) ที่มีพฤติกรรมเฉพาะตัว:

แต่ละยูนิตมีระยะการเดิน (Movement Range) และระยะโจมตี (Attack Range) ที่คำนวณผ่านพิกัดพจน์แกนสลับ $(X, Y)$ บนกระดานอย่างเป็นเอกลักษณ์

มีระบบ Role-Based คอยคุมสถานะของยูนิต เช่น ยูนิตแนวหน้ารับหน้าที่เป็น Tank ยูนิตดาเมจเป็น DPS และยูนิตสายก่อกวนหรือบล็อกทางเป็น Control

2. Spell Logic & Elemental Interactions (ระบบธาตุและสกิล)

7-Element Matrix: ออกแบบระบบคำนวณดาเมจแบบคูณพลังธาตุที่แตกต่างกันถึง $7$ ชนิด เพื่อให้เกิดทิศทางกลยุทธ์ที่ลื่นไหล (Fluid Meta-Gameplay)

Persistent Status Afflictions (สถานะผิดปกติ):

Freeze (แช่แข็ง): ห้ามเคลื่อนที่และตัดสิทธิ์ Action Phase ของยูนิตที่โดน

Burn (ไฟไหม้): ได้รับความเสียหายสะสมต่อเนื่องตามเวลาในตอนสิ้นสุดของแต่ละ Turn Phase

Active Field Mechanics: ออกแบบให้ยูนิตสามารถปรับปรุงสภาพสิ่งแวดล้อมรอบตัว (Field Modification) และส่งผลกับยูนิตอื่น ๆ ที่เดินเข้ามาเหยียบได้โดยตรง

3. Turn Engine & Victory Validation (การควบคุมรอบและการตัดสินผล)

Action Points Loop: ควบคุมวงจรจังหวะเล่น (Active Turn Loop) รวมถึงกำหนดขีดจำกัดพลังงานและกฎการสลับฝั่งโจมตี

Automated Win Condition Verification: ระบบตรวจสอบเงื่อนไขแพ้ชนะอัตโนมัติที่คำนวณผลลัพธ์ผ่าน 3 ปัจจัย:

ค่าพลังชีวิตโดยรวมของหมากสำคัญ ($HP = 0$)

คะแนนรวมในการสะสมเป้าหมาย (Point-based Metric)

ฟังก์ชันตรวจการกดยอมจำนน (Surrender Mechanism API)

4. Supabase Network Synchronization (สถาปัตยกรรมมัลติเพลเยอร์)

ออกแบบ API Routing และโครงสร้างฐานข้อมูลที่มีความหน่วงต่ำ (Low Latency) เพื่อประมวลผลการเดินหมาก การกดใช้สกิล และการประสานสถานะ (State Sync) แบบเรียลไทม์ผ่าน Supabase Channel