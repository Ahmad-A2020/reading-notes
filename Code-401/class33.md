#### Recourses: 
- [review: Intro to Serverless](https://hackernoon.com/what-is-serverless-architecture-what-are-its-pros-and-cons-cc4b804022e9)
- [review: AWS Amplify Kool-Aid](https://aws.amazon.com/amplify/)
- [GraphQL @connection section](https://docs.amplify.aws/cli/graphql-transformer/connection/)

#### [lab](https://github.com/Ahmad-A2020/taskmaster):
![lab33](C:\Users\Ahmad\asac\reading-notes\Code-401\ScreenShot\lab33-1.PNG)
![lab33](C:\Users\Ahmad\asac\reading-notes\Code-401\ScreenShot\lab33-2.PNG)

#### GraphQL @connection section: 
- **@connection:** The @connection directive enables you to specify relationships between @model types.
  - connections types: 
    - Has one:   In the simplest case, you can define a one-to-one connection, take the below example, on where a project has one team:
             type Project @model {
             id: ID!
             name: String
             team: Team @connection (fields: ["teamID"])
             }

             type Team @model {
             id: ID!
             name: String!
             }
    - Has many:     The following schema defines a Post that can have many comments:
            type Post @model {
             id: ID!
             title: String!
             comments: [Comment] @connection(keyName: "byPost", fields: ["id"])
             }

            type Comment @model
           @key(name: "byPost", fields: ["postID", "content"]) {
           id: ID!
           postID: ID!
           content: String!
           }
    - Many-to-many connections: You can implement many to many using two 1-M @connections, an @key, and a joining @model. For example:
           type Post @model {
           id: ID!
           title: String!
           editors: [PostEditor] @connection(keyName: "byPost", fields: ["id"])
           }

          type PostEditor
          @model(queries: null)
          @key(name: "byPost", fields: ["postID", "editorID"])
          @key(name: "byEditor", fields: ["editorID", "postID"]) {
          id: ID!
           postID: ID!
          editorID: ID!
          post: Post! @connection(fields: ["postID"])
          editor: User! @connection(fields: ["editorID"])
          }
  
    type User @model {
    id: ID!
    username: String!
    posts: [PostEditor] @connection(keyName: "byEditor", fields: ["id"])
    }