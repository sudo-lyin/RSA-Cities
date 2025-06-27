# 🇿🇦 RSA Cities Database (SQL Script)

This repository contains a complete SQL Server script for setting up a normalized schema of countries, provinces, and cities, with a  focus on major South African Cities.

## 📂 Structure

- **Schema**: `address`
- **Tables**:
  - `country`: All ISO 3166-1 alpha-3 country codes
  - `region`: South African provinces (linked to country)
  - `city`: Cities and towns with unique city IDs (linked to region)

## 🛠️ How to Use

### ⚙️ Requirements

- Microsoft SQL Server (2016+ or Azure SQL)
- SQL Server Management Studio (SSMS) or Azure Data Studio
- Permissions to create schemas and run insert scripts

---

### 📥 Step-by-Step

1. Clone the repo:
   ```bash
   git clone https://github.com/sudo-lyin/RSA-Cities
   cd rsa-cities-database
   ```

2. Open the SQL script:
   - Launch **SSMS** or **Azure Data Studio**
   - Load `RSA-Cities.sql`

3. Connect to your SQL Server instance:
   - Make sure you are connected to a database where you have `CREATE SCHEMA` and `INSERT` privileges

4. Run the script:
   - Execute the entire `RSA-Cities.sql` file
   - This will:
     - Create a schema named `address`
     - Create 3 tables: `country`, `region`, and `city`
     - Insert ISO country codes, South African provinces, and cities/towns

5. Verify the data:
   ```sql
   SELECT * FROM address.country;
   SELECT * FROM address.region;
   SELECT * FROM address.city WHERE RegionID = 'ZAF-GAU'; -- Gauteng cities
   ```

---

### 💡 Example Use Cases

- Integrate into CRM or ERP systems for address validation
- Use in dropdown selectors for web/mobile address forms
- Reference in municipal, GIS, or reporting tools
- Extendable to include ZIP/postal codes or geo-coordinates



