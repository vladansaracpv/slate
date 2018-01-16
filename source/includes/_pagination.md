
# Pagination
All search requests return paginated results. Each page holds up to 2000 elements.  Additionally, most of the resources that appear as lists in responses are returned as paginated results. Two types of paginations are available on the platform:

* Pagination for backend service
* Pagination for reporting service

When using pagination for APIs provided by backend service, page and size attributes could be used to request page number and number of elements per page. Please inspect [backend pagination object](#backendPaginationObject) for more details

When using pagination for APIs provided by reporting service -  *page, sort and pageSize (defaults to 25)* attributes could be used to request page number, sorting order and number of elements per page. 

Please inspect [reporting pagination object](#reportingPaginationObject) for more details



