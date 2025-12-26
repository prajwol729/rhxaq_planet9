# Event Registration System

## 📋 Overview
A simple event registration system that manages user registrations for events. The system enforces key business rules at the database level to ensure data integrity.

## 🎯 What the System Does
- Allows users to register for events
- Tracks event capacity and registrations
- Enforces business rules to prevent invalid data
- Provides a state-based workflow for registration status

## ⚡ Enforced Business Rule
**Primary Rule: Prevent Duplicate Registrations**

A user cannot register for the same event more than once.

**Implementation:**
```sql
ALTER TABLE registrations ADD CONSTRAINT unique_user_event 
UNIQUE (user_id, event_id);