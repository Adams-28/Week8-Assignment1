# Week 8 Assignment 1

##  Queries Explanations (Queries can be found on the ProductsRunner.java file ) 

**-Finds all products of a specific category:**  

System.out.println("Soda products: " + repo.findByCategory("Soda"));

**-Finds all products that cost less than the specified price:**  

System.out.println("Products less than 4 dollars: " + repo.findByPriceLessThan(4));

**-Finds all products that are no longer in stock:**  

@Query("SELECT p FROM Product p WHERE p.stockQuantity = 0")
System.out.println("We no longer have the following items in stock: " + repo.findByStockQuantity());

**-Finds the average price of products in each category:**  

for (Object[] row : repo.priceAverageByCategory()) {
    System.out.println("Average price of " + row[0] + ": " + row[1]);
}
