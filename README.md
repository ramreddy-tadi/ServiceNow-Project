# 🚇 Metro Ticket Generation System — ServiceNow

> A ServiceNow-based Metro Ticket Generation System that provides a user-friendly ticket booking experience through the Service Portal, with dynamic fare calculation, conditional payment fields, and QR-based ticket presentation.

## 🎥 Demo Video

🔗 **Demo** :

---

## 📌 Project Overview

The **Metro Ticket Generation System** is a ServiceNow application designed to provide a simple and interactive metro ticket booking experience.

The application allows users to:

- Select their starting and destination metro stations
- Select the type of journey
- Select the number of passengers
- Automatically calculate the applicable fare
- Select a payment mode
- Enter an additional payment mode when required
- Generate and display a QR-based metro ticket

The project was developed using ServiceNow application development features such as **Custom Tables, Service Catalog, Catalog Variables, Catalog Client Scripts, Catalog UI Policies, Service Portal, and Custom Widgets**.

---

## 🎯 Objectives

- Provide a simple metro ticket booking interface.
- Maintain metro station information using a custom ServiceNow table.
- Capture journey details through a Service Catalog Item.
- Dynamically calculate fares based on journey details.
- Implement conditional field visibility using UI Policies.
- Generate and display a QR-based ticket experience.
- Demonstrate ServiceNow development and configuration concepts through an end-to-end project.

---

## 🏗️ Project Architecture

```text
                    ┌─────────────────────────┐
                    │    ServiceNow Portal    │
                    └────────────┬────────────┘
                                 │
                                 ▼
                    ┌─────────────────────────┐
                    │  Book A Metro Ticket    │
                    │      Catalog Item       │
                    └────────────┬────────────┘
                                 │
                  ┌──────────────┼──────────────┐
                  ▼              ▼              ▼
          ┌─────────────┐ ┌─────────────┐ ┌─────────────┐
          │  Variables  │ │ Client      │ │ UI Policy   │
          │             │ │ Scripts     │ │             │
          └─────────────┘ └─────────────┘ └─────────────┘
                  │              │              │
                  └──────────────┼──────────────┘
                                 ▼
                    ┌─────────────────────────┐
                    │    QR Ticket Widget     │
                    │    Metro QR Widget      │
                    └─────────────────────────┘

                    Backend:
                    Metro Station Details
                           Table
