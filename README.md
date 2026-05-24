# 📊 MongoDB Data Modeling Practice: Optical Store – Glasses UI (Óptica Cul d'Ampolla)

## 📌 Description

The objective of this project is to design a NoSQL data model using MongoDB based on a real-world business scenario, focusing on a different perspective of the same system.

In this case, the data model is centered on the **glasses (gafas)** as the main entity, instead of the client.

The model is built by analyzing a user interface where detailed information about a specific pair of glasses is displayed, along with the list of clients who have purchased them.

The focus is on adapting the structure to optimize read access from a product-oriented perspective, following MongoDB best practices such as embedded documents and arrays.


## 🛠 Technologies

- MongoDB (Compass)
- JSON
- Draw.io (for database diagram)

## 📂 Project Structure

MongoDB-estructura/

`OpticGafasUI.json` → MongoDB document structure  
`opticGafasUISchema.png` → Data model diagram  
`README.md` → Project documentation  

## 🧠 What was Practiced

### 🔹 NoSQL Data Modeling

- Designing a database based on a different UI perspective  
- Transitioning from client-centered to product-centered modeling  
- Understanding how document structure changes depending on access patterns  

### 🔹 Embedded Documents

- Use of nested objects for:
  - Frame (montura)  
  - Provider (proveedor)  
  - Provider address  

### 🔹 Arrays

- Implementation of arrays to represent:
  - Clients who purchased the glasses (`comprado_por`)  

### 🔹 Relationships in MongoDB

- **1:N relationship using arrays**:
  - Gafas → Clientes  

- **1:1 embedded relationships**:
  - Gafas → Proveedor  

### 🔹 Data Organization

- Structuring data around the main entity shown in the UI (glasses)  
- Avoiding unnecessary attributes not visible in the interface  
- Optimizing the model for fast product-based queries  

## 📈 Design Approach

The model follows a **UI-driven design approach**, where:

- The main document represents the entity displayed on screen (glasses)  
- Related data (provider and clients) is embedded within the document  
- Only relevant attributes from the interface are included  

The model prioritizes simplicity and direct access to information.

## 🔗 Key Design Decisions

- ✅ One document per glasses item  
- ✅ Provider stored as an embedded document  
- ✅ Clients stored as an array  
- ✅ No unnecessary attributes included (e.g. graduation, employee, or purchase date)  
- ✅ Structure strictly aligned with the UI  

## 🚀 How to Use

1. Open MongoDB Compass  
2. Create database: `bottleBottomOptic`  
3. Create collection: `gafas`  
4. Import file: `opticaGafasUIData.json`  
5. Explore the data  


