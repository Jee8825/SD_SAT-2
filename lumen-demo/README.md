# Lumen — Round 2 demo

A simple, dependency-free learning management system demo, scoped to the supplied Round 2 question.

## Run locally

From this directory:

```sh
python3 -m http.server 4173 --bind 127.0.0.1 --directory dist
```

Open http://127.0.0.1:4173. The site also works as a static deployment.

## Demonstration

1. Search or filter courses and select **View course**.
2. Review the syllabus and **Enroll in course**.
3. Try **Simulate decline** to demonstrate a failed payment, then **Simulate payment** to activate access. No real money or card details are involved.
4. Read lessons and mark them complete.
5. Open the course assignment and submit a written answer.
6. Select **My learning** to see completion percentages and assignment status.
7. Select **Round 2 API design** for methods/URIs, enrollment request and response, status codes, the student sequence, assignment API, and live simulated request/response history.

## Boundaries

- This is a frontend demo, not a production LMS or an HTTP API server. API calls are simulated centrally in `dist/app.js`.
- Fixed demo student: `stu_001`. Courses and lesson readings are sample content.
- Enrollment, progress, and assignment answers are saved in browser localStorage on this device. They do not sync to a database or other devices. Clear the site's browser storage to start over.
- Payment is simulated. Course content stays locked until a simulated successful payment. No authentication, real payment processing, file uploads, or grading is implemented.
- Progress is completed lessons divided by four. Assignment status is recorded separately.
- Production authentication, database uniqueness, and payment-provider verification are described in the API design tab but are not implemented.

## Files

- `dist/index.html` — page structure
- `dist/styles.css` — responsive styling
- `dist/app.js` — sample data, simulated API, and interactions

Round 2 tasks are all covered by the API design tab and functional student flow. No Round 1 material is included.
