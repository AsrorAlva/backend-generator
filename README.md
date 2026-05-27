# Backend Generate Exam

Backend service untuk sistem generate exam / ujian otomatis.
Project ini dibuat untuk menangani proses autentikasi, manajemen soal, generate exam, dan pengelolaan data ujian secara terstruktur melalui REST API.

---

## Features

* Authentication & Authorization
* CRUD Questions
* CRUD Exam
* Generate Random Exam
* Question Categories
* User Management
* Exam Result Management
* REST API Architecture
* Validation & Error Handling

---

## Tech Stack

* PHP / Laravel
* MySQL
* REST API
* Docker (Optional)

---

## Installation

Clone repository:

```bash
git clone <repository-url>
```

Masuk ke folder project:

```bash
cd backend-generate-exam
```

Install dependency:

```bash
composer install
```

Copy environment file:

```bash
cp .env.example .env
```

Generate app key:

```bash
php artisan key:generate
```

Setup database di file `.env`

```env
DB_DATABASE=generate_exam
DB_USERNAME=root
DB_PASSWORD=
```

Run migration:

```bash
php artisan migrate
```

Jalankan server:

```bash
php artisan serve
```

---

## API Endpoint Example

### Authentication

| Method | Endpoint        | Description   |
| ------ | --------------- | ------------- |
| POST   | `/api/login`    | Login user    |
| POST   | `/api/register` | Register user |

---

### Questions

| Method | Endpoint              | Description       |
| ------ | --------------------- | ----------------- |
| GET    | `/api/questions`      | Get all questions |
| POST   | `/api/questions`      | Create question   |
| PUT    | `/api/questions/{id}` | Update question   |
| DELETE | `/api/questions/{id}` | Delete question   |

---

### Exams

| Method | Endpoint              | Description                 |
| ------ | --------------------- | --------------------------- |
| GET    | `/api/exams`          | Get all exams               |
| POST   | `/api/exams/generate` | Generate exam automatically |

---

## Project Structure

```bash
app/
├── Http/
├── Models/
├── Services/
├── Repositories/

database/
├── migrations/
├── seeders/

routes/
├── api.php
```

---

## Running With Docker

```bash
docker compose up --build
```

---

## Environment Variables

Example:

```env
APP_NAME=GenerateExam
APP_ENV=local
APP_DEBUG=true

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
```

---


