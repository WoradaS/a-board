## A Board (Next.js + NestJS)

Web board for employees to ask questions and express their opinions.

## Application Architecture.

![](https://github.com/WoradaS/the-sale-campaign/blob/main/preview/architecture.png)
![](/preview/architecture.png)

## Project Screen Shot(s) and Video

case: sign-in

![sign-in.gif](https://github.com/WoradaS/the-sale-campaign/blob/main/preview/sign-in.gif)

case: board

![board.gif](https://github.com/WoradaS/the-sale-campaign/blob/main/preview/board.gif)

case: create update and delete blog

![create-update-delete.gif](https://github.com/WoradaS/the-sale-campaign/blob/main/preview/create-update-delete.gif)

case: comments

![comment.gif](https://github.com/WoradaS/the-sale-campaign/blob/main/preview/comments.gif)

## Libraries and Packages

### FrontEnd

- **chakra-ui**: Chakra UI is a React component library that helps developers create accessible, responsive, and customizable user interfaces quickly. It offers pre-designed components, a flexible theming system, and strong TypeScript support.

- **mui/material**: a React component library based on Material Design, providing customizable UI components for building modern web applications.

- **axios**: Axios is a JavaScript library for making HTTP requests, commonly used in frontend and backend applications to interact with APIs and web servers.

### BackEnd

- **sqlite3**: SQLite3 is a lightweight, serverless SQL database engine popular for embedded systems, mobile apps, and small to medium-sized projects due to its simplicity and efficiency.

- **typeorm**: TypeORM is an Object-Relational Mapping library for TypeScript and JavaScript, facilitating database interactions through object-oriented programming techniques.

- **jest**: Jest is a JavaScript testing framework known for its simplicity, speed, and zero-config setup. It's widely used for testing JavaScript code, including React applications, and offers features like assertions, mocking, and code coverage analysis.

## Installation and Setup Instructions

### FrontEnd

#### Installation

```bash
# go to the directory
$ cd a-board-ui/

# install packages
$ yarn install

```

#### Running the app

```bash
# development
yarn dev

```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

### BackEnd

#### Installation

```bash
# go to the directory
$ cd a-board-api/

# install packages
$ yarn install

```
#### Installation Extensions In VSCode
![SQLite](a-board-api/asset/SQLite.png)

#### Running the app
```bash
# development
$ yarn run start

# watch mode
$ yarn run start:dev

# production mode
$ yarn run start:prod
```
To Visit App:
Open [http://localhost:5000](http://localhost:5000) with your browser to see the result.

## API Document

Method |API Path | Params | Query | Body | Response
----- | ----- | ----- | ----- | ----- | ----- |
POST | user | - | - | - |Response |
GET | user:id | id: string | - |{"username": "Sam"}| {"id": 1, "username": "Worada"} |
GET | blog:blogID | blogID: string  | - | - | { "blogID": 1, "userID": "", "community": "", "title": "","description": ""} |
GET | blog | - | userID?: string,community?: string, search?: string: string | - | { "blogID": 3, "userID": 1, "community": "","title": "","description": "","username": "","comments": [{"blogCommentID": 3,"blogID": 3,"userID": 1,"comment": "","username": ""}]} |
POST | blog:blogID | - | userID?: string, community?: string |{"userID":2,"community": "Food", "title":"History 3", "description": ""} | Response |
PATCH | blog:blogID | blogID: string | userID?: string, community?: string |{ "userID" :1, "community": "community","title":"title 2", "description":"description"} | Response |
DELETE | blog:blogID | blogID: string| - | - | Response |
POST | blog-comment | - | - |{"blogID": 1,"userID": 1, "comment": ""} |Response |

[Go to API Document](https://github.com/WoradaS/a-board/blob/main/a-board-api/README.md)

## UI Document

Path: http://localhost:3000/sign-in

![](https://github.com/WoradaS/a-board/blob/main/preview/moblie/sign-in-page.png)
![](/preview/moblie/sign-in-page.png)

Path: http://localhost:3000/

![](https://github.com/WoradaS/a-board/blob/main/preview/moblie/home-page.png)
![](/preview/moblie/home-page.png)


Path: http://localhost:3000/our-blog

![](https://github.com/WoradaS/a-board/blob/main/preview/moblie/our-borad-page.png)
![](/preview/moblie/our-borad-page.png)

Path: http://localhost:3000/blog

![](https://github.com/WoradaS/a-board/blob/main/preview/moblie/blog.png)
![](/preview/moblie/blog.png)

[More Information about UI](https://github.com/WoradaS/a-board/blob/main/a-board-ui/README.md)
