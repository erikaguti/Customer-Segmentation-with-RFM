# Customer Segmentation based on Recency, Frequency, Monetary (RFM) Characteristics

In this notebook I take a dataset of 541,909 transactions spanning from 01/12/2010 and 09/12/2011 for a UK-based ecommerce business containing the following information:

- InvoiceNo: unique identifier of the transaction (each unique product purchased by a customer is a new transaction entry)
- StockCode: unique identifier of the product 
- Product Description
- Quantity: how many of the product were purchased
- InvoiceDate: date of the purchase
- UnitPrice: unit price of the product
- CustomerID: unique identifier of the customer
- Country: country associated with the customer

I first cleaned the data and created the following features associated with RFM per customer

**Recency**
- Number of Days Since Last Purchase
- Customer Duration (numbers of days between customers first purchase and last purchase)

**Frequency**
- Average Number of Times a Customer Purchases in a Month
- Average Number of Days in Between Purchases
- Average Number of Purchases per Week

**Monetary**
- Transaction Cost
- Average Spend Per Invoice By Customer
- Number of Invoices Per Customer
- Average Quantity Per Invoice

From these features I was able to group the 4,373 unique customers into 3 segements using the KMeans clustering algorithm. The profile of these segments are as follows:

- Segment 1: Customers with the highest ticket values but lowest frequency.
- Segment 2: Customers with the lowest ticket values but highest frequency.
- Segment 3: Customers with high ticket values and high frequency. Our best customers!
