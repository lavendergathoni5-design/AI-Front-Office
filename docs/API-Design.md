# API Design

Version: 1.0 (MVP)

Status: Planning

---

# Overview

This document defines the REST API used by the AI Front Office platform.

The API enables communication between the frontend, backend, AI engine, and database.

All endpoints return JSON responses.

Base URL

/api/v1

---

# Authentication

Protected endpoints require authentication.

Authentication Method

JWT Bearer Token

Authorization Header

Authorization: Bearer <token>

---

# Health Check

GET /health

Purpose

Verify the API is running.

Response

200 OK

{
  "status": "healthy"
}

---

# Chat

POST /chat

Purpose

Send a customer message to the AI.

Request

{
  "conversation_id": "...",
  "message": "I'm looking for a 3-bedroom house."
}

Response

{
  "reply": "...",
  "conversation_id": "...",
  "intent": "buy_property"
}

---

# Conversations

GET /conversations

Returns all conversations.

GET /conversations/{id}

Returns a single conversation.

DELETE /conversations/{id}

Archives a conversation.

---

# Customers

GET /customers

Returns customer list.

GET /customers/{id}

Returns one customer.

POST /customers

Creates a customer.

PATCH /customers/{id}

Updates customer information.

DELETE /customers/{id}

Archives customer.

---

# Leads

GET /leads

Returns all leads.

GET /leads/{id}

Returns lead details.

POST /leads

Creates a lead.

PATCH /leads/{id}

Updates lead.

DELETE /leads/{id}

Archives lead.

---

# Properties

GET /properties

Returns all properties.

GET /properties/{id}

Returns property details.

POST /properties

Adds property.

PATCH /properties/{id}

Updates property.

DELETE /properties/{id}

Archives property.

---

# Search Properties

GET /properties/search

Supported filters

- budget
- location
- bedrooms
- bathrooms
- property_type

Example

GET /properties/search?location=Westlands&budget=15000000

---

# Appointments

GET /appointments

Returns appointments.

GET /appointments/{id}

Returns one appointment.

POST /appointments

Creates appointment.

PATCH /appointments/{id}

Reschedules appointment.

DELETE /appointments/{id}

Cancels appointment.

---

# Agents

GET /agents

Returns agents.

GET /agents/{id}

Returns agent details.

POST /agents

Creates agent.

PATCH /agents/{id}

Updates agent.

DELETE /agents/{id}

Archives agent.

---

# Notifications

GET /notifications

Returns notifications.

PATCH /notifications/{id}/read

Marks notification as read.

---

# Knowledge Base

GET /knowledge

Returns uploaded documents.

POST /knowledge

Uploads document.

PATCH /knowledge/{id}

Updates document.

DELETE /knowledge/{id}

Deletes document.

---

# Dashboard

GET /dashboard

Returns:

- Total Leads
- Active Conversations
- Today's Appointments
- Conversion Metrics

---

# AI Endpoints

POST /ai/qualify

Qualifies a lead.

POST /ai/recommend

Recommends matching properties.

POST /ai/summarize

Summarizes conversation.

POST /ai/escalate

Escalates conversation to human.

---

# Response Format

Success

{
  "success": true,
  "data": {}
}

Error

{
  "success": false,
  "message": "Description of error"
}

---

# HTTP Status Codes

200 OK

201 Created

400 Bad Request

401 Unauthorized

403 Forbidden

404 Not Found

500 Internal Server Error

---

# Versioning

Current Version

v1

Future versions

v2

v3

---

# End of Document
