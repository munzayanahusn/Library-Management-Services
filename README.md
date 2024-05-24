# Library-Management-Services
Kontributor: Husnia Munzayana
## Penjelasan Singkat Program
Library Management Services adalah sebuah sistem manajemen perpustakaan yang terdiri dari beberapa microservices, yaitu `author-service` dan `book-service`. Sistem ini memungkinkan pengguna untuk mengelola data buku dan penulis, serta melakukan operasi CRUD (Create, Read, Update, Delete) pada data tersebut.

## Sub-module services
   a. Book Service : ```https://github.com/munzayanahusn/Library-Management-Service-book-service.git```<br>
   b. Author Service : ```https://github.com/munzayanahusn/Library-Management-Service-author-service.git```<br>

## Cara Setup
1. Clone repository ini<br>
   ```bash
   git clone https://github.com/munzayanahusn/Library-Management-Services.git
   cd Library-Management-Services
   ```
   
2. Install dependencies untuk semua service<br>
  ```bash
    cd author-service
    npm install
  ```
  ```bash
    cd book-service
    npm install
  ```

3. Buat file .env yang berisi:<br>
  ```bash
    POSTGRES_HOST=localhost
    POSTGRES_PORT=5432
    POSTGRES_USER=postgres
    POSTGRES_PASSWORD=yourpassword
    POSTGRES_DB=library_management_service
    MONGODB_URI=mongodb://localhost:27017/library_logs
  ```

## Cara Menjalankan Program
### Melalui Docker
1. Setup Database PostgreSQL dan MongoDB
2. Pastikan Docker sudah terinstall
3. Buka terminal dan arahkan pada tempat clone
4. Jalankan perintah berikut untuk menjalankan container Docker:<br>
  ```bash
  docker-compose up --build
  ```
5. Akses Swagger website melalui browser dengan URL:<br>
   a. Book Service : ```http://localhost:3001/api```<br>
   b. Author Service : ```http://localhost:3002/api```

### Melalui Terminal
1. Setup Database PostgreSQL dan MongoDB
2. Buka terminal dan arahkan pada tempat clone
3. Jalankan setiap service:<br>
   a. Book Service<br>
   ```bash
   cd book-service
   npm run start:dev
   ```
   b. Author Service<br>
   ```bash
   cd author-service
   npm run start:dev
   ```
4. Akses Swagger website melalui browser dengan URL:<br>
   a. Book Service : ```http://localhost:3001/api```<br>
   b. Author Service : ```http://localhost:3002/api```
