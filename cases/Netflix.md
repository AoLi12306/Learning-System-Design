Reference:

[Mastering Chaos - A Netflix Guide to Microservices](https://www.youtube.com/watch?v=CZ3wIuvmHeM)


### Netflix DVD data center - 2000
HTTPS -> Load Balance --(http)-->  Linux Hosts

each Linux Host contains "Appach -> Tomcat(Java Web)"

Tomcat --(JDBC)--> Database STORE

this Database store inter connect with othe databse using "database link"


Problem:
- Monolithic code base: everyone contribute to same codes, if problem haapen, very hard to debug
- Monolithic database: every holiday, find bigger hardware to vertically scale
- Tightly coupled architect: all schema is binded, codes directly call to database, many applications directly reference to table schemas and add a column to a table is a big cross-functioanl project.


### Microservices

- Define: