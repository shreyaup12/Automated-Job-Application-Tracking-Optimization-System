# AI-Powered Application Tracking System

An end-to-end application tracking and automation system built using **n8n, OpenAI, Gmail APIs, and Notion** to streamline job application management, automate status tracking, and generate intelligent JD–resume insights.

---

# Features

## Application Management
Centralized application tracking in Notion with structured records for:

- Company
- Role
- Job Description (JD)
- Resume
- Application Status

---

## Automated Status Tracking

Automatically updates application stages based on incoming emails:

- Interview emails → `Interview`
- Offer emails → `Offer`
- Rejection emails → `Rejected`

---

## Event-Driven Workflows

### Notion-Triggered Workflow
Runs automatically when a new application entry is added or updated.

### Gmail-Based Tracking Workflow
Continuously monitors emails and updates application status automatically.

### Smart Matching Logic
Matches incoming emails to the correct company/application entry before updating status.

---

## JD & Resume Intelligence

Uses OpenAI to analyze job descriptions and resumes for:

- Skill extraction
- Skill gap detection
- Resume improvement suggestions
- Interview question generation

---

# Tech Stack

| Technology | Purpose |
| n8n | Workflow automation |
| OpenAI API | JD & resume analysis |
| Gmail API | Email parsing & tracking |
| Notion API | Centralized database |
| JavaScript | Workflow logic & matching |

---

# Workflow Architecture

## Workflow 1 — JD & Resume Analysis

Notion Trigger
 → Extract Resume
 → Parse PDF
 → OpenAI Analysis
 → Store Results in Notion


## **Workflow 2 — Email Status Tracking**

 Schedule Trigger
 → Gmail API
 → Status Detection
 → Company Matching
 → Update Notion Status

## ** Status Pipeline**
Applied → Interview → Offer → Rejected
