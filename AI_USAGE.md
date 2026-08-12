# AI Usage 
เอกสารบันทึกการประยุกต์ใช้ AI ช่วยในการทำแบบฝึกหัด ข้อผิดพลาดของ AI และบทสรุปความรู้ (Self-Reflection)

## 1. จุดที่ใช้ AI ในการพัฒนา (AI Assistance)

* **การสร้าง Custom Tool:** ให้ AI ช่วยวางโครงสร้างฟังก์ชัน concert_budget_planner และเขียน Docstring ตามมาตรฐาน Google ADK เพื่อให้ LLM ทำ Function Calling ได้ถูกต้อง
* **การตั้งค่า Qdrant Vector Client:** ให้ AI ช่วยแนะนำวิธีการสร้างCollection models.VectorParams และการอัปโหลด PointStruct เข้า In-Memory Qdrant
* **การออกแบบ LLM-as-Judge Prompt:** ให้ AI ช่วยร่าง Prompt สำหรับประเมินคำตอบและบังคับให้ส่งกลับมาเป็น JSON Format ({"score": X, "reason": "..."})

---

## 2. Prompts สำคัญที่ใช้ในการทำงาน

Prompt 1 (สร้าง Tool):
"เขียนฟังก์ชัน Python สำหรับคำนวณงบประมาณคอนเสิร์ต 2,500 บาท รองรับค่าบัตร ค่าเดินทาง ค่ากิน ค่าที่พัก และค่าช้อปปิ้ง พร้อมสร้าง Docstring ละเอียดสำหรับใช้กับ Google ADK FunctionTool"

Prompt 2 (LLM-as-Judge):
"สร้าง JSON Prompt สำหรับให้ Gemini ประเมินความถูกต้องของคำตอบจาก RAG โดยให้คะแนน 1-5 พร้อมระบุเหตุผล"
