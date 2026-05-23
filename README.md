# 🌳 TreeKinator — Binary Tree Informatics Recommendation System

TreeKinator adalah aplikasi berbasis **Binary Tree Decision System** yang membantu pengguna menentukan jalur pembelajaran, bahasa pemrograman, framework, dan teknologi terbaik berdasarkan minat di bidang Informatika.

Project ini menggunakan:
- ⚡ FastAPI sebagai Backend API
- 🎨 Vue.js + Vite sebagai Frontend
- 🌲 Binary Tree sebagai Recommendation Logic
- 🔄 REST API Communication
- 🧠 Object-Oriented Programming (OOP)

---

# 📚 Table of Contents
- Features
- Technologies Used
- Project Structure
- Requirements
- Clone Repository
- Backend Installation
- Frontend Installation
- Running Backend
- Running Frontend
- Running Full Project
- API Documentation
- API Endpoints
- How TreeKinator Works
- Example Decision Flow
- Screenshots
- Common Errors
- Future Development
- Developer
- License

---

# 🚀 Features

✅ Binary Tree Recommendation System  
✅ Strict 3-Stage Decision Logic  
✅ 6 Informatics Categories  
✅ FastAPI REST API  
✅ Vue.js Frontend  
✅ JSON-Based Communication  
✅ Swagger Documentation  
✅ OOP-Based Architecture  
✅ Frontend & Backend Separation  
✅ CORS Enabled  

---

# 🌲 Informatics Categories

| ID | Category |
|---|---|
| 1 | Web Development |
| 2 | Mobile Development |
| 3 | Data Science & AI |
| 4 | Game Development |
| 5 | Cyber Security |
| 6 | IoT & Robotics |

---

# 🛠️ Technologies Used

## Backend
| Technology | Function |
|---         |       ---|
| Python     | Main Programming Language |
| FastAPI    | Backend Framework |
| Pydantic   | Data Validation |
| Uvicorn    | ASGI Server |

## Frontend
| Technology | Function |
|---         |       ---|
| Vue.js     | Frontend Framework |
| Vite       | Frontend Build Tool |
| JavaScript | Frontend Logic |

---

# 📂 Project Structure

