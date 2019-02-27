==========
Spring-Data-XXX

Project SpringDataFundamental demonstrates the core features of Spring-Data-XXX family especially Spring-Data-JPA

* CrudReposiory (@Entity, @Table, @Id, @GeneratedValue, @Column, @ManyToOne, @OneToMany)
* JpaRepository (for bulk batch processing on repository)
* PagingAndSortingRepository
* ReadOnly Repository (@NoRepositoryBean)
* Query in Java Style (Selection Criteria, Order, Limit, etc)
* Query in SQL Style (@Query, Not Commonly Used)
* Query with Paging and Sorting (PagingAndSortingRepository, Pagable, PageRequest, Sort)
* Query DSL Extension (Dynamic Builder-like Queries)
* Query by Example (Not Commonly Used)
* Auditable and AbstractAuditable

==========
Spring-Data-REST

How to Enable Spring-Data-REST?
in project SpringDataFundamental, uncomment the spring-boot-starter-data-rest line in pom.xml dependency declaration.

The following additional features are offered by spring-data-rest on top of spring-data-jpa
* HATEOAS support (REST json responses are navigatable via hyperlinks, e.g. foreign key referenced object is navigatable with a link; when paging is enabled, first/last/previous/next page links are also available in the json responses)
* standard set of GET/POST/PUT/DELET opearations are supported on /xxx REST endpoints for each XxxRepository
* additional /xxx/search rest endpoint is automatically added
* paging and sorting (?size=10, ?page=5, ?sort=title, ?sort=title,asc)


for example, for a TourRepository, 
http://localhost:8080/tours?size=5&page=1&sort=title,asc
* sort all tours by title, in ascending order
* pagenate into 5 tours per page
* take the 2nd page

http://localhost:8080/tours/search/findByTourPackageCode?code=ABC&size=5&sort=title,asc
* find all tours by their associated TourPackages, those TourPackages with code ABC
* sort tours by title, and take the first 5 tours on the first page

Project SpringDataMongoDB demonstrates the features of Spring-Data-Mongodb