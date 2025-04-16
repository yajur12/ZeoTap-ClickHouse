**ZeoTap ClickHouse Ingestion Tool**
A full-stack MERN-based application enabling seamless, bi-directional data ingestion between ClickHouse databases and flat files (CSV). Built as part of a real-world technical initiative to address modern data movement challenges.

**Project Overview**
This tool simplifies:

Connecting to ClickHouse instances

Exporting ClickHouse data to CSV

Importing CSV files into ClickHouse

Schema browsing and validation

Real-time ingestion preview and status tracking

**Project Structure**

## Project Structure

```text
ZeoTap-ClickHouse/
├── backend/                # Node.js + Express backend
│   ├── src/
│   │   ├── config/         # Configuration files
│   │   ├── controllers/    # API logic
│   │   ├── routes/         # REST API endpoints
│   │   ├── services/       # Business logic layer
│   │   ├── utils/          # Helper utilities
│   │   └── server.js       # Entry point
│   ├── uploads/            # Uploaded CSV files
│   ├── exports/            # Generated export files
│   └── package.json
│
├── frontend/               # React + Next.js frontend
│   ├── src/
│   │   ├── app/            # Next.js application
│   │   ├── components/     # Modular UI components
│   │   └── lib/            # API and utility services
│   └── package.json
│
├── package.json            # Root workspace file
├── start.sh                # Unix startup script
├── start.bat               # Windows startup script
└── .gitignore
```

**Features**
**Connect to any ClickHouse database instance**

Export data from ClickHouse to downloadable CSV
Import CSV into ClickHouse with schema mapping
Preview records before ingestion
Column Selection with schema and data type awareness
Track Progress of ingestion with real-time feedback

**Tech Stack**
**Backend**
**1.**Node.js + Express.js
**2.**ClickHouse Node.js client
**3.**Multer (file upload)
**4.**csv-parser, fast-csv
**5.**TypeScript, Mocha + Chai for testing

**Frontend**
**1.**React.js + Next.js
**2.**TailwindCSS + ShadCN UI
**3.**Axios for HTTP
**4.**Jest + React Testing Library

**Database**
**1.**ClickHouse
**2.**MongoDB (for logs and metadata)

**Performance Considerations**
**1.**Stream-based file read/write for handling large datasets
**2.**Support for configurable delimiters
**3.**Real-time progress logging stored in MongoDB
**4.**Dynamic table creation with validation

**Testing**
**Frontend**
**1.**Form validation
**2.**File uploads
**3.**Preview rendering

**Backend**
**1.**API coverage
**2.**JWT handling
**3.**Fault tolerance (invalid schema, bad input)


**Installation**
**Option 1: Unified Install
git clone https://github.com/yajur12/ZeoTap-ClickHouse.git
cd ZeoTap-ClickHouse
pnpm install:all**

Option 2: Separate Install
bash
Copy
Edit
git clone https://github.com/yajur12/ZeoTap-ClickHouse.git
cd ZeoTap-ClickHouse

cd backend && pnpm install
cd ../frontend && pnpm install
Running the App
Option 1: Auto Start
bash
Copy
Edit
# Unix/Mac
chmod +x start.sh
./start.sh

# Windows
start.bat
Option 2: Manual Start
bash
Copy
Edit
# Backend
cd backend
pnpm dev

# Frontend
cd frontend
pnpm dev
Open your browser at: http://localhost:3000

Usage
Connect to ClickHouse
Enter hostname, username, password

Click "Connect"

Export ClickHouse → CSV
Select tables/columns

Set file name

Click "Export"

Import CSV → ClickHouse
Upload CSV file

Set target table name

Click "Import"

🏗️ Extendability
Modular backend ready for new DB integrations (e.g., PostgreSQL, Snowflake)

Reusable UI components with dynamic rendering

Future additions: scheduling, compression, file format (Parquet, JSON)

