# Internship Defense Presentation Draft

## Slide 1: Title Slide
*   **Topic:** AttendancS.I Group Co., Ltd.)
*   **Name:** Phy Vathane Management System & Leave Request Platform Integration
*   **Company:** SINET (ak
*   **Role:** Software Developer Intern

## Slide 2: Introduction to Company (SINET)
*   **Profile:** A specialist Internet and Telecom Service Provider in Cambodia focusing on engineering excellence and reliable support. Operates under S.I Group Co. Ltd.
*   **History:** Established in 2009. Expanded infrastructure nationwide with over 200 network POPs covering cities, provinces, and remote areas.
*   **Products & Services:** 
    *   Fiber internet and enterprise connectivity solutions.
    *   Telecom infrastructure and corporate network solutions (DWDM, SDH, Metro Ethernet).
    *   Nationwide technical support services.

## Slide 3: My Role
*   **Position:** Software Developer Intern
*   **Department:** Engineering & Operations Department
*   **Core Responsibility:** Developing, maintaining, and extending the company's internal HR Attendance and Leave Management platforms.

## Slide 4: Problem Statement (Why build QR Attendance?)
*   **Previous Era:** SINET used physical biometric scanners.
*   **The Problem:** High hardware costs, difficult to manage across many remote branches, and long queues for staff checking in.
*   **The Solution:** The company shifted to a QR-based attendance system via Telegram to centralize data and reduce hardware dependency.

## Slide 5: Existing System
*   **What was already there:** A basic QR-code check-in/check-out system accessible via a Telegram Mini App.
*   **Core Function:** Captured check-in times and mapped them to basic branch locations.

## Slide 6: Current Challenge
*   **Incomplete Rules:** The system could not handle flexible working schedules or varied shifts.
*   **Data Privacy:** No data isolation between different companies under the S.I Group.
*   **Manual Workload:** HR still processed leaves manually and had to calculate missing attendance by hand.
*   **Performance:** The database queries were slow as the system grew.

## Slide 7: Objectives
*   **Automate HR Operations:** Reduce manual attendance tracking and payroll deduction calculations.
*   **Enhance System Scalability:** Re-architect the system to securely support multiple sister companies under S.I Group.
*   **Improve User Experience:** Make attendance scanning and leave requests completely seamless for staff via Telegram.
*   **Ensure Data Accuracy:** Eliminate missing attendance records through automated system checks.

## Slide 8: Literature Review
*   **CheckinMe (Commercial SaaS):** Evaluated existing SaaS platforms. They offer great features but lack custom workflow flexibility and force company data onto third-party servers.
*   **SINET's Approach:** Using Telegram internally ensures high user adoption (since it's popular in Cambodia) and guarantees complete internal data ownership.

## Slide 9: Features That I Already Built
*   **Company Isolation:** Strict dynamic filtering so HR only sees their own company's staff.
*   **Shift Engine:** Automated logic to determine exactly when a staff member should be working (Base Shifts, Manager Plans).
*   **Daily Automation:** Scripts that run every morning to automatically detect missing check-ins/outs.
*   **Leave Request Platform:** Mobile request forms, multi-tier Telegram Approval Bots, and Web Calendars.

## Slide 10: Methodology & Team Workflow
*   **Approach:** Incremental Development Approach.
*   **Professional Workflow (3 Parts):**
    *   **1. Task Assignment:** Received direct tasks and goals from the **CTO**.
    *   **2. Technical & Deployment:** Discussed development concepts and coordinated live deployment with **Senior Developers**.
    *   **3. End-User Interaction:** Met directly with staff and HR to clarify requirements, gather feedback, and provide support when they faced system issues.

## Slide 11: Tools I Used to Build
*   **Frontend:** React.js / Next.js, Bootstrap, Telegram Mini App SDK.
*   **Backend:** Python (Django Rest Framework), Node.js (Next.js API).
*   **Database:** PostgreSQL, Prisma ORM.
*   **Infrastructure:** Docker, Docker Compose, Nginx.

## Slide 12: Implementation (Use Case & ERD Concept)
*   **System Roles (Use Case):** 
    *   **Staff:** Request leave, check-in via QR.
    *   **Team Lead:** Plan team shifts, approve/reject leaves via Telegram bot.
    *   **Admin:** Manage HR reports and company leave balances.
    *   **Super Admin:** Configure system settings and audit logs.
*   **ERD Concept:** Linking `Users` to their `Shifts`, `Attendance Records`, and `Leaves`. 
*(Note: Briefly show this and move on to the sequence diagrams!)*

## Slide 13: Implementation (Sequence Diagrams)
*   **Concept 1: Attendance Scan Flow**
    *   Staff scans DeepLink QR -> Mini App fetches GPS -> Backend validates location & network -> Attendance recorded.
*   **Concept 2: Leave Request Flow**
    *   Staff submits leave via Mini App -> Next.js API triggers Webhook -> Manager approves via Bot -> HR approves -> Database updates.

## Slide 14: Deployment Strategies
*   **Data Migration Planning:** Safely partitioned legacy data between companies without corrupting historical payroll.
*   **QA Testing:** Conducted strict Unit testing for edge cases, and E2E (End-to-End) testing on physical devices before release.
*   **Pre-Release Simulation:** Tested all migrations and Docker builds on a staging server first.
*   **Rollback Strategy:** Maintained physical backups and marker-based rollback scripts to ensure we could revert instantly if a production bug occurred.

## Slide 15: Findings, Conclusion & What I Learned
*   **Core Findings:**
    *   Time tracking is now highly accurate based on shifts, completely removing manual HR calculations.
    *   Staff can check in instantly using the fast camera DeepLink.
    *   Leaves are now permanently recorded in the system history for management and HR, replacing old manual Excel sheets and Redmine tracking.
*   **What I Learned:**
    *   How to integrate Python/Django with Next.js/React.
    *   How to safely manage and migrate a live-production database.
*   **Conclusion:** Delivered an enterprise-grade platform that is actively improving SINET’s daily operations.

## Slide 16: Video Demo
*   **1. Attendance Scan (Staff):** Scanning the QR code instantly via the camera DeepLink.
*   **2. Shift Management (Team Lead):** Showing how a manager assigns a shift plan for their team.
*   **3. Leave Request (Staff to HR):** Requesting a leave on the Mini App and approving it via the Telegram Bot.
*   **4. HR Processing (Admin):** Generating the daily attendance and deduction reports on the Back Office.

---
*(End of Presentation)*