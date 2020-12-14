<h3 align="center">
    Challenge 02: Node.js Concepts
</h3>

<p align="center">
  <img alt="GitHub language count" src="https://img.shields.io/github/languages/count/marcosbergami/nodejs-concepts-challenge?color=blueviolet">

  <a href="https://www.linkedin.com/in/marcos-bergami-160771112">
    <img alt="Made by Marcos Bergami" src="https://img.shields.io/badge/made%20by-Marcos%20Bergami-blueviolet">
  </a>

  <img alt="Last commit" src="https://img.shields.io/github/last-commit/marcosbergami/nodejs-concepts-challenge">
</p>

## :computer: My first challenge

I have started my journey on learning web development. I am currenly enrolled in a **[boot camp](https://pages.rocketseat.com.br/gostack)** provided by Rocketseat.

Our first development challenge, was to build the back-end of an application that allows the user to create, read, update, and delete repositories.

In the first stage of the bootcamp, we have been learning about HTTP requests and REST API.

### Application routes

The back-end of this newly created application, has a total of 5 routes at the moment.

- **`POST /repositories`**: This route receives a title, url, and techs inside of the request's body. Whenever a new repository is created, it is stored in the following format: `{ id: "uuid", title: 'Node.js Challenge', url: 'http://github.com/...', techs: ["Node.js", "..."], likes: 0 }`; The likes will always start at 0 whenever a repository is created. A user will be able to like repositories and the likes amount will be stored as it increases.

- **`GET /repositories`**: This route will list all of the repositories.

- **`PUT /repositories/:id`**: This route will only alter the title, url, and techs of the repository whose id has been passed as a parameter to the request. This route will not update the number of likes. A separate route will be responsible for like creation. A middleware was utilized in this route to check if the id that was received is a valid one.

- **`DELETE /repositories/:id`**: This route will be responsible for deleting a repository whose id matches the one received in the request. A middleware was utilized in this route to check if the id that was received is a valid one.

- **`POST /repositories/:id/like`**: This route will increase the number of likes by 1 for the specific repository whose id matches the one received in the request. A separate route was created to handle likes in order to interpret its creation. This will be useful in the future in order to track which user liked this repository and store this data in a database moving forward, for example. A middleware was also utilized in this route to ensure the id passed as a parameter is valid.

This was overall a very fun challenge to begin with. I have utilized **[Insomnia](https://insomnia.rest/)** to test the requests as well as I have ran the automated tests provided by Rocketseat to ensure the application is working as expected.

<img alt="Tests" src="https://user-images.githubusercontent.com/56553101/101205665-97074480-3633-11eb-9437-cbc769538405.png" />

---

Made with :heart: by Marcos Bergami
