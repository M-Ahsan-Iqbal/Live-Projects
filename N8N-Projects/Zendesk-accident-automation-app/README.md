# 🚨 Accident Ticket Automation System (Zendesk + n8n + WhatsApp)

## 📌 Overview
This project automates the **accident report ticket assignment process** inside Zendesk.

Instead of manual ticket assignment, the system automatically:
- Identifies the correct experts based on accident location (city/area)
- Notifies available agents via WhatsApp
- Assigns the ticket when an agent accepts
- Keeps track of agent availability in real-time

This eliminates manual effort and ensures **faster response times for accident handling**.

---

## 🎯 Problem Statement
In traditional workflows, accident-related tickets are:
- Manually assigned to agents
- Often delayed due to unavailability
- Not optimized based on location or expertise
- Poorly tracked for agent workload

This leads to:
- Slow response times
- Incorrect assignments
- Inefficient agent utilization

---

## 💡 Solution
We built a fully automated system that:

- Filters agents based on **city/location of accident**
- Sends WhatsApp notifications to relevant experts
- Allows agents to **accept or reject tickets**
- Automatically assigns ticket to the first accepted agent
- Ensures only **available agents receive notifications**
- Prevents duplicate agent entries in Zendesk using phone number validation
- Frees agents after ticket resolution for future assignments

---

## ⚙️ System Architecture

**Zendesk Sidebar App**
- Fetches accident ticket details
- Sends data to automation workflow

**Automation Layer (n8n workflows)**
- Processes ticket data
- Filters agents based on city
- Manages assignment logic

**Sunshine Conversations API**
- Handles WhatsApp communication with agents
- Sends ticket alerts and updates

**Zendesk Agent Management**
- Stores agent profiles
- Tracks availability status (busy/free)
- Prevents duplicate agents using phone number validation

---

## 🔄 Workflow Process

### 1. Accident Ticket Created
- Ticket is generated in Zendesk
- Sidebar app collects accident details

### 2. Agent Filtering
- System identifies agents based on:
  - City / area
  - Availability status
  - Current workload

### 3. WhatsApp Notification
- Relevant agents receive WhatsApp message via Sunshine Conversations API
- Message includes:
  - Accident details
  - Accept / Reject options

### 4. Assignment Logic
- First agent to accept gets assigned the ticket
- Other agents are notified that the ticket is already taken

### 5. Agent Status Management
- Assigned agent is marked as **busy**
- When ticket is resolved:
  - Agent status is updated back to **free**

---

## 🧠 Key Features

- 🔁 Fully automated ticket assignment
- 📍 Location-based agent routing
- 📲 WhatsApp-based agent communication
- ⚡ Real-time accept/reject handling
- 🧑‍💼 Agent availability tracking
- 🧹 Duplicate agent prevention (phone-based validation)
- 🚫 No manual intervention required

---

## 🛠️ Tech Stack

- Zendesk Apps Framework (ZAF)
- n8n Workflow Automation
- Sunshine Conversations API
- WhatsApp Messaging Integration
- JavaScript (Sidebar App Logic)
- REST APIs

---

## 🚀 Impact

- Reduced manual ticket assignment effort
- Faster emergency response time
- Improved agent utilization efficiency
- Reduced human errors in assignment process
- Fully scalable automation system

---

## 📌 Future Improvements

- AI-based agent selection optimization
- Priority-based ticket routing
- Analytics dashboard for response times
- Multi-region load balancing for agents

---

## 👨‍💻 Author
Built as part of a Zendesk automation system focusing on real-time incident management and intelligent workflow automation.