```bash
TreeKinator/
│
├── .gitignore         # Menyaring file sampah seperti node_modules & __pycache__ (Pusat)
├── README.md          # Dokumentasi panduan proyek ini (Pusat)
│
├── backend/           # Ruang Lingkup Python & FastAPI Core Logic
│   ├── __pycache__/
│   └── main.py        # Menyimpan kelas Node & inisialisasi 6 pohon biner
│
└── frontend/          # Ruang Lingkup Vue.js (User Interface)
    ├── public/
    │   └── favicon.ico
    ├── src/
    │   ├── App.vue    # Komponen utama visualisasi hexagon honeycomb & alur data API
    │   └── main.js
    ├── index.html
    ├── package-lock.json
    ├── package.json
    └── vite.config.js

📋 Requirements
Sebelum menjalankan project ini, pastikan sudah menginstall:
Software   Version
Python     3.10+
Node.js    18+
npm        Latest
Git        Latest

🔎 Check Installed Version
Python
python --version

Node.js
node -v

npm
npm -v


# Clone repositori dari GitHub
git clone [https://github.com/Choco-MilkShake/TreeKinator.git](https://github.com/Choco-MilkShake/TreeKinator.git)

# Masuk ke folder project yang terbentuk
cd TreeKinator

#⚙️ Backend Installation
1. Open Backend Folder
cd backend

2. Create Virtual Environment (Recommended)
Windows
python -m venv venv
venv\Scripts\activate

MacOS / Linux
python3 -m venv venv
source venv/bin/activate

3. Install Backend DependenciesInstall manual:
pip install fastapi uvicorn pydantic

▶️ Running Backend ServerMasih di folder backend, jalankan : 
python -m uvicorn main:app --reload

Jika berhasil, terminal akan menampilkan : 
INFO : Uvicorn running on [http://127.0.0.1:8000](http://127.0.0.1:8000)

🌐 Backend API Documentation
Setelah backend berjalan: 
Swagger UI
[http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)

ReDoc
[http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)

🎨 Frontend Installation
1. Open Frontend FolderBuka terminal baru di folder utama proyek:
cd frontend

2. Install Frontend Dependencies
npm install

Dependencies akan otomatis diinstall berdasarkan file package.json.

▶️ Running Frontend
Masih di folder frontend, jalankan:
npm run dev

Jika berhasil, terminal akan menampilkan:
VITE vX.X.X ready in XXX ms
➜ Local: http://localhost:5173/

Buka browser: http://localhost:5173

🚀 Running Full Project
TreeKinator membutuhkan kedua layanan berjalan bersamaan menggunakan 2 terminal VS Code berbeda:

🖥️ Terminal 1 — Backend
cd backend
python -m uvicorn main:app --reload

🎨 Terminal 2 — Frontend 
cd frontend
npm run dev

📡 API Endpoints
1. Root Endpoint
Request
GET /

Response
{
  "message": "Informatics Forest API is Active! API backend siap melayani frontend Anda."
}

2. Get All Forests
Mengambil semua kategori utama TreeKinator.

Request
GET /api/forests

Response Example
[
  {
    "id": "1",
    "name": "Web Development",
    "root_node_id": "WEB_ROOT"
  },
  {
    "id": "5",
    "name": "Cyber Security",
    "root_node_id": "SEC_ROOT"
  }
]


3. Get Specific Node
Mengambil node tertentu berdasarkan node_id.
Request
GET /api/node/{node_id}

Example
GET /api/node/WEB_ROOT

Response Example
{
  "id": "WEB_ROOT",
  "question": "Fokus ke Visual/Frontend (1) atau Logika/Backend (2)?",
  "is_leaf": false,
  "result": null,
  "frameworks": [],
  "left_id": "W_FE",
  "right_id": "W_BE"
}


🌲 How TreeKinator WorksTreeKinator menerapkan struktur data Strict 3-Stage Binary Tree. Setiap kali pengguna disuguhkan pertanyaan logika, sistem menyediakan tepat dua cabang pilihan (left_id dan right_id).

Pilihan tersebut mengeksplorasi pohon keputusan secara bertahap hingga menyentuh simpul daun (Leaf Node), di mana fungsi penentu is_leaf otomatis mendeteksi keberadaan muatan hasil berupa rekomendasi teknologi murni tanpa interaksi lanjutan.

🧠 Example Decision Flow
Cyber Security (SEC_ROOT)
│
└── Defensive / Pertahanan (S_DEF)
    └── Forensik Data (S_D_FOR)
        └── Data Recovery (R_S8) -> Hasil Akhir: C++ + Custom Recovery Tools

🔥 Example Recommendations
Category                   Recommendation
Frontend                   WebJavaScript + Vue.js / React
Enterprise                 WebTypeScript + Angular / Next.js
Backend AI                 Python + FastAPI / Django
Mobile Cross Platform      Dart + Flutter
Cyber Forensics            Bash/Shell + Volatility
Game System Level          C++ + DirectX / Vulkan
Cyber Security Automation  Python + Scapy / Metasploit
Embedded Bare Metal        C + Arduino / FreeRTOS


🧪 Testing API Using Swagger
Step 1
Open browser : http://127.0.0.1:8000/docs

Step 2
Find endpoint : GET /api/node/{node_id}

Step 3
Click : Try it out

Step 4
Input : WEB_ROOT

Step 5
Click : Execute

🏗️ System Architecture
Frontend (Vue.js - Honeycomb Interface)
                 ↓
      REST API Communication
                 ↓
       Backend (FastAPI Engine)
                 ↓
    Binary Tree Lookup (O(1) Memory Cache)

📸 Screenshots
Frontend
![Frontend](./screenshots/frontend.png)

Swagger API
![Swagger](./screenshots/swagger.png)

🚫 Files Not Uploaded to GitHub
Berkas berikut secara otomatis disaring oleh berkas .gitignore pusat agar tidak mengotori repositori : 
node_modules/    # Dependensi Frontend (Raksasa)
venv/            # Lingkungan Virtual Python
__pycache__/     # Hasil Kompilasi CPython Local

⚠️ Important Notes
CORS Configuration
Saat pengembangan lokal, konfigurasi CORS diatur terbuka : 
allow_origins=["*"]

Untuk tahap produksi di dunia nyata, bagian ini wajib diisi oleh domain asal frontend resmi demi menjaga keamanan pertukaran data.

In-Memory Database
Project ini memetakan seluruh simpul ke memori RAM menggunakan mekanisme caching dictionary instan:
db_nodes = {}

Data diregistrasi secara rekursif saat server pertama kali dijalankan sehingga pencarian data oleh frontend berjalan dalam kompleksitas waktu konstan $O(1)$.

❌ Common Errors
1. Address Already in Use
Gunakan port lain jika port 8000 bertabrakan:B
python -m uvicorn main:app --reload --port 8001

2. npm command not found
Unduh dan pasang Node.js paket installer terlebih dahulu melalui situs resmi: https://nodejs.org

3. Module Not Found
Pastikan untuk mengulang proses penarikan paket dependensi pada direktori yang tepat : 
pip install -r requirements.txt   # Di dalam folder backend
npm install                       # Di dalam folder frontend

📈 Future Development
[ ] Authentication System
[ ] User Session
[ ] Database Integration
[ ] Recommendation History
[ ] Binary Tree Visualization
[ ] Admin Dashboard
[ ] Docker Support
[ ] Cloud Deployment

👨‍💻 Developer
Developed by:
- Pascal Eyota (FrontEnd Designer)
- Farhan Nizam S.A (FrontEnd Designer)
- Daniel Abner (BackEnd & FrontEnd Developer)

📜 License
This project is licensed under the MIT License.