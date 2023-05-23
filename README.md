# Linkody_Test

# Test Description : 

We need a simple Symfony application that allows users to import URLs from a CSV file.
The application consist of just one form to select the CSV file. The URLs are inserted into a MySQL table. 

Before inserting the URLs, we want to check if they are already in the table so we don’t insert duplicates. After the form is submitted we inform the user how many URLs have been added to the table.

The table is stored in MySQL with the InnoDB engine, the Dynamic row format, and the utf8mb4 character set. With this setting, MySQL has an index key prefix length limit of 3072 bytes.

We have 3 additional requirements:

1/ The table can grow to millions of URLs. However, we can’t have the user wait more than a couple of seconds for inserting CSV files with tens of thousands of URLs. What are the usual approaches?

2/ The URLs can be up to 2048 characters. What problem are we facing? How to solve that problem?

3/ We want all versions of the same URL to match. For instance, if 2 URLs differ only by the scheme, they are considered the same URL. If one URL has the default port 80 and another has no port, they are considered the same URL. If the URLs have the same query parameters and values but in different orders, they are considered the same URL.
Note: you don’t have to implement all conditions of this constraint. Just show that you understand what is required.

Implement a mini Symfony application taking into consideration the 3 previous constraints.
