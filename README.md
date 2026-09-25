# 🚗 Automotive Sales & Inventory AI Assistant (Langflow + Astra DB)

Sistem Asisten AI berbasis **RAG (Retrieval-Augmented Generation)** yang dirancang menggunakan **Langflow** dan **Astra DB Vector Store**. Sistem ini bertindak sebagai *Automotive Consultant* cerdas yang mampu memberikan informasi stok kendaraan, spesifikasi unit, harga OTR, hingga simulasi kredit secara *real-time* berdasarkan dokumen katalog resmi.

---

## 🌟 Fitur Utama
- **Real-time Vector Search**: Membaca dan mencari data relevan dari dokumen PDF katalog resmi menggunakan Astra DB Vector Database.
- **Automated Document Processing**: Memecah (*chunking*) dan mengubah teks katalog menjadi *embeddings* secara otomatis.
- **Structured Financial & Spec Response**: Memberikan jawaban terstruktur mencakup spesifikasi unit, harga OTR, dan estimasi simulasi kredit (DP/tenor).
- **Anti-Hallucination Guardrails**: Dilengkapi instruksi prompt ketat untuk memastikan AI hanya menjawab berdasarkan data katalog resmi.

---

## 📐 Arsitektur Sistem (Langflow Workflow)
Sistem ini dibangun dengan dua alur (*flow*) utama:
1. **Ingestion Pipeline**: `Read File (PDF)` ➔ `Text Splitter` ➔ `Gemini Embeddings` ➔ `Astra DB Ingestion`.
2. **Retrieval & Generation Pipeline**: `Chat Input` ➔ `Astra DB Search Query` ➔ `Parser (Stringify)` ➔ `Prompt Template` ➔ `Gemini 1.5 Flash` ➔ `Chat Output`.

![Langflow Architecture]
https://github.com/rizkytyofakhri9/Automotive-AI-Sales-Assistant-Langflow/blob/main/assets/Architecture.png)

---

## 📸 Demo & Hasil (Playground)
![Playground Demo]
(https://github.com/rizkytyofakhri9/Automotive-AI-Sales-Assistant-Langflow/blob/main/assets/playground1.png
https://github.com/rizkytyofakhri9/Automotive-AI-Sales-Assistant-Langflow/blob/main/assets/playground2.png
https://github.com/rizkytyofakhri9/Automotive-AI-Sales-Assistant-Langflow/blob/main/assets/playground3.png))

---

## 🚀 Cara Import Flow ke Langflow Anda
1. Clone repositori ini:
   ```bash
   git clone [https://github.com/USERNAME_ANDA/Automotive-AI-Sales-Assistant-Langflow.git](https://github.com/USERNAME_ANDA/Automotive-AI-Sales-Assistant-Langflow.git)
