#Initial Service List

##api-gateway-service: - Serves as the single entry point for all client requests.
- Routes requests to the appropriate backend service.
- Handles authentication, authorization, rate limiting, and request validation.
##request-service: - Accepts and manages emergency assistance requests.
- Tracks request status (submitted, assigned, in progress, completed).
- Stores request details, including location, urgency, and resource needs.
##volunteer-service: - Manages volunteer accounts and availability.
- Matches volunteers with assistance requests based on location and skills.
- Updates volunteer assignments and completion status.
##dispatch-service: - Coordinates emergency response and resource allocation.
- Assigns requests to volunteers, shelters, or emergency responders.
- Prioritizes high-urgency requests and sends notifications when assignments are made.
