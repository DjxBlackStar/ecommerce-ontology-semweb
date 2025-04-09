📚 Domain Chosen: E-commerce

We selected E-commerce as the domain for this semantic web mini-project because it is highly structured and commonly used in real-world applications. The e-commerce ecosystem involves various entities such as products, sellers, buyers, orders, payments, and reviews—all of which can be clearly defined and interlinked using semantic web technologies.

Modeling this domain with ontologies enables:

* Better interoperability between systems

* Improved product search and recommendation

* Clearer understanding of customer behaviors and preferences

* Intelligent querying of e-commerce data

* This ontology can be useful for:

* Developers building smart e-commerce platforms

* Businesses aiming to analyze and organize product data

* Researchers working on semantic web and data integration

✅ Key Concepts and Relationships
Here’s a suggestion for how you might model the core of your ontology:

🎓 Main Classes
- Product

- Customer

- Order

- Seller

- Review

- Category

- Payment

🔗 Object Properties

* purchasedBy → links Order to Customer

* soldBy → links Product to Seller

* hasCategory → links Product to Category

* includesProduct → links Order to Product

* hasReview → links Product to Review

🧮 Data Properties

* hasPrice (float)

* hasRating (integer or float)

* hasDate (date)

* hasEmail (for Customer or Seller)

* hasQuantity (integer)

* productName (string)
