# PostgreSQL **Performance** TSG.
![](images\1.png)

When you are working on troubleshooting Performance for Azure database for PostgreSQL Please check the following:
## Steps to follow in order to troubleshoot performance issues in PostgreSQL:

1. Make sure the customer workload is not maxing out any of resource limits. 
2. Make sure the customer doesn't have [Query logging enabled](https://docs.microsoft.com/en-us/azure/postgresql/concepts-server-logs)
3. Make sure customer is applying application side best practices (connection pooling, accelerated networking)
4. If customer is complaining about slow connection to the database please read this:  New Connection Perfromance in PostgreSQL
5. Ask customer to [Analyze his entire database](https://www.postgresql.org/docs/9.1/sql-analyze.html) 
	
6. Ask customer to use Query Store:
	Query Store feature in Azure Database for PostgreSQL provides a way to track query performance over time. Query Store simplifies performance troubleshooting by helping you quickly find the longest running and most resource-intensive queries. Query Store automatically captures a history of queries and runtime statistics, and it retains them for your review. It separates data by time windows so that you can see database usage patterns. Data for all users, databases, and queries is stored in a database named azure_sys in the Azure Database for PostgreSQL instance.
	Learn more about Query store here.
	you can also view some usage scenario for Query Store and some Best Practices for Query Store.
	
7. [Query Performance Insight](https://docs.microsoft.com/en-us/azure/postgresql/concepts-query-performance-insight)
	Query Performance Insight helps you to quickly identify what your longest running queries are, how they change over time, and what waits are affecting them.
	
8. [Performance recommendations](https://docs.microsoft.com/en-us/azure/postgresql/concepts-performance-recommendations)
	Performance Recommendations feature analyses your databases to create customized suggestions for improved performance. To produce the recommendations, the analysis looks at various database characteristics including schema. Enable Query Store on your server to fully utilize the Performance Recommendations feature. After implementing any performance recommendation, you should test performance to evaluate the impact of those changes.


Feel free to refer your customers to the following [blog post](https://techcommunity.microsoft.com/t5/Azure-Database-for-PostgreSQL/Performance-Troubleshooting-Basics-on-Azure-Database-for/ba-p/819227)
	
## Related TSGs regarding Azure Database for PostgreSQL can be found as the following: 
1. [Running Processes](http://www.chrismiles.info/systemsadmin/databases/articles/viewing-current-postgresql-queries/)
2. [Update Statistics](https://www.postgresql.org/docs/9.1/sql-analyze.html)
3. PostgreSQL queries performance 
4. Testing PostgreSQL Performance
5. PostgreSQL Locks
6. Testing Postgres with OSTRESS
7. Query Store, Query Performance Insights, and Performance Recommendations
8. Query Store 
9. DTA - Database tuning advisor
10. Performance best practices for using Azure Database for PostgreSQL
11. Performance TSG/XTS Views
