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

## Grading rubric (100 pts)

* **Endpoints (30 pts):** ≥3 endpoints; at least one independent of external API; correct HTTP methods and status codes.
* **Architecture & OOP (25 pts):** Clear separation of layers; abstractions; classes well‑designed.
* **External API integration (15 pts):** Repository encapsulates HTTP; resilient to errors/timeouts.
* **Error handling & logging (15 pts):** Custom exceptions, mapped responses, sensible logs.
* **Code quality & docs (15 pts):** Clean code, typing where useful, README clarity.
