# eCommerce Graph Analytics: Product Recommendation Using Graph Algorithms

**Graduate Team Project**  
**Master of Information and Data Science**  
**University of California, Berkeley**

**Chase Foster**
---

## Overview

This project explores how graph databases and graph algorithms can improve product recommendation systems in e-commerce. Using an Amazon product dataset, we modeled relationships between users and products as a graph and applied graph algorithms to identify influential products, discover communities of related products, and generate recommendation opportunities.

Rather than relying on traditional relational databases, this project demonstrates how graph-based approaches better capture complex relationships between customers and products, enabling more effective recommendations, cross-selling, and product bundling strategies.

---

## Business Problem

Modern e-commerce platforms depend heavily on recommendation systems.

Traditional relational databases can efficiently store transactional data but often struggle to model complex relationships between products and customers due to expensive joins and limited relationship visibility.

Graph databases provide a natural way to represent these connections and enable algorithms that reveal hidden relationships within customer purchasing behavior.

---

## Project Objectives

The goals of this project were to:

- Build a graph representation of customer-product relationships.
- Identify influential products using graph analytics.
- Discover groups of similar products.
- Generate product recommendations using graph algorithms.
- Compare graph databases with alternative NoSQL technologies for e-commerce analytics.

---

## Dataset

### Source

- Amazon Sales Dataset (Kaggle)

### Data Summary

The dataset contains over 1,000 Amazon product records, including:

- Product information
- Customer ratings
- Product reviews

These records were transformed into a graph where:

- **Nodes:** Users and Products
- **Edges:** Customer review relationships and co-reviewed products
- **Edge Weights:** Frequency of shared reviewers between products

---

## Graph Design

The graph consisted of:

### Nodes

- Users
- Products

### Relationships

- **REVIEWED**
  - Connects users to products they reviewed.

- **CO_REVIEWED**
  - Connects products reviewed by the same users.

Edge weights represent the strength of the relationship based on how frequently products were reviewed together.

---

## Graph Algorithms

Several graph algorithms were implemented to analyze the product network.

### PageRank

Used to identify the most influential products within the network.

### Louvain Community Detection

Detected groups of highly connected products that may represent natural purchasing communities or bundle opportunities.

### Node Similarity

Measured similarity between products to generate recommendation candidates based on shared customer behavior.

---

## Key Findings

The graph-based approach successfully revealed hidden relationships among products.

Major findings included:

- Identification of highly influential products using PageRank.
- Discovery of natural product communities through Louvain clustering.
- Generation of product recommendations using node similarity.
- Demonstration that graph analytics supports recommendation systems, cross-selling, and product bundling more effectively than traditional relational approaches for highly connected data.

---

## Comparison with Other NoSQL Databases

The project also evaluated alternative database technologies.

### MongoDB

Strengths:

- Flexible document storage
- Well suited for review text and semi-structured data
- Easy integration with downstream machine learning workflows

Limitations:

- Limited support for relationship-based analytics and recommendation chains.

---

### Redis

Strengths:

- Extremely fast retrieval
- Real-time dashboard support
- Efficient caching

Limitations:

- Memory constraints
- Less suitable for long-term historical analysis
- Cannot efficiently model complex graph relationships. :contentReference[oaicite:6]{index=6}

---

## Technologies Used

### Programming

- Python

### Graph Database

- Neo4j

### Libraries

- pandas
- Neo4j Graph Data Science Library

---

## Repository Structure

```
ecommerce-graph-analytics/

│── README.md
│── LICENSE
│── .gitignore

├── code/
│   Analysis notebook

├── data/
│   Dataset

├── graphs/
│   Graph visualizations

└── presentation/
│   Final presentation slides
```

---

## My Contributions

This project was completed as part of a graduate team in the UC Berkeley Master of Information and Data Science program.

My contributions included:

- Graph modeling and database design
- Query development
- Graph algorithm implementation
- Visualization of graph structures
- Interpretation of graph analytics results
- Preparation of the final presentation

---

## Skills Demonstrated

- Graph Databases
- Neo4j
- Graph Algorithms
- Recommendation Systems
- Network Analysis
- Data Modeling
- Data Visualization
- Python
- Team Collaboration

---

## Future Work

Potential future extensions include:

- Incorporating purchase history alongside reviews.
- Building personalized recommendation models.
- Scaling the graph to millions of products.
- Integrating graph embeddings for machine learning applications.
- Deploying a real-time recommendation engine using graph analytics.

---

## Acknowledgments

This project was completed as part of the Master of Information and Data Science program at the University of California, Berkeley.

Special thanks to my teammates for their collaboration throughout the project.

---

## Contact

Feel free to connect with me on LinkedIn or reach out via email if you have questions about this project.
