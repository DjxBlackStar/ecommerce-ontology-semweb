# 🛍️ E-Commerce Ontology - Semantic Web Mini Project

## 📚 Domain Chosen: E-commerce

We selected **E-commerce** as the domain for this semantic web mini-project because it is highly structured and commonly used in real-world applications. The e-commerce ecosystem involves various entities such as products, sellers, buyers, orders, payments, and reviews—all of which can be clearly defined and interlinked using semantic web technologies.

### 🔍 Why E-commerce?

Modeling this domain with ontologies enables:
- Better interoperability between systems
- Improved product search and recommendation
- Clearer understanding of customer behaviors and preferences
- Intelligent querying of e-commerce data

This ontology can be useful for:
- Developers building smart e-commerce platforms
- Businesses aiming to analyze and organize product data
- Researchers working on semantic web and data integration

---

## 🧠 Model Overview

### 🎓 Classes (Concepts)
- `Product`
- `Customer`
- `Order`
- `Seller`
- `Review`
- `Category`
- `Payment`

### 🔗 Object Properties
| Property         | Domain     | Range     | Description                                |
|------------------|------------|-----------|--------------------------------------------|
| `purchasedBy`    | Order      | Customer  | Links an order to the customer who placed it |
| `soldBy`         | Product    | Seller    | Links a product to the seller              |
| `hasCategory`    | Product    | Category  | Specifies the category of the product      |
| `includesProduct`| Order      | Product   | Indicates products included in an order    |
| `hasReview`      | Product    | Review    | Links a product to its reviews             |

### 🧮 Data Properties
| Property        | Domain     | Range       | Description                                 |
|-----------------|------------|-------------|---------------------------------------------|
| `hasPrice`      | Product    | xsd:float   | Price of a product                          |
| `hasRating`     | Review     | xsd:float   | Numeric rating given in a review            |
| `hasDate`       | Order/Review| xsd:date   | Date of order or review                     |
| `hasEmail`      | Customer/Seller | xsd:string | Email of a customer or seller           |
| `hasQuantity`   | Order      | xsd:int     | Quantity of a product in the order          |
| `productName`   | Product    | xsd:string  | Name of the product                         |

---

## 🧩 Namespaces Used

We will use standard semantic web namespaces, including:

- `rdf`: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
- `rdfs`: <http://www.w3.org/2000/01/rdf-schema#>
- `xsd`: <http://www.w3.org/2001/XMLSchema#>
- `owl`: <http://www.w3.org/2002/07/owl#>
- `foaf`: <http://xmlns.com/foaf/0.1/>
- `dc`: <http://purl.org/dc/elements/1.1/>

---

## ⚙️ Project Phases

| Phase           | Description |
|----------------|-------------|
| ✅ Phase 1      | Choose the domain and define key concepts |
| 🔜 Phase 2      | Model the domain in RDF/RDFS using Protégé |
| 🔜 Phase 3      | Interrogate the ontology with SPARQL queries |
| 🔜 Phase 4      | Extend and formalize the ontology using OWL |
| 🔜 Phase 5      | Define reasoning rules using SWRL |

---

## 🗂️ Project Structure
 ecommerce-ontology-semweb ├── ontology/ │ ├── ecommerce.owl │ └── ecommerce.rdf ├── queries/ │ └── sparql_queries.rq ├── rules/ │ └── swrl_rules.txt ├── README.md
 
---

## ✨ Conclusion

This project demonstrates how semantic web technologies like RDF, RDFS, OWL, SPARQL, and SWRL can be applied to the domain of E-commerce. The ontology provides a structured way to describe e-commerce entities and their relationships, enabling powerful querying, reasoning, and data integration across platforms.

---

## 🧑‍💻 Authors
- Med Salim Gharsellaoui & Nour Abed


