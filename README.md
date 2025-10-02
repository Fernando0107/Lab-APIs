# Lab: APIs

Build a small Flask application that consumes a free public API and exposes your own endpoints on top of it. You’ll use an N‑tier architecture, apply OOP for the Service and Repository layers, practice robust error handling, and ship something fun.

---

## Learning goals

* Discover and evaluate free/public APIs.
* Design a simple **N‑tier** app with **Flask**.
* Implement **OOP** in Service and Repository layers.
* Practice **error handling** and input validation.
* Expose at least **3 Flask endpoints** that do something fun.
* Write documentation.

---

## Deliverables

1. A working Flask app following the N‑tier software architecture.
2. At least **3 JSON endpoints** (GET/POST as you see fit).
3. OOP implementation for **Service** and **Repository** layers.
4. Proper **error handling** with meaningful responses.
5. A **README** with setup instructions and API docs.

---

## Constraints & Requirements

* **Architecture:** N‑tier (Routes/Controllers → Services → Repositories → External API/Storage).
* **External API:** choose a free/public API (no auth or free-tier auth).
* **Endpoints:** at least 3; at least 2 must call the external API through your layers.
* **OOP:** Service and Repository implemented as classes with clear responsibilities; consider interfaces/abstract base classes when helpful.
* **Error Handling:** no unhandled exceptions bubbling to Flask; return JSON error payloads with appropriate HTTP status codes.

---

## Choosing a free API (ideas)

Pick something playful and simple:

* "Cat facts" / random facts
* Public jokes/quotes
* Open weather (free tier)
* Pokémon info
* Space/astronomy pictures of the day

---

## Endpoint ideas (pick at least 3)

1. `GET /api/v1/random` → returns a decorated random item from the external API.
2. `GET /api/v1/search?q=...` → searches upstream and returns the top 10.
3. `POST /api/v1/transform` → accepts JSON and returns a fun transformation.
4. `GET /api/v1/stats` → returns simple stats (count, last fetch time, cache hits).
5. `POST /api/v1/mashup` → combines user payload with a fresh upstream item.

At least one endpoint must **not** depend on the external API (e.g., `/transform`, `/stats`).

---

## README checklist

* Project description & chosen external API.
* Setup: Python version, virtualenv, `pip install -r requirements.txt`.
* Run: `FLASK_APP=app.py flask run` (or `python app.py`).
* Endpoints with examples (curl + sample responses).
* Notes on error handling and any caching.

---
## Evaluation Criteria (100 pts)

| Criterion                        | Points | Description |
|----------------------------------|--------|-------------|
| Endpoints                        | 30     | At least 3 endpoints are implemented; at least one does not depend on the external API. Endpoints use correct HTTP methods and return proper status codes. |
| Architecture & OOP               | 25     | Clear N-tier architecture (Routes/Controllers → Services → Repositories). Service and Repository layers use classes with well-defined responsibilities. |
| External API integration         | 15     | External API is integrated through the Repository layer, resilient to timeouts or errors. Proper abstraction is applied. |
| Error handling & logging         | 15     | Custom exceptions and error mapping to JSON responses with appropriate status codes. Logs are informative and helpful for debugging. |
| Code quality & documentation     | 15     | Code is clean, readable, and uses typing where appropriate. A `PLEASE-README.md` is provided with clear instructions, examples of usage, and endpoint documentation. |

---

### Git Requirements

- ✅ Use Git from the start of the project.  
- ✅ Commit at **meaningful milestones** (e.g., project setup, external API integration, first endpoint, error handling, final refactor).  
- ✅ Use **meaningful commit messages** that clearly describe what was implemented or changed.  

---

### README and Usability (Required)

A separate `README.md` (not this lab instruction file) must be included. It should:

- Clearly explain what the project does and which external API was chosen.  
- Provide **step-by-step instructions on how to run the application** (Python version, virtualenv, dependencies (`pip install -r requirements.txt`), and commands (Run: `FLASK_APP=app.py flask run` (or `python app.py`)). 
- Document the available endpoints with examples (e.g., curl requests and sample responses).  
- Include notes on error handling, logging, and any optional features (e.g., caching).  

⚠️ **Important:** Do not forget to include instructions on how to run the code. This will be explicitly graded.  

