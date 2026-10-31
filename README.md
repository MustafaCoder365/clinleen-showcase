<div align="center">

# 🦷 ClinLeen — كلين لين

**Multi-tenant SaaS platform for dental clinics: patients, appointments, dental charts, billing, inventory, and labs, in Arabic and English.**

[![Showcase](https://img.shields.io/badge/Showcase-View%20Gallery-0D9488?style=for-the-badge&logo=githubpages&logoColor=white)](https://mustafacoder365.github.io/clinleen-showcase/)
![Status](https://img.shields.io/badge/Status-Launching%20soon-1D4ED8?style=for-the-badge)
![Source](https://img.shields.io/badge/Source-Private-334155?style=for-the-badge&logo=github)

![Next.js](https://img.shields.io/badge/Next.js_14-000000?style=flat-square&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=flat-square&logo=prisma&logoColor=white)
![NextAuth](https://img.shields.io/badge/NextAuth-000000?style=flat-square&logo=auth0&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Zod](https://img.shields.io/badge/Zod-3E67B1?style=flat-square&logo=zod&logoColor=white)
![Vitest](https://img.shields.io/badge/Vitest-6E9F18?style=flat-square&logo=vitest&logoColor=white)

<img src="./screens/hero.jpg" width="100%" alt="ClinLeen dashboard on desktop and phone" />

</div>

> 🔒 **This repository is a showcase.** ClinLeen is a commercial product, so its source code is private. Screens below come from the real app running with demo data.

---

## ✨ What it does

ClinLeen lets any dental clinic subscribe and run its whole practice from one account, fully isolated from every other clinic on the platform.

| | |
|---|---|
| 🏥 **Multi-tenant, multi-branch** | Each clinic is a tenant with strict data isolation; one clinic can run several branches with their own staff, chairs, and schedules |
| 👥 **Roles and permissions** | Platform admin, clinic owner, dentist, and reception, with a granular permission catalog and an audit log |
| 🦷 **Interactive dental chart** | FDI numbering for permanent and primary teeth, per-surface conditions, and a full treatment history for every tooth |
| 📅 **Appointments** | Booking from the dashboard or a public booking page, status flow (pending → confirmed → arrived → with doctor → completed), and conflict prevention per dentist and chair |
| ⏱️ **Waiting room** | Live queue with check-in, call-in, and waiting time |
| 📋 **Complete patient file** | Medical history, visits, treatment plans, prescriptions, consents, cosmetic and laser sessions, lab orders, photos, and billing |
| 💳 **Billing** | Itemized invoices, discounts, installment plans, partial payments, local methods (Cash, Card, ZainCash, Qi Card, FastPay), and voids with reasons |
| 💰 **Cash and expenses** | Daily cash register sessions per branch, expenses by category, and financial reports with CSV export |
| 📦 **Inventory and labs** | Stock with batches and expiry, low-stock and expiry alerts, suppliers, purchase orders, and dental lab orders with delivery tracking |
| 🔔 **Notifications** | Appointment reminders through a provider interface, ready for email, WhatsApp, or SMS |
| 🌍 **Arabic and English** | Full right-to-left and left-to-right layouts, chosen before sign-in |
| 📱 **Installable** | Mobile-first UI that installs as a PWA |

---

## 🖼️ Screens

### Interactive dental chart
<img src="./screens/dental-chart.jpg" width="100%" alt="Dental chart with tooth conditions on desktop and phone" />

### Appointments and waiting room
<img src="./screens/appointments.jpg" width="100%" alt="Appointments list and booking form" />
<img src="./screens/waiting-room.jpg" width="100%" alt="Waiting room queue" />

### Public booking page for patients
<img src="./screens/booking.jpg" width="100%" alt="Public booking page" />

### English interface
<img src="./screens/english.jpg" width="100%" alt="English dashboard" />

<details>
<summary><b>More screens</b></summary>
<br>

| | |
|---|---|
| <img src="./screens/patients.jpg" alt="Patients list" /> Patients | <img src="./screens/patient.jpg" alt="Patient file" /> Patient file |
| <img src="./screens/billing.jpg" alt="Billing" /> Billing | <img src="./screens/reports.jpg" alt="Financial reports" /> Financial reports |
| <img src="./screens/inventory.jpg" alt="Inventory" /> Inventory | <img src="./screens/labs.jpg" alt="Labs" /> Labs |
| <img src="./screens/cash.jpg" alt="Cash register" /> Daily cash register | <img src="./screens/services.jpg" alt="Services" /> Services and pricing |
| <img src="./screens/staff.jpg" alt="Staff" /> Staff | <img src="./screens/login.jpg" alt="Sign in" /> Sign in |

</details>

---

## 🏗️ Architecture

```
Next.js 14 (App Router, Server Actions)
├── NextAuth (credentials, role-based sessions)
├── Middleware: locale routing + auth guard
├── Server actions validated with Zod
│     └── every query scoped by clinicId (tenant isolation)
├── Prisma ORM ──► PostgreSQL (47 models, 7 migration phases)
└── PWA: manifest + service worker
```

**Built in phases:** permissions, branches, and audit → medical history, visits, and media → services, treatment plans, prescriptions, and consents → appointment states and conflict prevention → invoicing, installments, expenses, and cash → inventory and labs → notifications.

---

## 👤 Author

**Mustafa Shakir** — Frontend Software Developer, Baghdad

[![GitHub](https://img.shields.io/badge/GitHub-MustafaCoder365-181717?style=flat-square&logo=github)](https://github.com/MustafaCoder365)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Mustafa%20Shakir-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/mustafa-shakir-840374330)
[![Email](https://img.shields.io/badge/Email-Contact-0F172A?style=flat-square&logo=gmail&logoColor=white)](mailto:mustafa1997670@gmail.com)

Interested in ClinLeen for your clinic, or in a demo? Get in touch.
