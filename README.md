# API Testing – Petstore Demo

## Giới thiệu
- Test CRUD API Petstore với Postman + Newman
- Data-driven với pets.csv
- CI/CD với GitHub Actions

## Cách chạy local
```bash
npm install -g newman newman-reporter-htmlextra
newman run Petstore_Collection.json \
  -e Petstore-Demo.postman_environment.json \
  -d TestData/pets.csv \
  -r cli,htmlextra \
  --reporter-htmlextra-export Newman_Reports/report.html
