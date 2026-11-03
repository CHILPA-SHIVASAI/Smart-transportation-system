# SmartTrans

SmartTrans is a responsive HTML/CSS/vanilla JavaScript logistics demonstration. It includes a public landing and tracking view, local demo registration and login, role-specific dashboards, connected fleet/driver/customer/shipment workflows, and the advanced feature areas 53–100.

## Run locally

Open this folder in VS Code and start **Live Server** on `index.html`, or open `index.html` in a current browser. Chart.js, Leaflet, QRCode.js, OpenStreetMap tiles, and the Inter/Manrope fonts load from public CDNs and need an internet connection. There is no backend or build step.

## Demo accounts

| Role | Email | Password |
| --- | --- | --- |
| Admin | `admin@smarttrans.com` | `Admin@123` |
| Manager | `manager@smarttrans.com` | `Manager@123` |
| Driver | `driver@smarttrans.com` | `Driver@123` |
| Customer | `customer@smarttrans.com` | `Customer@123` |

Sample tracking IDs: `ST-849301`, `ST-849276`.

## Main workflows

- Register as a customer or driver; admin and manager accounts are seeded demo accounts.
- Sign in to see a role-specific dashboard and navigation. Customer shipment views are scoped to their account; drivers see their assigned shipments.
- Create, search, edit, export, and delete connected vehicle, driver, customer, shipment, warehouse, inventory, maintenance, fuel, payment, support, and trip records.
- Track shipment status from its tracking ID; shipment status updates drive the tracking timeline.
- Estimate a route using approximate coordinate distance; map locations and traffic remain simulated.
- Import shipment CSV records with validation and duplicate detection; export CSV or back up and restore JSON data.
- Use the in-app assistant for answers based on records visible to the active role.

## Data and security limits

Records and demo accounts are stored in browser `localStorage`; the active session is stored in `sessionStorage`. Demo passwords are kept in plain browser storage so this project can demonstrate the flow. This is not secure authentication, a secure database, or server-side authorization. Do not use real credentials or sensitive personal data. Production deployment requires a backend, password hashing, server-enforced authorization, a database, and configured identity, payment, routing, and tracking services. GPS, traffic, weather, route estimates, payments, email, document review, and company isolation are demonstrations or unavailable integrations.

## Files

- `index.html` — app shell, public views, dialogs, and library imports
- `styles.css` — public site, authentication, dashboard, and responsive styling
- `app.js` — app navigation, demo auth, storage, role checks, CRUD, dashboards, charts, maps, and simulated workflows

## Suggested manual checks

1. Register a customer and a driver; try the same email twice and mismatched passwords.
2. Sign in with each demo role and confirm available navigation differs.
3. As Admin, add a vehicle and driver; confirm duplicate registration and license checks.
4. Create a shipment, assign registered fleet records, track it, and update its status.
5. Sign in as the Customer demo and confirm only its shipments appear. Sign in as the Driver demo and confirm only assigned shipments appear.
6. Check CSV preview/confirmation, JSON backup/restore, notifications, dark mode, and mobile layout.

