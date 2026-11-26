# API รายการสินค้า
สถานะ: PROPOSED
รุ่น: v1
เจ้าของข้อเสนอ: Microservice

{
  "data": [
    { "id": "pencil", "name": "ดินสอ", "priceSatang": 1200, "available": true },
    { "id": "ruler", "name": "ไม้บรรทัด", "priceSatang": 2000, "available": false },
    { "id": "eraser", "name": "ยางลบ", "priceSatang": 800, "available": true },
    { "id": "sharpener", "name": "กบเหลาดินสอ", "priceSatang": 1500, "available": false }
  ]
}


คำขอ: GET /api/v1/catalog/products
Request body: ไม่ส่ง
จะตอบกลับ pencil ruler eraser sharpener state code 200

คำขอ GET /api/v1/catalog/products?available=true
Request body: ไม่ส่ง
จะตอบกลับ pencil กับ eraser  state code 200

คำขอ GET /api/v1/catalog/products?available=flase
Request body: ไม่ส่ง
จะตอบกลับ sharpener กับ ruler state code 200

คำขอ GET /api/v1/catalog/products?available=yes
Request body: ไม่ส่ง
จะตอบกลับ กรณีผิดพลาด state code 422 