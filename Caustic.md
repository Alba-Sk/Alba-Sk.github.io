
## 💰  Caustic Soda- Chemical Rate APP


Streamlit-based pricing tool for calculating chemical product costs across multiple units of measure (UOM), delivery locations, and services like pumping.

This tool allows users to easily calculate freight-inclusive pricing for chemicals using flexible inputs and provides a detailed breakdown of all costs — including material, freight, tote, pumping, and labor.

### 🚀 Features

  * Supports multiple UOMs (Pound, Kg, Liter, IBC, DST, LMT)
  * Delivery date & location-based pricing
  * Freight allocation based on weight and truck count (Full truck FL, Less truck load LTL)
  * Optional pumping & labor costs
  * IBC-specific pricing including tote return scenarios
  * Expandable breakdown of price components in the UI
  * Submit Order from the customer
  * Get the Order request in Goodle Sheet

<img width="488" height="461" alt="image" src="https://github.com/user-attachments/assets/937d6e84-a78c-4658-b9b9-00f9ad3f3e53" />



### 🧮  How the Pricing Works 

🔹 General Workflow User selects:

  * Delivery date
  * Destination
  * Quantity
  * Unit of Measure (UOM) — Pound, KG, Liter, IBC, DST, LMT, etc.
  * Pumping service option
  * Internally:
      -  Quantity is normalized to pounds for pricing consistency
      -  Pricing logic branches depending on UOM
      -  Special handling for IBC, DST, and LMT
      -  Pumping and labor costs are conditionally added
      -  Freight is allocated per pound and truck



## Results:

Total price per unit

Submit Order request to the company

Detailed cost breakdown (Material, Freight, Tote, Pumping, Labor)

<img width="599" height="257" alt="image" src="https://github.com/user-attachments/assets/081c9ab4-c93c-4e94-8069-9f20b0e35f87" />


<img width="716" height="883" alt="caustic app 08 17 2025" src="https://github.com/user-attachments/assets/305b61a6-3d36-4430-8900-d5a854379f0d" />

