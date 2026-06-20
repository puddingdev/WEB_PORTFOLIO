Project: MAGICIAN (Magic Warfare Fantasy)

Genre: Fast-Paced FPS + Action RPG + Competitive Multiplayer

Platform: PC / Console

Role: Game Systems & UX Designer (Group Project)

Project Folder in Drive: Game Design Portfolio/MAGICIAN

💡 Concept Overview

เกมแอ็กชันยิงเวทมนตร์มุมมองบุคคลที่หนึ่ง ที่ผู้เล่นจะได้รับบทเป็นจอมเวท โดยจุดเด่นอยู่ที่ การผสมผสานธาตุประจำเวทมนตร์เพื่อสร้างความหลากหลายให้กับการต่อสู้ ตัวเกมถูกดีไซน์มาเพื่อรองรับทั้งโหมด Co-op ฝ่ามอนสเตอร์สู้บอสยักษ์ (PvE) และโหมดไต่อันดับยึดพื้นที่แข่งกันแบบทีม (PvP) ที่รวดเร็วฉับไว

⚙️ Core System Design Specifications

1. Spell Combination System (ระบบผสมเวทมนตร์ธาตุ)

ผู้เล่นสามารถเลือกร่ายเวทหลักจาก 5 ธาตุหลัก ได้แก่ ไฟ (Fire), น้ำ (Water), ดิน (Earth), ลม (Wind) และ ความมืด (Dark)

Rock-Paper-Scissors Interaction: ดำเนินการจัดทำผังแพ้-ชนะทางแบบเป่ายิ้งฉุบระหว่างธาตุเพื่อเป็นแนวทางกลยุทธ์หลักในการต่อสู้

Dynamic Combo Cast: สกิลสามารถสวมทับผสมกันเพื่อแสดงผลแอนิเมชันและการแสดงผลความเสียหายคอมโบพิเศษ เช่น การผสมเวทมนตร์ลมคู่กับไฟเพื่อจุดระเบิดพายุไฟ (Fire Whirl / Inferno Burst)

2. High-Mobility Combat Loop (วงจรรอบการต่อสู้ความเร็วสูง)

Movement Subsystem: ออกแบบโครงสร้างระบบเคลื่อนที่ซึ่งช่วยสร้างจังหวะเกมเพลย์แบบ Dynamic Combat:

Dash Mechanics: การเคลื่อนหลบระยะสั้นด้วยอัตราเร่งความเร็วสูง

Air Movement & Blink Steps: ออกแบบระบบกระโดดกลางอากาศเพื่อช่วยเปลี่ยนแกนโจมตี

Mana Economy Management: ออกแบบระบบทรัพยากรการจ่ายมานา (Mana Cost) โดยปรับสมดุลให้อิงตามประเภทของสกิล ป้องกันการรัวกดสกิลที่แรงเกินไป และบังคับให้คิดแผนล่วงหน้า

3. Progression & Economy Loop (ระบบเก็บของและการพัฒนาตัวละคร)

Ability Trees & Upgrade Paths: ออกแบบผังสาขาสกิล (Skill Path) และสมุดเวทมนตร์ให้เกิดการต่อยอดทักษะ

Inventory & Itemization: ออกแบบระบบอินเทอร์เฟซสวมใส่อุปกรณ์เสริมพลัง เช่น เครื่องรางที่ส่งเสริมความแรงของการคาสต์ธาตุที่กำหนด

4. User Experience & Persona Solutions (การออกแบบและแก้ Pain Points)

จากพฤติกรรมผู้เล่น (Player Persona) ได้ออกแบบตรรกะระบบควบคุมสภาพแวดล้อมดังนี้:

Matchmaking Engine Concept: ปรับสมดุลระบบสุ่มห้องโดยอ้างอิงสถิติการเล่นของแต่ละคน ป้องกันปัญหาช่องว่างฝีมือ

Toxic Behavior Prevention: ระบบเกียรติยศ (Honor System) เพื่อลดพฤติกรรมเกรียน และส่งเสริมการเล่นร่วมกันแบบทีเวิร์กในโหมด Objective-based (ยึดจุดควบคุมพื้นที่ 3v3 / 5v5)