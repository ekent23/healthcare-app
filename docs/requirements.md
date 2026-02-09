# Function Requirements

## User Stories

### User Story 1: Estimate Healthcare Costs
##### As a patient I want to enter my location, insurance status, and a medical service or prescription so that I can see an estimated out-of-pocket cost before receiving care.

### Acceptance Criteria:

- *User can input location, insurance type, and service or medication*  
- *System returns a cost estimate within 5 seconds*
- *Estimate includes a short explanation of how the cost was calculated*


### User Story 2: Compare Options
##### As a patient I want to compare multiple providers or medication options so that I can choose the most affordable option.

### Acceptance Criteria:

- *System displays at least two comparable options when available*  
- *Results are sorted by estimated out-of-pocket cost*
- *Lowest-cost option is visually highlighted*

### User Story 3: Find the Cheapest Medication Nearby
##### As a patient I want to enter the name of a medication and my location so that I can find the cheapest place to buy it near me.



### Acceptance Criteria:
 - *User can enter a medication name (brand or generic)*

- *User can enter or auto-detect their location*

- *System returns a list of nearby pharmacies or providers*

- *Results include estimated out-of-pocket prices*

- *Options are sorted from lowest to highest cost*

- *The cheapest option is clearly highlighted*


## Non-Functional Requirements

### Performance

- Cost estimates must be generated within 5 seconds for 95% of requests

- The system must support at least 50 concurrent users

### Security & Privacy
- No personal health information is stored permanently

- All AI processing occurs locally using Ollama


### Usability
- Interface must be usable by non-technical users


## AI-Specific Requirements
- AI must normalize user input (e.g., synonyms for services or drugs)
- AI must generate human-readable explanations for estimates

## Prioritization

### Must Have

- Cost estimation for services or prescriptions

- Local AI processing via Ollama

- Basic comparison of options

### Should Have

- Cost ranges when AI isn't sure about exact price 

- Simple UI feedback for missing information

### Nice to Have

- Historical cost trends

- Provider quality indicators
