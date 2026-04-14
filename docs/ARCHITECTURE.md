# Architecture Documentation

## Overview
This Planner-Executor implements Manufacturing Traceability for Kanban for Manufacturing use cases.

## Components
1. **Line Intake**: Collect, validate and normalize quality records from MES; attach a runId and timestamp for traceability.
2. **Planner**: Execute planner phase for the Planner-Executor pattern: persist interim state, enforce guardrails, and emit structured JSON results.
3. **Executor**: Execute executor phase for the Planner-Executor pattern: persist interim state, enforce guardrails, and emit structured JSON results.
4. **Defect Detection**: Defect Detection across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
5. **Traceability**: Traceability across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
6. **In-Process Check**: In-Process Check across joined datasets; branch on thresholds using decision gates; write metrics (success/error counts) for observability.
7. **Production Report**: Assemble final payload with status, artifacts, KPIs and audit trail; store to QMS; return response JSON for the client.

## Data Flow
- Input: Line Intake
- Processing: 7 sequential steps
- Output: Production Report
