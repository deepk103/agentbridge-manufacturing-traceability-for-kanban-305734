# API Documentation

## Endpoints
### Line Intake
- **Description**: Collect, validate and normalize quality records from MES; attach a runId and timestamp for traceability.
- **Type**: Processing

### Planner
- **Description**: Execute planner phase for the Planner-Executor pattern: persist interim state, enforce guardrails, and emit structured JSON results.
- **Type**: Processing

### Executor
- **Description**: Execute executor phase for the Planner-Executor pattern: persist interim state, enforce guardrails, and emit structured JSON results.
- **Type**: Processing

### Defect Detection
- **Description**: Defect Detection across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### Traceability
- **Description**: Traceability across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### In-Process Check
- **Description**: In-Process Check across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
- **Type**: Processing

### Production Report
- **Description**: Assemble final payload with status, artifacts, KPIs and audit trail; store to QMS; return response JSON for the client.
- **Type**: Processing
