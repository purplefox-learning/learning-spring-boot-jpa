
Once the application is started, POST to http://localhost:8080/tours/1/ratings with a few ratings like this
{
    "score": 3,
    "comment": "I thought it was good",
    "customerId": 1
}

then see the results at
http://localhost:8080/tours/1/ratings
http://localhost:8080/tours/1/ratings?size=3&page=1&sort=score,asc