# GraphQLExample
Testing GraphQL, mySQL to GraphQL

# Tesing

- Run `node Basic_Server.js`
- Open `http://localhost:4000/graphql`

## Basic_Server.js
- Type
    ```
    query getCourseWithFragments($courseID1: Int!, $courseID2: Int!) {
          course1: course(id: $courseID1) {
                 ...courseFields
          },
          course2: course(id: $courseID2) {
                ...courseFields
          } 
    }
    
    //use fragment to re-use code
    fragment courseFields on Course {
      title
      author
      description
      topic
      url
    }
    ```
- In Query Variables area
    ```
    { 
    "courseID1":1,
    "courseID2":2
    }
    ```
- Press `Run`

## mySQL_to_GraphQL_Server.js
- Type
  ```
  {
    getGame(gameName: "Agricola") {
      getDesc
      getImage
    }
  }
  ```
- Press `Run`
