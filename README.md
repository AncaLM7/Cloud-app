# Cloud App – Documentație proiect

## 🔹 Introducere

Această aplicație web permite gestionarea unei colecții de articole prin operațiuni CRUD (Create, Read, Update, Delete), utilizând MongoDB Atlas pentru stocarea datelor și OpenAI ChatGPT pentru asistență conversațională. Aplicația este construită cu Next.js, TailwindCSS și este publicată în cloud prin AWS EC2.

## 🔹 Descriere problemă (0.25p)

Gestionarea digitală a articolelor poate deveni ineficientă în lipsa unui sistem centralizat. Aplicația vine în sprijinul utilizatorilor oferind o interfață intuitivă de creare, editare și ștergere articole, împreună cu un chatbot integrat pentru clarificări și informații.

## 🔹 Descriere API (0.25p)

Aplicația expune două API-uri principale:

- `/api/records` – Operațiuni CRUD
- `/api/answer` – Interacțiune cu OpenAI ChatGPT

| Metodă HTTP | Rută                  | Funcționalitate          |
|-------------|-----------------------|--------------------------|
| `GET`       | `/api/records`        | Afișează toate articolele |
| `GET`       | `/api/records?id=...` | Afișează un articol       |
| `POST`      | `/api/records`        | Creează un articol       |
| `PUT`       | `/api/records`        | Editează un articol      |
| `DELETE`    | `/api/records?id=...` | Șterge un articol        |
| `POST`      | `/api/answer`         | Trimite întrebări către ChatGPT |

## 🔹 Flux de date (0.25p)

1. Utilizatorul interacționează cu interfața.
2. Request-ul este trimis către API.
3. MongoDB Atlas gestionează datele.
4. Răspunsul este afișat în UI.

## 🔹 Exemple de request / response

###  Creare articol

```http
POST /api/records
Content-Type: application/json

{
  "title": "Exemplu",
  "description": "Acesta este un articol de test."
}
POST /api/answer

{
  "messages": [
    {
      "role": "user",
      "content": "Cine este Albert Einstein?"
    }
  ],
  "type": "user"
}
| Metodă   | Endpoint       | Scop                   |
| -------- | -------------- | ---------------------- |
| `GET`    | `/api/records` | Afișează articolele    |
| `POST`   | `/api/records` | Creează un articol     |
| `PUT`    | `/api/records` | Editează un articol    |
| `DELETE` | `/api/records` | Șterge un articol      |
| `POST`   | `/api/answer`  | Trimite mesaj către AI |
🔹 Autentificare & Autorizare
MongoDB Atlas: prin URI în .env

OpenAI API: prin OPENAI_API_KEY în .env

Referințe
Next.js

TailwindCSS

MongoDB Atlas

OpenAI

Docker

AWS EC2

YouTube (nelistat): https://youtu.be/8TMvkr0dsfk
Git:  https://github.com/AncaLM7/Cloud-app.git
Vercel: 
https://cloud-app-sand.vercel.app/
https://cloud-app-sand.vercel.app/chat
AWS: http://51.21.81.80

