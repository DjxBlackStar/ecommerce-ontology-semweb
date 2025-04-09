# 🛍️ E-Commerce Ontology - Semantic Web Mini Project

## 📚 Domain Chosen: E-commerce

We selected **E-commerce** as the domain for this semantic web mini-project because it is highly structured and commonly used in real-world applications. The e-commerce ecosystem involves various entities such as products, sellers, buyers, orders, payments, and reviews—all of which can be clearly defined and interlinked using semantic web technologies.

### 🔍 Why E-commerce?

Modeling this domain with ontologies enables:
- Better interoperability between different e-commerce systems
- Improved product search and recommendation mechanisms
- Clearer understanding of customer behaviors and preferences
- Intelligent querying of e-commerce data across platforms

This ontology can be useful for:
- Developers building smart e-commerce platforms
- Businesses aiming to analyze and organize product data
- Researchers working on semantic web and data integration
- Market analysts studying consumer behavior patterns

---

## 🧠 Model Overview

### 🎓 Classes and Subclasses

**Main Classes:**
- `Product`
  - `PhysicalProduct` (subclass)
  - `DigitalProduct` (subclass)
- `Customer`
  - `RegisteredCustomer` (subclass)
  - `GuestCustomer` (subclass)
- `Order`
  - `CompletedOrder` (subclass)
  - `PendingOrder` (subclass)
  - `CanceledOrder` (subclass)
- `Seller`
  - `IndividualSeller` (subclass)
  - `CompanySeller` (subclass)
- `Review`
  - `VerifiedPurchaseReview` (subclass)
  - `UnverifiedReview` (subclass)
- `Category`
  - `Electronics` (subclass)
  - `Fashion` (subclass)
  - `Books` (subclass)
  - `HomeAppliances` (subclass)
  - `Toys` (subclass)
- `Payment`
  - `CreditCardPayment` (subclass)
  - `BankTransferPayment` (subclass)
  - `DigitalWalletPayment` (subclass)
- `Address`

### 🔗 Object Properties
| Property         | Domain     | Range     | Description                                |
|------------------|------------|-----------|--------------------------------------------|
| `purchasedBy`    | Order      | Customer  | Links an order to the customer who placed it |
| `soldBy`         | Product    | Seller    | Links a product to the seller              |
| `hasCategory`    | Product    | Category  | Specifies the category of the product      |
| `includesProduct`| Order      | Product   | Indicates products included in an order    |
| `hasReview`      | Product    | Review    | Links a product to its reviews             |
| `writtenBy`      | Review     | Customer  | Links a review to the customer who wrote it |
| `processedWith`  | Order      | Payment   | Links an order to its payment method       |
| `shippedTo`      | Order      | Address   | Links an order to a shipping address       |

### 🧮 Data Properties
| Property        | Domain     | Range       | Description                                 |
|-----------------|------------|-------------|---------------------------------------------|
| `hasPrice`      | Product    | xsd:float   | Price of a product                          |
| `hasRating`     | Review     | xsd:float   | Numeric rating given in a review            |
| `hasDate`       | Order/Review| xsd:date   | Date of order or review                     |
| `hasEmail`      | Customer/Seller | xsd:string | Email of a customer or seller           |
| `hasQuantity`   | Order      | xsd:int     | Quantity of a product in the order          |
| `productName`   | Product    | xsd:string  | Name of the product                         |
| `description`   | Product    | xsd:string  | Detailed description of the product         |
| `hasPhone`      | Customer/Seller | xsd:string | Phone number                            |
| `hasDiscount`   | Product    | xsd:float   | Discount percentage on a product            |
| `hasWeight`     | PhysicalProduct | xsd:float | Weight of a physical product             |

---

## 🖼️ Conceptual Model Diagram

```
[A diagram will be created using Protégé or draw.io showing the relationships 
between the main classes of our e-commerce ontology]
```

---

## 🧩 Namespaces Used and Justification

