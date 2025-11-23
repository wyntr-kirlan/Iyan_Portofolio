## Implementation of Odoo ERP for Kopi Gaiyo (Multi-Outlet Coffee Shop)

### About Project 
- Client/Company: Gayo
- Project Duration: Three Months
- Objective: Integration with Odoo ERP. 

### Background of Kopi Gaiyo & Integration with Odoo ERP
Kopi Gaiyo is a growing coffee shop business operating three physical outlets with plans to expand into a franchise model. As transaction volumes increased, the business faced challenges in managing multi-outlet operations, payment processing, inventory synchronization, and delivery platform workflows.

To address these challenges, Kopi Gaiyo planned the implementation of Odoo Enterprise as a unified ERP and POS solution. The integration of Odoo allows the business to benefit from:

- Real-time monitoring of sales and stock across outlets
- Unified payment channels (QRIS, cash, EDC, delivery platforms)
- Automated reporting and operational oversight
- Improved accuracy in inventory and financial reconciliation

The project also utilized a hybrid server architecture, combining a home server (homelab) for operations and cloud backup for security and remote access.

### Project Overview
This project focuses on creating a dynamic Power BI dashboard to visualize ESG performance in real-time. The goal is to provide stakeholders with clear, actionable insights into ESG trends and identify areas for improvement. This involves collecting data from various sources, designing interactive visualizations, and collaborating with IT to ensure seamless data integration. 

### Problems & System Solutions Using Odoo
Business Problems Identified
1. **Stock inconsistencies across outlets**: Manual stock updates caused discrepancies between physical stock and system records.
2. **Lack of centralized data**: Sales, cash flow, and delivery transactions were scattered across spreadsheets and delivery apps.
3. **Manual reconciliation of QRIS, cash, and EDC payments**: Cashiers often made mistakes recording payment types.
4. **Slow reporting and no real-time dashboards**: Decision-making required waiting for end-of-day manual reports.

#### System Solutions Implemented with Odoo
- Odoo POS to centralize outlet transactions.
- Odoo Inventory to synchronize stock movement automatically.
- Odoo Sales & Invoicing for financial documentation.
- Odoo Users & Access Rights for cashier and manager roles.
- QRIS Integration (via Midtrans – planned) for seamless digital payments.
- Menu Management via Odoo Website/Backend to ensure delivery platform consistency.
- Cloud Backup System for disaster recovery.

### Implementation of Kopi Gaiyo POS (Technical & Functional Overview)
![](https://github.com/wyntr-kirlan/Iyan_Portofolio/blob/374a55d0e82214f6b680df34d85bd9f408a9853d/ERP%20Project/Kopi%20Gayo/Workflow%20Kopi%20Gayo.png)

**Hybrid Architecture Diagram**:
  Outlet POS → Home Server (Odoo + PostgreSQL) → Cloud Backup/Remote Access
- Outlets operate with Odoo POS front-end.
- All transactional data is pushed to the home server running Odoo + PostgreSQL.
- Automatic replication to cloud storage ensures data security.
- Admin dashboard accessed remotely for monitoring sales & stock.

### Detailed Workflows: 
**POS Transaction Workflow**
1. Cashier processes an order using Odoo POS.
2. Customer chooses payment method:
- QRIS (system generates QR code → customer scans → payment confirmed)
- Cash (cashier inputs amount received)
- EDC/Tap Debit (input transaction reference)
3. Odoo automatically:
- Decreases stock
- Records payment type
- Creates backend sales record
4. Admin reviews all transactions through the backend dashboard.


### Processes with Odoo ERP: 
1. **Sales**: Used for order validation, payment tracking, and receipt generation.
2. **POS Module**: Front-end interface for cashiers; supports QRIS, EDC, cash, and delivery orders.
3. **Purchase**: Controls supplier orders and restocking demands.
4. **Accounting/Reporting**: Delivers real-time sales summaries and financial tracking.


### Benefits of Using Odoo POS: 
**Operational Benefits** 
- Real-time stock updates across all outlets
- Faster cashier workflow
- Accurate payment reconciliation
- Reduced manual errors
- Unified database for sales history

**Business Benefits** 
- Better decision-making through dashboards
- Reduced loss from stock discrepancies
- Consistent menu/pricing across delivery channels
- Scalability for future franchise expansion

**Impact of Automation** 
- 40–60% faster reporting
- Reduced stock discrepancies by up to 90%
- Centralized control for 3 outlets
- Real-time cash flow visibility

### Estimated Cost Summary
- Odoo Enterprise License: approx. $24/user/month
- Home Server Hardware: Rp 5–10 juta
- QRIS Integration (Midtrans): Free setup + transaction fee
- Implementation Setup: Rp 100–150 juta range
- Cloud Backup: Rp 1jt–2.5/month
