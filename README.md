# Week 8 Assignment 1: Implementing Repositories and Defining Queries

##  Queries Explanations: (Queries can be found on the ProductsRunner.java file ) 

**1. Finds all products of a specific category:**  

System.out.println("Soda products: " + repo.findByCategory("Soda"));

**2. Finds all products that cost less than the specified price:**  

System.out.println("Products less than 4 dollars: " + repo.findByPriceLessThan(4));

**3. Finds all products that are no longer in stock:**  

@Query("SELECT p FROM Product p WHERE p.stockQuantity = 0")
System.out.println("We no longer have the following items in stock: " + repo.findByStockQuantity());

**4. Finds the average price of products in each category:**  

for (Object[] row : repo.priceAverageByCategory()) {
    System.out.println("Average price of " + row[0] + ": " + row[1]);
}