| Namespace | URI                                    | Justification                           |
|-----------|----------------------------------------|----------------------------------------|
| `rdf`     | <http://www.w3.org/1999/02/22-rdf-syntax-ns#> | Foundation for creating RDF triples |
| `rdfs`    | <http://www.w3.org/2000/01/rdf-schema#> | Provides vocabulary for describing RDF resources |
| `xsd`     | <http://www.w3.org/2001/XMLSchema#>    | Defines data types for property values  |
| `owl`     | <http://www.w3.org/2002/07/owl#>       | Extends RDF/RDFS with additional expressivity |
| `foaf`    | <http://xmlns.com/foaf/0.1/>           | Used for representing people and their social connections |
| `dc`      | <http://purl.org/dc/elements/1.1/>     | Used for metadata elements like title, creator, date |
| `schema`  | <http://schema.org/>                   | Provides vocabulary for products and commercial entities |
| `vcard`   | <http://schema.org/](http://www.w3.org/2001/vcard-rdf/3.0#>| If your ontology includes contact information for individuals, vCard can be used. |
| `skos`   | <http://www.w3.org/2004/02/skos/core#>| Useful for modeling controlled vocabularies, taxonomies, and classifications. This could help in product categories. |
| `ecomm`   | <http://www.semanticweb.org/ecommerce#>| Our custom namespace for e-commerce specific concepts |

---

## 📝 Planned SPARQL Query Examples

Our ontology will support complex queries such as:

1. Find all products in a specific category with ratings above 4.0
2. Identify customers who have purchased more than 5 items in the last month
3. List the top-selling products across all categories
4. Find all reviews written by verified purchasers of a specific product
5. Identify patterns between product categories and customer demographics

---

## 🧠 Planned SWRL Rules

We plan to implement rules such as:

1. If a customer makes purchases exceeding $1000, classify them as a "PremiumCustomer"
2. If a product has more than 10 five-star reviews, mark it as "HighlyRated"
3. If an order remains in "Processing" status for more than 7 days, flag it for review
4. If a customer regularly purchases products from a specific category, suggest related products

---

## ⚙️ Project Development Plan

| Phase | Description | Tools & Methods | Expected Outcome |
|-------|-------------|----------------|------------------|
| ✅ Phase 1 | Choose domain & define concepts | Conceptual modeling, GitHub setup | Clear domain definition and project structure |
| 🔜 Phase 2 | Model in RDF/RDFS | Protégé, RDF Validator | Valid RDF/RDFS ontology with basic concepts and relationships |
| 🔜 Phase 3 | Create SPARQL queries | Apache Jena, SPARQL endpoint | Set of meaningful queries that extract valuable information |
| 🔜 Phase 4 | Extend with OWL | Protégé, OWL reasoners | Enhanced ontology with richer semantics and inference capabilities |
| 🔜 Phase 5 | Define SWRL rules | Protégé SWRL Tab, Drools | Rules that enable advanced reasoning and automated classification |

---

## 🗂️ Project Structure

```
ecommerce-ontology-semweb/
├── ontology/
│   ├── ecommerce.owl
│   └── ecommerce.rdf
├── queries/
│   └── sparql_queries.rq
├── rules/
│   └── swrl_rules.txt
├── diagrams/
│   └── conceptual_model.png
├── data/
│   └── sample_instances.ttl
├── README.md
└── LICENCE
```

---

## 🔍 Case Studies and Use Cases

Our ontology will support the following concrete use cases:

1. **Product Recommendation System**
   - Suggesting products based on customer purchase history and browsing behavior

2. **Intelligent Search**
   - Enabling semantic search across product categories and attributes

3. **Customer Segmentation**
   - Classifying customers based on purchase patterns for targeted marketing

4. **Inventory Management**
   - Tracking product availability and predicting restocking needs

5. **Review Analysis**
   - Extracting insights from customer reviews to improve products and services

---

## ✨ Conclusion

This project demonstrates how semantic web technologies like RDF, RDFS, OWL, SPARQL, and SWRL can be applied to the domain of E-commerce. The ontology provides a structured way to describe e-commerce entities and their relationships, enabling powerful querying, reasoning, and data integration across platforms.

---

## 🧑‍💻 Authors
- Med Salim Gharsellaoui & Nour Abed
