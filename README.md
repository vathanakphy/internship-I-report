**Slide 1: Title Slide**

- **Topic:** Attendance System
- **Name:** Phy Vathanak
- **Company:** SINET
- **Role:** Software Developer Intern

**Slide 2: Introduction to Company (SINET)**

- **Profile:** A specialist Internet and Telecom Service Provider in Cambodia focusing on engineering excellence and reliable support. Operates under S.I Group Co. Ltd.
- **History:** Established in 2009. Expanded infrastructure nationwide with over 200 network POPs covering cities, provinces, and remote areas.
- **Products & Services:**
    - Fiber internet and enterprise connectivity solutions.
    - Telecom infrastructure and corporate network solutions (DWDM, SDH, Metro Ethernet).

**Slide 3: My Role**

- **Position:** Software Developer Intern
- **Department:** Engineering & Operations Department
- **Core Responsibility:** Developing, maintaining, and extending the company's internal Attendance platforms.

**Slide 4: Problem Statement**

- **Previous Era:** SINET used physical biometric scanners.
- **The Problem:**
    - **Manual HR Process:** Time-consuming attendance and shift management.
    - **Long Check-in Queues:** Slow attendance registration during peak times.
    - **Remote Branch Management:** Difficult to manage attendance across multiple locations.
- **The Solution:** The company built their own QR-based attendance system via Telegram.

**Slide 5: Existing System**

- A QR-code check-in/check-out system accessible via a Telegram Mini App.

**Limitation**

- **Incomplete Rules:** The system could not handle SINET business rules.
- **Manual Workload:** HR still processed manually and had to calculate missing attendance by hand.
- **Performance:** The database queries were slow as the system grew.

**Slide 7: Objectives**

- **Automate HR Operations:** Eliminate manual attendance tracking and **reduce administrative workload** through an automated attendance management system.
- **Enhance System Scalability:** Optimize the existing system architecture to **improve performance, reliability, and data accuracy** while supporting future organizational growth.
- **Improve User Experience:** Deliver a more intuitive system for users to make it less confusing.

**Slide 8: Literature Review**

- **CheckinMe (Commercial SaaS):** Evaluated existing SaaS platforms. They offer great features but lack custom workflow flexibility and force company data onto third-party servers.

**Slide 9: Core Features**

- **Deep Link QR:** Camera-based QR check-in/check-out.
- **Company Isolation:** Secure multi-company data access.
- **Shift & Schedule Management:** Flexible schedules and work planning.
- **HR Reports:** Attendance, monthly summaries, and payroll deductions.
- **Leave Management:** Telegram leave requests with approval workflow.

**Slide 10: Methodology & Team Workflow**

- **Approach:** Incremental Development Approach.
- **Workflow:** Analysis Requirement → Dev → Testing → Release
- **Professional Workflow (3 Parts):**
    1. **Task Assignment:** Received direct tasks and goals from the CTO.
    2. **Technical & Deployment:** Discussed development concepts and coordinated live deployment with Senior Developers.
    3. **End-User Interaction:** Met directly with staff and HR to clarify requirements, gather feedback, and provide support when they faced system issues.

**Slide 11: Tools & Technology**

- **Frontend:** Next.js, Bootstrap, Tailwind CSS.
- **Backend:** Python (Django), Node.js (Next.js App Routing).
- **Database:** PostgreSQL.
- **Tools:** Docker, Nginx, Telegram.

**Slide 12: Implementation (Use Case & ERD Concept)**

- **System Roles (Use Case):**
    - **Staff:** Request leave, check in via QR.
    - **Team Lead:** Plan team shifts, approve/reject leaves.
    - **Admin:** Manage HR reports and company leave balances.
    - **Super Admin:** Perform full actions, audit logs, add new company.

**Slide 13: Implementation (Sequence Diagrams)**

- **Concept 1: Attendance Scan Flow**
    - Staff scans DeepLink QR -> Mini App fetches GPS -> Backend validates location & network -> Attendance recorded.
- **Concept 2: Leave Request Flow**
    - Staff submits leave via Mini App -> Next.js API triggers Webhook -> Manager approves via Bot -> HR approves -> Database updates.

**Slide 14: Release Strategies**

- **Migration & Rollback Planning:** Prepared database migration and rollback plans before deployment.
- **Local Testing:** Verified functionality and conducted end-to-end (E2E) testing in the local development environment.
- **Pre-Production Simulation:** Simulated the complete deployment process in the pre-production environment, including migrations and rollback scripts,  before production.

| **Phase** | **Date** | **Focus Area & Changes Deployed** |
| --- | --- | --- |
| Release 1 | 13-May-2026 | Server-side optimization (pagination, search, export) and attendance report improvements. |
| Release 2 | 21-May-2026 | Shift plan driven attendance, manager scheduling dashboard, and daily attendance automation. |
| Release 3 | 05-Jun-2026 | Company structure isolation, audit logging, recycle bin recovery, and expanded leave handling. |
| Release 4 | 16-Jun-2026 | Leave replacement, manual time selection, centralized action logs, UI upgrades, and Mini App modularization. |
| Release 5 | 1-July-2026 | In-system User Manuals, FAQs, Manager Excel import, shift and leave improvement. |
| Release 6 | 18-July-2026 ( might be) | Leave Request Platform |

**Slide 15: Findings, Conclusion & What I Learned**

- **Core Findings:**
    - Removing manual HR work via a system providing reports and flexible shift work.
    - Staff can check in instantly using the fast camera DeepLink.
    - Leaves are now permanently recorded in the system history for management and HR.
- **Lessons Learned:**
    - How to integrate Python/Django with Next.js/React.
    - How to safely manage and migrate a live-production database.

**Slide 16: Video Demo**

1. **Attendance Scan (Staff):** Scanning the QR code instantly via the camera DeepLink.
2. **Shift Management (Team Lead):** Showing how a manager assigns a shift plan for their team.
3. **Leave Request (Staff to HR):** Requesting leave on the Mini App and approving it via the Telegram Bot.
4. **HR Processing (Admin):** Generating the daily attendance and deduction reports on the Back Office.

**Slide 17-End: Resources**

- Testing result
- ERD
- Log