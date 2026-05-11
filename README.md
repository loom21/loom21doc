<a id="docs-top"></a>

<h3 align="center">Loom21 Docs</h3>

  <p align="center">
    Track and manage your inventory, invoices, customers, vendors, payments and more.
    <br />
    <a href="https://github.com/loom21/loom21doc" target="_blank"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/loom21/loom21doc/issues" target="_blank">Report Bug</a>
    ·
    <a href="https://github.com/loom21/loom21doc/issues" target="_blank">Request Feature</a>
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#create-account">Create Account</a></li>
        <li><a href="#sign-in">Sign In</a></li>
      </ul>
    </li>
    <li><a href="#dashboard">Dashboard</a></li>
    <li><a href="#payment-links">Payment Links</a></li>
    <li>
      <a href="#sales">Sales</a>
      <ul>
        <li><a href="#add-edit-sales">Add/Edit Sales</a></li>
        <li><a href="#payments">Payments</a></li>
      </ul>
    </li>
    <li>
      <a href="#reports">Reports</a>
      <ul>
        <li><a href="#sales-report">Sales Report</a></li>
        <li><a href="#deliveries-report">Deliveries Report</a></li>
      </ul>
    </li>
    <li>
      <a href="#settings">Settings</a>
      <ul>
        <li><a href="#general-settings">General Settings</a></li>
        <li><a href="#stripe">Stripe</a></li>
        <li><a href="#btcpay-server">BTCPay Server</a></li>
        <li><a href="#misty-breez">Misty Breez</a></li>
        <li><a href="#speed-wallet">Speed Wallet</a></li>
        <li><a href="#lnbits">LNBits</a></li>
        <li><a href="#product-settings">Product Settings</a></li>
        <li><a href="#product-categories">Product Categories</a></li>
        <li><a href="#measures">Measures</a></li>
        <li><a href="#brands">Brands &amp; Models</a></li>
        <li><a href="#custom-fields">Custom Fields</a></li>
        <li><a href="#price-lists">Price Lists</a></li>
        <li><a href="#import-templates">Import Templates</a></li>
      </ul>
    </li>
    <li><a href="#accounts">Accounts</a></li>
    <li><a href="#products-services">Products and Services</a></li>
    <li><a href="#inventory">Inventory</a></li>
    <li><a href="#stores">Stores</a></li>
    <li><a href="#deliveries">Delivery Orders</a></li>
    <li><a href="#customers-suppliers">Customers and Suppliers</a></li>
    <li><a href="#user-profile">User Profile</a></li>
  </ol>
</details>

<!-- GETTING STARTED -->
## Getting Started<a id="getting-started"></a>

In order to start using the loom21 app you need to create an account. Here is the recommended setup flow:

