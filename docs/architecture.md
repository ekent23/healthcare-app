
# System Architecture

## Diagram


**UI → Backend API → AI → Prices → Result**

---

## Component Descriptions

### Frontend (UI)

* Collects user input (location, insurance type, service, or medication)
* Displays estimated costs and comparisons

### Backend API

* Validates and normalizes incoming requests
* Deals with calls between the AI model and data sources
* Returns structured results to the frontend

### AI Layer (Ollama)

* Runs locally on the host machine
* Interprets vague or incomplete user input
* Generates explanations for cost estimates

### Data Source

* Fetches healthcare and prescription pricing from an API

---

## Data Flow

1. The user enters a request in the UI (e.g., medication name and location).
2. The UI sends the request to the backend API.
3. The backend uses the Ollama to interpret and normalize the request.
4. The backend queries the pricing data source using the AI’s output.
5. The backend combines pricing results with an AI-generated explanation.
6. The final response is sent back to the UI and displayed to the user.


## Architecture Decision Records (ADRs)

### ADR 1: Local AI via Ollama

**Decision:** Use Ollama to run the AI model locally.
**Reasoning:** Preserves user privacy, avoids external API costs, and ensures the system works offline.
**Trade-offs:** Limited model size compared to cloud-based solutions.

---

### ADR 2: Not Sure Yet
