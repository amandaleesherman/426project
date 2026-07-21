# Service Level Objectives

## api-gateway-service

### Latency SLO
The `POST /api/requests` endpoint must respond within 200 ms at the 95th percentile so residents submitting emergency requests are not delayed during critical situations.

### Reliability SLO
At least 99.95% of requests received by the API gateway must be successfully routed to the appropriate backend service. Requests should use at-least-once delivery with idempotency protections to prevent duplicate operations when clients retry after timeouts.

## request-service

### Latency SLO
The `POST /requests` endpoint must respond within 300 ms at the 95th percentile so residents can submit emergency assistance requests quickly during periods of high demand.

### Reliability SLO
At least 99.9% of emergency request submissions must succeed without losing or duplicating a request. Because retries may occur after network failures, request creation should use at-least-once delivery with idempotency protection.

## volunteer-service

### Latency SLO
The `PATCH /volunteers/{id}/availability` endpoint must respond within 500 ms at the 95th percentile so volunteer availability can be updated quickly enough for dispatch decisions.

### Reliability SLO
At least 99.9% of volunteer availability and assignment updates must succeed without losing the latest confirmed volunteer status.

## dispatch-service

### Latency SLO
The `POST /dispatch` endpoint must respond within 1 second at the 95th percentile so urgent assistance requests can be assigned to an available responder or resource without significant delay.

### Reliability SLO
At least 99.99% of dispatch requests must be successfully processed without losing or duplicating an assignment. Dispatch operations should use idempotent processing to prevent duplicate assignments when requests are retried.
