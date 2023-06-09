# Discover Ethiopia (EthioDiscovery)

  Backend for Flutter Mobile app 

  ## Installation


  1 . Move  to xampp dir called htdocs and create api folder

   ```bash
    cd /opt/lampp/htdocs
    mkdir api
    cd api
   ```

  2 . Clone the repo in the api dir

   ```bash
    git clone https://github.com/CSEC-ALPHA-WARRIORS/.git

   ```
  3 . Install XAMPP and start XAMPP server

   ```bash
    sudo /opt/lampp/lampp/ start
   ```

  4 . Create all tables in the server by run mysql.sql file in mysql local server 

   ## Usage

    -  base-url : http://localhost/api

   ## End Point


| endpoints             | Request Type | Headers | Body/ Param                                                  | Response                                                  | URL                         |
|-----------------------|--------------|---------|--------------------------------------------------------------|-----------------------------------------------------------|-----------------------------|
| CreateBookmark        | POST         |         | Body:{user_id,place_id,event_id}                             | {user_id,place_id,event_id}                               | /bookmark                   |
| GetBookmark           | GET          | {id}    |                                                              | {{id,user_id,place_id,event_id},}                         | /bookmark?id=?              |
| GetBookmark           | GET          |         |                                                              | [Bookmarks]                                               | /bookmarks                  |
| DeleteBookmark        | GET          | {id}    |                                                              | {"deleted id no ${id}"}                                   | /bookmark/delete            |
| CreateUser            | POST         |         | Body:{name,email,password,photo_url,role('Admin','User')}    | {name,email,password,photo_url,role('Admin','User')}      | /user                       |
| GetUserByid           | GET          | {id}    |                                                              | {id,name,email,password,photo_url,role('Admin','User')}   | /user?id=?                  |
| GetUser               | GET          |         |                                                              | {{name,email,password,photo_url,role('Admin','User')},}   | /user                       |
| UpdateUser            | POST         |         | Body:{id,name,email,password,photo_url,role('Admin','User')} | {name,email,password,photo_url,role('Admin','User')}      | /user/update                |
| DeleteUser            | GET          | {id}    |                                                              | {"deleted id no ${id}"}                                   | /user/delete                |
| CreateReview          | POST         |         | Body:{user_id,place_id,comment,rating}                       | {user_id,place_id,comment,rating}                         | /review                     |
| GetReviewByid         | GET          | {id}    |                                                              | {user_id,place_id,comment,rating}                         | /review?id=?                |
| GetReview             | GET          |         |                                                              | {{id,user_id,place_id,comment,rating}}                    | /review                     |
| UpdateReview          | POST         |         | Body:{id,comment,rating}                                     | {id,user_id,place_id,comment,rating}                      | /review/update              |
| DeleteReview          | GET          | {id}    |                                                              | {"deleted id no ${id}"}                                   | /review/delete?id=?         |
| CreateEvent           | POST         |         | Body:{title,latitude,longitude,start_date,end_date,price}    | {title,latitude,longitude,start_date,end_date,price}      | /event                      |
| GetEventByid          | GET          | {id}    |                                                              | {id,title,latitude,longitude,start_date,end_date,price}   | /event?id=?                 |
| GetReview             | GET          |         |                                                              | {{id,title,latitude,longitude,start_date,end_date,price}} | /event                      |
| UpdateEvent           | POST         |         | Body:{id,title,latitude,longitude,start_date,end_date,price} | {id,title,latitude,longitude,start_date,end_date,price}   | /event/update               |
| DeleteEvent           | GET          | {id}    |                                                              | {"deleted id no ${id}"}                                   | /event/delete?id=?          |
| CreatePlace           | POST         |         | Body:{title,latitude,longitude,region,distance}              | {title,latitude,longitude,region,distance}                | /place                      |
| GetPlaceByid          | GET          | {id}    |                                                              | Body:{id,title,latitude,longitude,region,distance}        | /place?id=?                 |
| GetPlace              | GET          |         |                                                              | {{id,title,latitude,longitude,region,distance}}           | /place                      |
| UpdatePlace           | POST         |         | Body:{id,title,latitude,longitude,region,distance}           | Body:{title,latitude,longitude,region,distance}           | /place/update               |
| DeletePlace           | GET          | {id}    |                                                              | {"deleted id no ${id}"}                                   | /place/delete?id=?          |
| CreateRecommendation  | POST         |         | Body:{place_id,name,pricing}                                 | {place_id,name,pricing}                                   | /recommendation             |
| GetRecommendationByid | GET          | {id}    |                                                              | {place_id,name,pricing}                                   | /recommendation?id=?        |
| GetRecommendation     | GET          |         |                                                              | {{place_id,name,pricing}}                                 | /recommendation             |
| UpdateRecommendation  | POST         |         | Body:{id,name,pricing}                                       | {id,place_id,name,pricing}                                | /recommendation/update      |
| DeleteRecommendation  | GET          | {id}    |                                                              | {"deleted id no ${id}"}                                   | /recommendation/delete?id=? |
| CreateDescription     | POST         |         | Body:{place_id,event_id,language,content}                    | {place_id,event_id,language,content}                      | /description                |
| GetDescriptionByid    | GET          | {id}    |                                                              | {id,place_id,event_id,language,content}                   | /description?id=?           |
| GetDescription        | GET          |         |                                                              | {{id,place_id,event_id,language,content}}                 | /description                |
| UpdateDescription     | POST         |         | Body:{id,place_id,event_id,language,content}                 | {id,place_id,event_id,language,content}                   | /description/update         |
| DeleteDescription     | GET          | {id}    |                                                              | {"deleted id no ${id}"}                                   | /description/delete?id=?    |
| CreatePhoto           | POST         |         | Body:{place_id,event_id,url}                                 | { place_id,event_id, url}                                 | /Photo                      |
| GetPhotoByid          | GET          | {id}    |                                                              | {id, place_id,event_id, url}                              | /Photo?id=?                 |
| GetPhoto              | GET          |         |                                                              | {{id, place_id,event_id, url}}                            | /Photo                      |
| UpdatePhoto           | POST         |         | Body:{id, url}                                               | {id, place_id,event_id, url}                              | /Photo/update               |
| DeletePhoto           | GET          | {id}    |                                                              | {"deleted id no ${id}"}                                   | /Photo/delete?id=?          |
| CreateCategory        | POST         |         | Body:{name,desc,cover_url}                                   | {name,desc,cover_url}                                     | /category                   |
| GetCategoryByid       | GET          | {id}    |                                                              | {id,name,desc,cover_url}                                  | /category?id=?              |
| GetCategory           | GET          |         |                                                              | {{id,name,desc,cover_url}}                                | /category                   |
| UpdateCategory        | POST         |         | Body:{id,name,desc,cover_url}                                | {name,desc,cover_url}                                     | /category                   |
| DeleteCategory        | GET          | {id}    |                                                              | {"deleted id no ${id}"}                                   | /category/delete?id=?       |
| CreateCategoryPlace   | POST         |         | Body:{category_id,place_id}                                  | {id,category_id,place_id}                                 | /categoryplace              |
| GetCategoryPlaceByid  | GET          | {id}    |                                                              | {id,category_id,place_id}                                 | /categoryplace?id=?         |
| GetCategoryPlace      | GET          |         | Body:{id,category_id,place_id}                               | {{id,category_id,place_id}}                               | /categoryplace              |
| DeleteCategoryPlace   | GET          | {id}    |                                                              | {"deleted id no ${id}"}                                   | /categoryplace?id=?         |