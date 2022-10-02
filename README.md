# gql-server-3
Another Simple GraphQL API Server Built With NodeJS and Express.


I am following [this tutorial](https://dev.to/codesphere/how-to-build-a-graphql-server-with-nodejs-and-express-2g8j).

Queries that can be used:
```
query getSingleImage($imageId: Int!) {
  image(id: $imageId) {
    title
    category
  }
}

query getImagesByCategory($imageCat: String) {
  images(category: $imageCat) {
    id
    title
    category
  }
}

```

Parameters:
```
{
  "imageId": 1,
  "imageCat": "Coffee"
}
```

Results:
```
{
  "data": {
    "images": [
      {
        "id": 2,
        "title": "Shallow focus photography of Cafe Latte",
        "category": "Coffee"
      },
      {
        "id": 4,
        "title": "Beverage breakfast brewed coffee caffeine",
        "category": "Coffee"
      }
    ]
  }
}
```