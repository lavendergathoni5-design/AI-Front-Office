# User Flows

**Project:** Virexa AI Front Office

---

# Overview

This document defines how users interact with Virexa AI Front Office.

The objective is to ensure every customer interaction is smooth, professional, and results in a meaningful business outcome.

---

# Main Customer Journey

Customer visits website

↓

AI welcomes customer

↓

Customer selects intent

↓

AI collects required information

↓

AI performs requested action

↓

AI confirms completion

↓

AI notifies agent (if required)

↓

Conversation ends

---

# Welcome Flow

Customer opens chat

↓

AI

Hello 👋

Welcome to ABC Realty.

I'm Virexa AI, your virtual assistant.

I can help you:

• Buy a property

• Rent a property

• Sell a property

• Book a viewing

• Answer your questions

How can I help you today?

---

# Intent Flow

The AI should determine which of the following paths the customer wants.

Customer wants to:

- Buy Property
- Rent Property
- Sell Property
- Book Viewing
- Ask Question
- Speak to Human Agent

Each option follows a separate flow.

---

# Buy Property Flow

Customer

"I want to buy a house."

↓

AI

Great!

I'd love to help.

Let's find a property that matches your needs.

↓

Collect:

- Name
- Phone
- Email

↓

Ask:

What type of property?

- Apartment
- House
- Villa
- Land
- Commercial

↓

Ask budget

↓

Ask preferred location

↓

Ask number of bedrooms

↓

Ask timeline

"When are you planning to buy?"

↓

Search property database

↓

Display matching properties

↓

Customer selects property

↓

Offer viewing

↓

Book appointment

↓

Notify agent

↓

Conversation completed

---

# Rent Property Flow

Customer wants to rent

↓

Collect:

- Name
- Phone
- Email

↓

Ask:

Budget

↓

Location

↓

Property type

↓

Bedrooms

↓

Move-in date

↓

Search available rentals

↓

Recommend properties

↓

Offer viewing

↓

Book appointment

↓

Notify property agent

---

# Sell Property Flow

Customer

"I want to sell my house."

↓

Collect:

- Name
- Phone
- Email

↓

Ask:

Property location

↓

Property type

↓

Estimated asking price

↓

Property condition

↓

Schedule valuation meeting

↓

Notify sales team

---

# Book Viewing Flow

Customer

"I want to view Property #203."

↓

Collect:

- Name
- Phone

↓

Ask preferred date

↓

Ask preferred time

↓

Check calendar availability

↓

Confirm appointment

↓

Notify assigned agent

↓

Send confirmation

---

# FAQ Flow

Customer asks:

- Office hours
- Mortgage information
- Parking
- Security
- Payment methods
- Company information

↓

Search knowledge base

↓

Answer accurately

↓

Ask

"Is there anything else I can help you with?"

---

# Human Agent Flow

Customer requests a person

↓

AI

Certainly.

I'll connect you with one of our agents.

↓

Collect:

Name

Phone

Reason

↓

Notify available agent

↓

Conversation paused

---

# Unknown Question Flow

Customer asks something the AI cannot answer.

↓

AI

I want to make sure I give you accurate information.

I'll forward your question to one of our specialists.

↓

Collect contact details

↓

Notify agent

---

# Lead Qualification Flow

The AI should determine:

Budget

↓

Buying timeline

↓

Property type

↓

Preferred location

↓

Financing method

- Cash
- Mortgage
- Not decided

↓

Lead Score

High

Medium

Low

↓

Notify agent

---

# Appointment Flow

Customer requests viewing

↓

Check calendar

↓

Available?

YES

↓

Book

↓

Confirmation

↓

Reminder

↓

Agent notified

If NO

↓

Suggest alternative times

↓

Customer selects another slot

↓

Confirm booking

---

# Conversation End

Before ending every conversation the AI should:

✓ Confirm customer request has been completed.

✓ Ask if additional help is needed.

✓ Thank the customer.

Example:

"Thank you for contacting ABC Realty.

It was a pleasure assisting you today.

If you have more questions, I'm always here to help.

Have a wonderful day!"

---

# Escalation Rules

Immediately transfer to a human agent if:

- Customer requests a human.
- AI is uncertain.
- Customer becomes frustrated.
- Legal advice is requested.
- Financial advice is requested.
- Complaint is received.
- High-value customer requests immediate assistance.

---

# Business Goals Per Conversation

Every conversation should achieve at least one of these outcomes:

- Capture a new lead.
- Book a viewing.
- Answer a question.
- Connect to an agent.
- Schedule a follow-up.
- Collect customer information.

No conversation should end without attempting to provide value.

---

# End of Document
