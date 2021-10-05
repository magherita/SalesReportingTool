# Sales Reporting Tool
This is an API system to help us record the sales that are made for our products.

The solution is built with using ASP.NET Web API and currently has 2 functions, namely:
    * Uploading of Sales from a CSV file
    * Fetching all Sales from the database

Both of these are currently found in the `SalesController`.


# Challenge
Task is to improve the existing solution to address some of the challenges that have been identified
1. Restructure the domain (the Sales class) to make it more relational. Identify properties that can be moved into their own entities.

2. Implement the following endpoints to query for data from the database. 
    * An endpoint to show the top profitable itemTypes. One can also specify the top number of itemTypes they would like to view. If not specified then only the top **5** profitable items should be returned. Besides the itemTypes, the endpoint should also return the total units sold, total profit, total revenue and total revenue for each itemType. 
    * And endpoint to return the total profit made. 

    Each of the above endpoints should the relevant include query parameters. The query parameters should be optional but when specified should filter the data accordingly. The parameters to be included **the Order date range** and **one or more countries**.

3. The current implementation of Get all fetches all the data from the database. At the moment this query gets too long for us to fetch the data. Re-design the endpoint and the underlying logic to address this issue using the best practices. Ensure that the Swagger documentation is descriptive enough to be used by consumed.

# Hints
- Refer to the csv file uploaded in the `/Files` get an understanding of the data we are working with. 
- You are at liberty to re-structure the code base as well as include any relevant classes as fit in order to make the code readable and maintainable. Be sure to defend the basis upon which the code 
- Do not use external libraries except those natively provided by the framework.
- Even though we would like to see your solution run with successful results, that is not necessary the end goal. We are looking for code that;
    - Follows best practices and design patterns.
    - Is readable
    - Maintainable

- We would like to see unit tests written on the business logic. Of particular interest are the tests on the logic and not the controllers and the ORM. 