1. **Create an account** and confirm your email.
2. Configure **[General Settings](#general-settings)** — set your language, currency, VAT, and address.
3. Configure at least one **[payment processor](#settings)** (Stripe, BTCPay Server, etc.) so it appears at checkout.
4. Add your **[Products and Services](#products-services)**.
5. Create your first **[Sale](#sales)**.

### Create Account<a id="create-account"></a><a id="sign-in"></a>
After you sign up you will receive a confirmation email to confirm your account and then you can sign in.
![Sign Up to app.loom21.com](https://raw.githubusercontent.com/loom21/loom21doc/main/images/sign-up-and-in-light.PNG)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

<!-- DASHBOARD -->
## Dashboard<a id="dashboard"></a>

The Dashboard is the first page you see after signing in. It gives you an at-a-glance overview of your business performance for the selected time period.

**Key features:**

- **Period selector** — Choose from the last 30 days or any of the previous 6 calendar months to compare your performance over time.
- **KPI cards** — At the top you will find summary cards showing:
  - Total fiat revenue (card and bank payments)
  - Total Bitcoin revenue (in satoshis)
  - Number of paid invoices, broken down by payment method (Bitcoin vs. fiat)
  - Delivery orders completed and those still pending confirmation
  - Paid payment links, broken down by payment method
  - Trend indicators (up/down arrows) so you can quickly see whether your numbers are improving.
- **Sales chart** — A bar chart showing daily sales volume for the selected period.
- **Payment Links chart** — A bar chart showing daily payment link activity.
- **Deliveries chart** — A bar chart showing daily delivery order activity.
- **Activity feed** — A chronological list of recent events across sales, deliveries, and payment links.
- **Light / Dark mode toggle** — Switch between light and dark themes using the icon button in the top-right corner of the Dashboard toolbar. Your preference is applied immediately across the whole application.

![Dashboard overview](https://raw.githubusercontent.com/loom21/loom21doc/main/images/dashboard.png)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

<!-- PAYMENT LINKS -->
## Payment Links <a id="payment-links"></a>

A payment link is a unique URL you can share with customers to accept payments for a product, service, or donation — no login required on the buyer's side. Once created, you can copy the link, send it by email or message, or embed it anywhere.

**How to create a payment link:**

1. Navigate to **Payment Links** from the sidebar and click **New**.
2. Fill in the details:
   - **Name** — what the buyer will see (e.g. "Workshop Ticket").
   - **Currency** — the currency for this link.
   - **Amount** — the fixed price, or toggle **Variable Amount** to let the buyer enter their own amount within a min/max range you define.
   - **VAT** — enable and set a VAT percentage if applicable.
   - **Description** — optional details shown to the buyer.
   - **Image URL** — add a product photo that appears on the payment page.
   - **Short Code** — a memorable short identifier for the link (optional).
   - **Expiration Date** — automatically deactivate the link after a specific date.
   - **Stock Count** — limit the total number of purchases through this link.
   - **Max Per Order** — limit how many units a single buyer can purchase at once.
3. Select the **payment methods** to offer (only enabled processors appear here).
4. Add **promo codes** if you want to offer discounts — each code has a name, a discount value, and a type (percentage or fixed amount).
5. Click **Save**.

**After saving**, the link URL is shown at the top of the page. Use the **Copy** button to copy it to your clipboard, or **Preview** to open it as a buyer would see it.

**Pausing a link** — click the status toggle to pause a published link (buyers will no longer be able to pay) or re-publish it. You will be asked to confirm the change.

#### Supported Payment Processors

| Processor | Payment Type |
|-----------|-------------|
| Stripe | Credit / Debit Card |
| BTCPay Server | Bitcoin Lightning & On-chain |
| Misty Breez | Bitcoin Lightning & On-chain |
| Speed Wallet | Bitcoin Lightning & On-chain |
| LNBits | Bitcoin Lightning |

> :bell: More payment processors are coming soon.

![Payment Link](https://raw.githubusercontent.com/loom21/loom21doc/main/images/payment-link-add.gif)

<p align="right">(<a href="#docs-top">back to top</a>)</p>


## Sales<a id="sales"></a>

The Sales page lists all your sale orders. You can search by order number or customer name. Create a new order with the **New Order** button, or open an existing order by clicking the purple arrow icon.

![Sales list](https://raw.githubusercontent.com/loom21/loom21doc/main/images/sales-list-light.PNG)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### Add/Edit Sales <a id="add-edit-sales"></a>

**Order header fields** (left panel):
- **Serial Number** — auto-generated, but editable.
- **PO Number** — the customer's purchase order reference, if applicable.
- **Order Date / Due Date** — when the order was placed and when payment is expected.
- **Status** — track the order through Draft, Sent, Paid, etc.
- **Store** — select which store the goods are dispatched from (affects inventory levels; not applicable for services).
- **VAT** — enable or disable VAT per order; the percentage is inherited from your General Settings.
- **Discount %** — apply an overall percentage discount to the order total.
- **Note** — any internal note or instructions.

**Adding items:**
- Type directly into the product search field to add items one at a time.
- Click **Select Items** to search and tick multiple products or services at once.
- Click **Order History** (available once a customer is selected) to view that customer's previous purchases and re-add items from past orders in one click.

**Automatic price resolution** — when you select a product and a customer, the system automatically looks up the best applicable price from your [Price Lists](#price-lists) and [Customer Price Overrides](#price-lists). The unit price field updates instantly; you can still edit it manually if needed.

**Customer selection** — search and select a customer to automatically populate the shipping and billing address. You can modify the address fields directly on the order if needed.

![Saved sale order](https://raw.githubusercontent.com/loom21/loom21doc/main/images/sale-order-saved-light.PNG)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### Payments <a id="payments"></a>

The toolbar on a saved order gives you quick access to all payment and document actions:

**Pay** — a dropdown button showing every enabled payment processor. Choose one to open the payment dialog:
- **Stripe** — the customer enters card details directly in a secure dialog.
- **Bitcoin processors** (BTCPay Server, Misty Breez, Speed Wallet, LNBits) — a QR code and Lightning/on-chain payment address is displayed. Bitcoin payments are confirmed in real time — the order status updates automatically the moment the transaction is settled, without needing to refresh the page.

**Send** — saves the order and opens a dialog with the payment URL and print URL that you can copy and share with the customer.

**Download** — a dropdown to generate and download PDF documents:
- **Quote** — available before payment.
- **Invoice** — available once the order is marked as paid.
- **Receipt** — available once the order is marked as paid.
- **Pickup List** — available at any time.

**Set as Paid** — manually mark the order as paid (for cash or other offline payments).

**Export JSON** — download the full order data as a JSON file.

**Copy Order** — creates a new draft order pre-filled with the same customer, line items, payment methods, addresses, VAT settings, discount, currency, and notes as the current order. The copy is assigned the next available order number and opens immediately so you can review and adjust it before saving. Use this to quickly repeat a previous order or use an existing order as a starting template.


![Share sale order](https://raw.githubusercontent.com/loom21/loom21doc/main/images/share-sale-order.png)

![Pay with bitcoin](https://raw.githubusercontent.com/loom21/loom21doc/main/images/sale-order-lightning-payment.png)

![Pay with card](https://raw.githubusercontent.com/loom21/loom21doc/main/images/sale-order-stripe-payment.png)

> :bell: All features within the application are protected by authentication, except for the links generated through the Send button.

<p align="right">(<a href="#docs-top">back to top</a>)</p>

<!-- REPORTS -->
## Reports<a id="reports"></a>

The Reports section gives you detailed insight into your sales and delivery activity. Navigate to **Reports** from the sidebar to choose a report type.

<!-- ![Reports menu](screenshots/reports-menu.png) -->

### Sales Report<a id="sales-report"></a>

The Sales Report shows a full, searchable, and filterable list of every product or service that has been sold — one line per line item across all orders.

**How to use:**

1. Navigate to **Reports → Sales Report**.
2. Use the **search bar** at the top to find items by product name or serial number.
3. Click **Filters** to expand the filter panel and narrow results by:
   - **Date range** — select a start and end date.
   - **Category** — filter by product category.
   - **Measure** — filter by unit of measurement.
   - **Brand / Model** — filter by brand, and then by specific model within that brand.
   - **Customer** — type a customer name to search and filter by a specific buyer.
4. Press the **Search** button (magnifying glass) to apply your filters.
5. Click **Clear** to reset all filters and start fresh.
6. Use the **Export** menu to download the report:
   - **Export CSV** — downloads a spreadsheet-compatible file you can open in Excel or Google Sheets.
   - **Export JSON** — downloads a structured data file for technical use.
7. Results are sortable by clicking any column header. Use the **pagination** controls at the bottom to navigate through large result sets.
8. Click the arrow icon on any row to navigate directly to the original sale order.

Columns shown: Product name, barcode, serial number, quantity, note, unit price, total price, customer name, measure, category, and date.

![Sales Report](https://raw.githubusercontent.com/loom21/loom21doc/main/images/sales-report.png)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### Deliveries Report<a id="deliveries-report"></a>

The Deliveries Report provides the same detailed, filterable view for delivery orders — showing every product that has been received as a delivery, along with supplier and date information.

Use it in the same way as the Sales Report: apply filters, search, sort, and export as needed.

![Deliveries Report](https://raw.githubusercontent.com/loom21/loom21doc/main/images/deliveries-report.png)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

<!-- SETTINGS -->
## Settings<a id="settings"></a>

Configure your organization's preferences and payment processors here. Payment processors must be set up in this section before they become available as options at checkout or in payment links.

### General settings <a id="general-settings"></a>

This is where you configure your organization's core identity and preferences. These settings affect the whole application.

**Company details:**
- **Company Name, Email, Phone** — appear on printed invoices and documents.
- **Billing Address** — your organization's address, also printed on documents.

**Localization:**
- **Language** — changes the application language. The page reloads automatically when you save a language change.
- **Currency** — your primary operating currency. Affects prices, totals, and reports throughout the app.
- **Default Store** — the store pre-selected when creating new sales and deliveries.

**VAT settings:**
- **Enable VAT** — turns VAT on globally. You can still toggle it per order.
- **VAT Number** — your organization's tax registration number, printed on invoices.
- **VAT Percentage** — the default rate applied to new orders.

**Inventory control:**
- **Forbid Negative Quantity** — when enabled, the system will not allow a sale that would take a product's stock below zero.

**Bitcoin settings:**
- **Hide Bitcoin Prices** — removes all Bitcoin price displays and payment options across the app.
- **Override Bitcoin Rate** — lets you enter a fixed exchange rate instead of using the live market rate. Useful for invoicing in a fixed BTC price.
- **Use Bitcoin Only** — hides fiat totals and shows only Bitcoin amounts.

**Theme:**
- **Dark Mode** — toggle between light and dark theme. This can also be toggled quickly from the [Dashboard](#dashboard).

![General Settings Setup](https://raw.githubusercontent.com/loom21/loom21doc/main/images/general-setting-light.gif)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### Stripe<a id="stripe"></a>
- To accept fiat payments via Stripe, configure your Stripe Publishable and Secret keys.

![Stripe Setup](https://raw.githubusercontent.com/loom21/loom21doc/main/images/stripe-light.PNG)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### BTCPay Server<a id="btcpay-server"></a>
- Self-hosted Bitcoin payment processor supporting both Lightning and on-chain payments.
- Configure your BTCPay Server URL and API Key to enable it.

![BTCPay Server Setup](https://raw.githubusercontent.com/loom21/loom21doc/main/images/btcpay-server-light.PNG)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### Misty Breez<a id="misty-breez"></a>
- Non-custodial Bitcoin wallet supporting both Lightning and on-chain payments.
- Enter your Misty Breez API Key to enable it.

![Misty Breez](https://raw.githubusercontent.com/loom21/loom21doc/main/images/misty-breez.png)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### Speed Wallet<a id="speed-wallet"></a>
- Bitcoin wallet supporting both Lightning and on-chain payments.
- Enter your Speed Wallet API Key to enable it.

![Speed Wallet](https://raw.githubusercontent.com/loom21/loom21doc/main/images/speed-wallet.png)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### LNBits<a id="lnbits"></a>
- Open-source Lightning Network accounts system. Supports multiple wallets and extensions.
- Configure your LNBits URL and API Key to enable it.

![LNBits](https://raw.githubusercontent.com/loom21/loom21doc/main/images/lnbits.png)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### Product Settings<a id="product-settings"></a>

The **Product Settings** section (found under Settings in the sidebar) groups several configuration pages that control how your products are organized, described, and priced. Use the sub-navigation to switch between:

- **Brands & Models** — manufacturers and product model lines
- **Categories** — groups for organizing products
- **Measures** — units of measurement
- **Custom Fields** — additional fields you define for product data
- **Price Lists** — tiered and customer-specific pricing rules

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### Product Categories <a id="product-categories"></a>

Categories let you group related products together, making them easier to find and filter across the app — on the Products list, in Inventory, and in Reports.

**Adding a category:**

1. Navigate to **Settings → Product Settings → Categories**.
2. Click **Add** (or the **+** button) to open the category form.
3. Enter a **Name** for the category (e.g. "Electronics", "Clothing", "Raw Materials").
4. Click **Save**. The new category appears in the list and is immediately available to assign to products.

**Editing a category:**

1. Find the category in the list and click the **edit** icon on its row.
2. Update the name as needed.
3. Click **Save**. The change is reflected everywhere the category is used.

**Deleting a category:**

1. Click the **delete** icon on the category row.
2. Confirm the deletion when prompted.

> Products already assigned to that category are not deleted — they simply lose the category association and will show no category until you reassign them.

![Product Categories Setup](https://raw.githubusercontent.com/loom21/loom21doc/main/images/product-categories-light.PNG)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### Measures<a id="measures"></a>

Measures define the units of measurement used when describing product quantities — for example, kilograms, liters, pieces, or meters. Once defined, a measure can be assigned to any product or service and is used throughout the app in inventory, sales, and reports.

**Adding a measure:**

1. Navigate to **Settings → Product Settings → Measures**.
2. Click **Add** (or the **+** button) to open the measure form.
3. Enter a **Name** for the unit (e.g. "Kilogram", "Piece", "Liter").
4. Click **Save**. The measure is now available to assign to products and services.

**Editing a measure:**

1. Find the measure in the list and click the **edit** icon on its row.
2. Update the name as needed.
3. Click **Save**. The updated name is reflected wherever the measure is used.

**Deleting a measure:**

1. Click the **delete** icon on the measure row.
2. Confirm the deletion when prompted.

> Products already using that measure are not deleted — they simply lose the measure association and will show no unit until you reassign them.

![Measures Setup](https://raw.githubusercontent.com/loom21/loom21doc/main/images/measures-light.PNG)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### Brands & Models<a id="brands"></a>

If your products are associated with manufacturers or brand names, you can manage those brands here. Each brand can have multiple models beneath it, which you can then assign to individual products for more detailed categorization and reporting.

**How to use:**

1. Navigate to **Settings → Product Settings → Brands**.
2. Click **Add** to create a new brand. Enter the brand name, an optional description, and a logo URL if you have one.
3. Click a brand in the list to see its details on the right side and manage its models.
4. Within the brand detail panel, click **Add Model** to create models (e.g. specific product lines or versions) belonging to that brand.
5. Use the edit and delete buttons to update or remove brands and models as needed.

Once brands and models are set up, you can assign them to products on the product edit page. This lets you filter the Sales Report by brand or model to see exactly which product lines are performing best.

![Brands and Models](https://raw.githubusercontent.com/loom21/loom21doc/main/images/brands-models.png)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### Custom Fields<a id="custom-fields"></a>

Custom Fields let you add your own data fields to every product in your catalog — beyond the standard fields like name, price, and category. For example, you might add a "Warranty Expiry Date," a "Supplier Reference Number," or a "Certified" checkbox.

**How to use:**

1. Navigate to **Settings → Product Settings → Custom Fields**.
2. Click **Add Field** to define a new custom field. You will be asked to enter:
   - **Label** — the name shown on the product form (e.g. "Warranty Expiry").
   - **Field Name** — a short internal identifier (no spaces, e.g. `warrantyExpiry`).
   - **Data Type** — choose from Text, Number, Decimal, Yes/No, or Date.
   - **Required** — whether the field must be filled in before saving a product.
   - **Default Value** — an optional pre-filled value.
3. Use the **drag handle** (the grip icon on the left) to reorder fields — this controls the order they appear on the product form.
4. Use the **toggle switch** to activate or deactivate a field without deleting it. Inactive fields are hidden on product forms but their data is preserved.
5. Click the **edit** or **delete** icons to modify or remove a field definition.

Once custom fields are defined, they appear as an additional tab called **Custom Fields** on every product's edit page, where you can fill in the values for each product.

![Custom Fields settings](https://raw.githubusercontent.com/loom21/loom21doc/main/images/custom-fields-settings.png)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### Price Lists<a id="price-lists"></a>

Price Lists give you full control over your pricing strategy. Instead of using a single fixed price per product, you can create multiple price lists — for example, a "Wholesale" list with lower prices, a "Retail" list, or a seasonal promotion — and assign specific prices per product within each list.

Within each price list you can also set **quantity-based tiers** (the price automatically drops when the customer orders more), apply **percentage discounts**, or even define a **formula** that calculates the price dynamically.

In addition, you can set **customer-specific price overrides** directly on a product — so one particular customer always gets a special price regardless of the active price list.

#### Creating a Price List

1. Navigate to **Settings → Product Settings → Price Lists**.
2. Click **New Price List** to expand the creation form.
3. Enter a **name** (e.g. "Wholesale 2025"), select the **currency**, and optionally set a **Valid From / Valid To** date range to make the list active only during a specific period.
4. Check **Default** if this should be the primary price list used when no other rule matches.
5. Click **Save**. The new list appears in the left panel.

#### Adding Products and Tiers to a Price List

1. Click on a price list in the left panel to open it.
2. In the **Tiers** section, use the product search box to find the product you want to add.
3. Fill in:
   - **Min Qty** — the minimum quantity the customer must order to get this price (leave blank for "any quantity").
   - **Price** — the sale price for this product in this list.
   - **Discount %** — an optional percentage discount applied on top of the price.
   - **Formula** — an advanced option that lets you enter a mathematical expression to calculate the price automatically (e.g. `BasePrice * 0.85` to always apply a 15% reduction). Available variables: `BasePrice`, `Quantity`, and any custom fields you have defined.
4. Click **Add Tier**. You can add multiple tiers for the same product with different minimum quantities to create volume-based pricing steps.
5. Use the **edit** and **delete** icons on each tier row to modify or remove them.

#### Activating or Deactivating a Price List

- Use the **toggle switch** next to each price list name to activate or deactivate it without deleting it.

#### Deleting a Price List

- Click the **delete** icon next to the price list. You will be asked to confirm. Deleting a price list also removes all its tiers.

![Price Lists settings](https://raw.githubusercontent.com/loom21/loom21doc/main/images/price-lists.png)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

### Import Templates<a id="import-templates"></a>

If you already have a list of products, services, customers, or suppliers in a spreadsheet, you can import them directly instead of entering each one by hand.

**Accepted file format:** CSV (.csv) only. The first row must be a header row with the exact column names listed below. Column order does not matter, and any column not marked as required can be left out entirely.

**How to import:**

1. Navigate to **Settings → Product Settings → Import Templates**.
2. Download the template for the type of data you want to import (Products, Services, Customers, or Suppliers) to get a pre-formatted CSV file you can fill in.
3. Open the template in Excel, Google Sheets, or any spreadsheet application and add your data — one row per item.
4. Save or export the file as CSV, then return to the Import Templates page and upload it using the **Upload** button for the appropriate import type.
5. If any rows contain errors (such as a missing required field), the system will show you a list of problems to fix before the import can proceed. Correct the issues in your file and upload again.

Once imported successfully, your records are immediately available in the corresponding section of the app.

#### Products & Services CSV columns

| Column | Required | Description |
|---|---|---|
| `Name` | **Yes** | The product or service name |
| `PriceSale` | No | Selling price (must be 0 or greater) |
| `PriceDelivery` | No | Cost / delivery price (must be 0 or greater) |
| `Code` | No | Your internal product code or SKU |
| `Abr` | No | Short abbreviation for the product name |
| `Barcode` | No | Barcode number |
| `Category` | No | Category name (must already exist in [Product Categories](#product-categories)) |
| `Measure` | No | Unit of measurement (must already exist in [Measures](#measures)) |
| `Brand` | No | Brand name (must already exist in [Brands & Models](#brands)) |
| `Model` | No | Model name within the brand (must already exist in [Brands & Models](#brands)) |
| `Supplier` | No | Supplier name for reference |
| `Note` | No | Internal note |
| `Image` | No | URL to a product image |
| `Discontinued` | No | `true` or `false` — marks the item as discontinued |

> Services use the same column format as Products.

#### Customers & Suppliers CSV columns

| Column | Required | Description |
|---|---|---|
| `Name` | **Yes** | Company or person name |
| `ContactName` | No | Name of the primary contact person |
| `Email` | No | Email address |
| `Phone` | No | Phone number |
| `Website` | No | Website URL |
| `TaxNumber` | No | VAT or tax registration number |
| `Note` | No | Internal notes |
| `AddressLine1` | No | Street address, line 1 |
| `AddressLine2` | No | Street address, line 2 |
| `City` | No | City |
| `Region` | No | State, province, or region |
| `Postcode` | No | Postal or ZIP code |
| `Country` | No | Country name |
| `BitcoinAddress` | No | Bitcoin address for the contact |

> Customers and Suppliers use the same column format.

![Import Templates Setup](https://raw.githubusercontent.com/loom21/loom21doc/main/images/import-templates-light.PNG)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

## Accounts <a id="accounts"></a>

The Accounts page shows all users who have access to your organization. Each row displays the user's email, first name, last name, company name, website, and phone number.

**Inviting a new user:**
1. Click the **Invite** button.
2. Fill in the new user's **email address**, **password**, first name, last name, and phone.
3. Assign one or more **Roles** using the checkboxes — roles control which parts of the app the user can access.
4. Save — the user can now sign in with the credentials you created.

**Editing a user:**
- Click the edit icon on any row to update their details or change their role assignments.

**Removing a user:**
- Open the user's edit page and click **Delete** to remove their access.

You can invite an unlimited number of users to your organization.

![Invite account](https://raw.githubusercontent.com/loom21/loom21doc/main/images/account-invite-light.PNG)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

## Products and Services <a id="products-services"></a>
The Products list lets you search by name or code, filter by Category, Measure, Brand, and Model (selecting a Brand enables the Model filter), and import/export your catalog (CSV or JSON). The table shows each product's name, code, abbreviation, measure, category, barcode, delivery price, sale price, and creation date.

![Products list](https://raw.githubusercontent.com/loom21/loom21doc/main/images/product-list-light.PNG)

Click **New Product** to create one, or click the arrow icon on any row to open it. Available fields:

- **Name** (required), **Abbreviation**, **Code**, **Note**
- **Category**, **Measure**
- **Brand & Model** — assign to a brand and model (configured in [Brands & Models](#brands)); selecting a brand enables the model dropdown.
- **Delivery Price** — the cost price used when receiving stock via delivery orders.
- **Sale Price** — the default selling price (can be overridden by [Price Lists](#price-lists)).
- **Bitcoin prices** — if Bitcoin is enabled, separate Bitcoin price fields appear with arrow buttons to convert between fiat and Bitcoin at the current exchange rate.
- **Barcode & QR Code** — enter or scan a barcode; a QR code is generated automatically.

![Product edit](https://raw.githubusercontent.com/loom21/loom21doc/main/images/product-pricing.png)

#### Custom Fields Tab

If you have defined custom fields in [Settings → Custom Fields](#custom-fields), each product's edit page will include a **Custom Fields** tab. Here you can fill in the values for those extra fields — such as a warranty date, a supplier reference, or any other information specific to your business.

1. Open a product by clicking the purple arrow on the Products list.
2. Click the **Custom Fields** tab.
3. Fill in the values for each field displayed.
4. Click **Save** to store the custom data for this product.

![Product Custom Fields](https://raw.githubusercontent.com/loom21/loom21doc/main/images/product-custom-fields.png)

#### Pricing Tab

Each product also has a **Pricing** tab that lets you view and manage how this specific product is priced across all your price lists, as well as any customer-specific overrides.

**Price List Tiers** — For each price list you have created, you can see the pricing tiers already set for this product. You can delete a tier here; to add new tiers or edit existing ones, navigate to **Settings → Product Settings → Price Lists**.

**Customer Price Overrides** — You can set a special price for a specific customer for this product. Click **Add individual price** to:
- Search for and select a customer.
- Enter the override price (and optionally a minimum quantity, a formula, or a validity date range).
- Click **Save**.

**Test Price Resolution** — Enter a quantity and optionally select a customer, then click **Resolve Price** to see exactly which price the system will calculate for that combination. The result shows the final price and whether it came from a customer override, a price list tier, or the base product price.

![Product Pricing](https://raw.githubusercontent.com/loom21/loom21doc/main/images/product-pricing.png)

#### Services Management

Services are managed from a dedicated **Services** page in the sidebar. The list supports the same search, filter (Category, Measure), import, and export (CSV or JSON) capabilities as the Products list.

**Service fields:**
- **Name** (required), **Abbreviation**, **Code**, **Note**
- **Category**, **Measure**
- **Delivery Price**, **Sale Price** (and Bitcoin equivalents if Bitcoin is enabled)
- **QR Code** — auto-generated from the code field for easy scanning.

Services differ from products in two key ways:
- They are **not tracked in inventory** — selling a service never reduces stock.
- They have no **Brand**, **Model**, **Barcode**, **Custom Fields tab**, or **Pricing tab**.

<p align="right">(<a href="#docs-top">back to top</a>)</p>

## Inventory <a id="inventory"></a>

The Inventory page shows current stock levels for all your products across all stores. Stock is updated automatically as you record sales (which reduce stock) and delivery orders (which add stock).

**Filtering inventory:**
Click **Filters** to expand the filter panel and narrow the list by:
- **Search** — find a product by name.
- **Store** — show stock levels for a specific location.
- **Category, Measure, Brand, Model** — further narrow to specific product groups.

The table shows each product's current quantity, unit of measure, category, brand, and model.

**Manual stock adjustments:**
Click the edit icon on any product row to open the adjustment dialog:
- **Add** — enter a quantity and select a store to increase stock (e.g. after a physical stock count).
- **Remove** — enter a quantity and select a store to decrease stock.

This is useful when correcting discrepancies found during a stock count, or recording stock that was damaged or returned.

![Inventory](https://raw.githubusercontent.com/loom21/loom21doc/main/images/inventory-light.PNG)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

## Stores <a id="stores"></a>

Stores represent your physical locations or warehouses. Inventory is tracked per store, and each sale or delivery order is linked to a specific store.

**Store list** — stores are displayed as cards, each showing the store name, abbreviation, address, and phone number.

**Adding or editing a store:**

1. Click **Add Store** (or the edit button on an existing store card).
2. Fill in:
   - **Name** (required) — the full name of the store or location.
   - **Note** — any internal notes.
   - **Address** — street address and phone number for this location.
3. Click **Save**.

To delete a store, open it and click the **Delete** button.

![Stores](https://raw.githubusercontent.com/loom21/loom21doc/main/images/stores-light.PNG)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

## Delivery Orders <a id="deliveries"></a>

Delivery orders record incoming stock from suppliers. Each delivery you confirm automatically increases the inventory of the received products in the selected store.

- **Create** a new delivery order with the **New** button.
- **Search** existing orders and open them with the purple arrow icon.

![Deliveries List](https://raw.githubusercontent.com/loom21/loom21doc/main/images/deliveries-list-light.PNG)

#### Delivery Order Details

**Order header fields** (left panel):
- **Order Number** — auto-generated reference, editable.
- **Order Date / Due Date** — when the order was created and when it is expected.
- **Supplier** — search and select the supplier for this delivery.
- **Store** — the destination store where received stock will be added.
- **Include Tax** — toggle whether tax is included in item prices.
- **Status** — track the delivery from Draft through to Delivered.
- **Note** — any internal remarks.

**Adding items:**
- Search for products by name and add them one at a time, or use **Select Items** to multi-select.
- Enter the quantity and unit price for each item received.
- The subtotal, VAT, and grand total are calculated automatically.

**Documents** — use the **Download** button to generate and download a PDF:
- Delivery invoice, receipt, or pickup list.

**Address** — the supplier's delivery address is populated automatically when you select a supplier. You can edit it per order if needed.

![Delivery Edit](https://raw.githubusercontent.com/loom21/loom21doc/main/images/delivery-edit-light.PNG)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

## Customers and Suppliers <a id="customers-suppliers"></a>
This page allows you to easily manage your customer database. Key features include:
- Search Customers: Quickly find customers by name using the search bar.
- Import Customers: Bring in customer data from external sources.
- Create or Edit Customers: Add new customers by pressing the blue button or modify existing customer details by clicking the purple arrow.

![Customers list](https://raw.githubusercontent.com/loom21/loom21doc/main/images/customers-light.PNG)
On this page, you can manage and update detailed information for each customer. The available fields include:

#### Customer Details
- **Name** — the customer's full company or person name.
- **Contact Name** — the specific person to address at that company.
- **Tax Number** — the customer's VAT or tax registration number, printed on invoices.
- **Note** — any internal notes about this customer.
- **Phone, Email, Website** — contact details.
- **Price List** — optionally assign one of your [Price Lists](#price-lists) to this customer. When set, all new sale orders for this customer automatically use that price list instead of the default one.
- **Multiple Addresses** — add and manage multiple delivery or billing addresses for the customer.

![Customer Edit](https://raw.githubusercontent.com/loom21/loom21doc/main/images/customer-edit-light.PNG)

#### Suppliers Management

Suppliers are managed in a dedicated **Suppliers** section accessible from the sidebar. The list view lets you search, import, export (CSV or JSON), and paginate through your supplier records.

**Supplier details** (when creating or editing):
- **Name** (required), **Contact Name**, **Tax Number**, **Note**
- **Phone**, **Email**, **Website**
- **Multiple Addresses** — add as many delivery addresses as needed.

The key distinction from customers is in their usage:
- **Suppliers** are selected when creating **Delivery Orders** (incoming stock).
- **Customers** are selected when creating **Sale Orders** (outgoing sales).

Unlike customer records, suppliers do not have a Price List assignment.

<p align="right">(<a href="#docs-top">back to top</a>)</p>

## User Profile<a id="user-profile"></a>

Click your name or the profile icon in the top navigation bar to access your **User Profile**. Here you can update your personal information independently of the organization-wide settings.

**Profile Information:**
- First Name, Last Name
- Email address
- Phone number
- Company Name
- Website

Click **Save** to apply any changes.

**Change Password** — a separate form at the bottom of the page:
1. Enter your **Current Password**.
2. Enter a **New Password** (minimum 8 characters).
3. Confirm the new password.
4. Click **Change**.

![User Profile](https://raw.githubusercontent.com/loom21/loom21doc/main/images/user-profile.png)

<p align="right">(<a href="#docs-top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

loom21 - [@loom21app](https://x.com/loom21app)

Project Link: [https://github.com/loom21/loom21doc](https://github.com/loom21/loom21doc)

<p align="right">(<a href="#docs-top">back to top</a>)</p>
