# Database Design

Version: 1.0 (MVP)

Status: Planning

---

# Overview

This document defines the database structure for the AI Front Office platform.

The database stores customer information, conversations, appointments, properties, agents, and company data.

The database is designed to support multiple real estate agencies (multi-tenant architecture).

---

# Main Entities

The platform consists of the following core entities:

- Agencies
- Users
- Agents
- Customers
- Leads
- Properties
- Appointments
- Conversations
- Messages
- Knowledge Base
- Notifications

---

# Agencies

Purpose

Stores company information for each client using the platform.

Fields

- id
- company_name
- logo
- primary_color
- website
- email
- phone
- address
- timezone
- office_hours
- created_at
- updated_at

---

# Users

Purpose

Stores login accounts.

Fields

- id
- agency_id
- full_name
- email
- password_hash
- role
- status
- last_login
- created_at

Roles

- Admin
- Manager
- Agent

---

# Agents

Purpose

Stores information about real estate agents.

Fields

- id
- agency_id
- user_id
- full_name
- email
- phone
- specialization
- profile_photo
- status
- created_at

---

# Customers

Purpose

Stores customer information.

Fields

- id
- agency_id
- full_name
- email
- phone
- preferred_contact_method
- created_at

---

# Leads

Purpose

Stores qualified customer inquiries.

Fields

- id
- customer_id
- assigned_agent
- intent
- property_type
- budget
- preferred_location
- bedrooms
- timeline
- financing_method
- lead_score
- status
- notes
- created_at

Lead Status

- New
- Qualified
- Contacted
- Viewing Scheduled
- Negotiating
- Closed Won
- Closed Lost

---

# Properties

Purpose

Stores property listings.

Fields

- id
- agency_id
- title
- description
- property_type
- price
- bedrooms
- bathrooms
- parking_spaces
- location
- size
- availability
- assigned_agent
- images
- created_at

---

# Appointments

Purpose

Stores viewing appointments.

Fields

- id
- customer_id
- property_id
- agent_id
- appointment_date
- appointment_time
- status
- notes
- created_at

Appointment Status

- Scheduled
- Confirmed
- Completed
- Cancelled
- Rescheduled

---

# Conversations

Purpose

Stores every chat session.

Fields

- id
- customer_id
- channel
- started_at
- ended_at
- assigned_agent
- conversation_status

Channels

- Website
- WhatsApp
- Email
- Voice (future)

---

# Messages

Purpose

Stores every message.

Fields

- id
- conversation_id
- sender
- message
- timestamp

Sender

- Customer
- AI
- Agent

---

# Knowledge Base

Purpose

Stores company documents used by AI.

Fields

- id
- agency_id
- title
- category
- source_file
- uploaded_by
- created_at

Categories

- FAQ
- Buying Guide
- Selling Guide
- Rental Guide
- Policy
- Agent Information

---

# Notifications

Purpose

Stores notifications sent to staff.

Fields

- id
- agent_id
- notification_type
- title
- message
- read_status
- created_at

Notification Types

- New Lead
- Viewing Booked
- Customer Waiting
- Follow-up Reminder

---

# Relationships

Agency

↓

Users

↓

Agents

↓

Properties

↓

Customers

↓

Leads

↓

Appointments

↓

Conversations

↓

Messages

---

# Data Retention

The system should:

- Preserve conversation history.
- Keep appointment history.
- Maintain audit logs.
- Allow archived records.

---

# Security

Sensitive information should be:

- Encrypted where appropriate.
- Backed up regularly.
- Accessible only to authorized users.
- Protected using role-based permissions.

---

# Future Tables

The following tables may be added in future versions:

- Voice Calls
- Payments
- Contracts
- Property Documents
- Analytics
- CRM Integrations
- Marketing Campaigns
- AI Training Logs

---

# End of Document
