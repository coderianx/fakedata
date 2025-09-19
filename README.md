# Flint FakeData Generator

🔹 **Flint** is a simple yet powerful package for generating **fake user data** in Go.  
It can easily generate test or seed data in JSON, CSV, or **SQLite3 (modernc.org/sqlite)**.

## ✨ Features
- ✅ Generates realistic fake user data
- ✅ Export to JSON or CSV files
- ✅ Insert directly into SQLite database
- ✅ User fields:
  - `ID`, `Username`, `Email`
  - `Password` (plain) & `HashedPwd` (SHA256)
  - `FullName`, `Phone`, `Address`, `Country`
  - `CreatedAt` (random past date)

## 📦 Installation

```bash
go get github.com/username/flint
```

SQLite support uses `modernc.org/sqlite` (automatically installed).

## 🚀 Usage

### 1. Save as JSON/CSV

```go
package main

import "github.com/username/flint"

func main() {
    // Generate 20 users and save as JSON
    flint.FakeData("users.json", 20, "json")

    // Generate 20 users and save as CSV
    flint.FakeData("users.csv", 20, "csv")
}
```

### 2. Save to SQLite database

```go
package main

import "github.com/username/flint"

func main() {
    // Generate 50 users and insert into SQLite DB
    flint.FakeDataDB("users.db", 50)
}
```

### 3. Example Output (JSON)

```json
[
  {
    "id": 1,
    "username": "ali1_XyZ",
    "email": "ali1@example.com",
    "password": "A7xG9hT2qL",
    "hashed_password": "7d9c7f2...c9e",
    "full_name": "Ali Yılmaz",
    "phone": "+90-555-123-4567",
    "address": "42 Main St",
    "country": "Turkey",
    "created_at": "2022-11-15T13:24:05Z"
  }
]
```

## 🛠 Development

Clone the repo:
```bash
git clone https://github.com/username/flint.git
cd flint
```

Run example:
```bash
go run examples/main.go
```

## 📜 License

MIT License © 2025
