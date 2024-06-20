## Security Strategy conforms to OWASP recommandations (and ANSSI)


### Broken Access Control 

It permits user to access unauthorize ressource

how to prevent it? 

1. Creating a RBAC (Role Base Access Control). Table which describes all functionnality by type of user on the application. What each user can or can't do. 
2. Principle of least privilege. Every user should have the rights to do their tasks and no more.Example: No user root for everyone, No all CRUD for all. 
3. Having one access control mechanism and re-use it through the application. 
4. Minimize CORS. 
5. Verify the owner of the resource. Example: having a foreign key in every resource to ensure the user get its own resources and not others. 
6. Match business limits to application. Exemple: In Database, change the limits of relations. 0,N -> 0,2. Control the existence or relation before actions insert/update/delete/select. 
7. Control over metadata 
8. Authentication 