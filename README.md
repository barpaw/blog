<a name="readme-top"></a>

[![100commitow.pl](https://img.shields.io/badge/Participant-100commitow.pl-000000)](http://100commitow.pl)



# Blog

A simple open-source blog web application in which you can publish posts (markdown files with a defined structure) from the git repository.

## Main concepts

* The git repository defined in the application settings will serve as a database of post drafts (they will be automatically imported and can be manually/automatically published).

* Each post should be a separate branch in the repository (Branch is the unique identifier of a post).

* Each post should have a specific structure defined in the markdown file.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Mockups
![Blog home page](docs/images/mockups/homepage/homepage.png?raw=true)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Architecture & Infrastructure

- Modular monolith
- Message bus ([MassTransit](https://github.com/MassTransit/MassTransit) & RabbitMQ)
- Uses [Keycloak](https://github.com/keycloak/keycloak) for Identity and Access Management (IDP)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Features

- CRUD Posts/Categories/Tags
- Posts divided into two types: shorts and articles
- Posts are not created through the editor in the application, but by synchronizing with the indicated git repository and specific Markdown files
- Two post publishing mechanisms: manual and automatic
- Using automatic publishing, you can define the time of publication of the post
- Using manual publishing, you can preview the post before publishing
- The post has one author, but they may be different authors
- Social media share 
- Time to read indicator
- Slug URL / Clean URL
- i18n (English & Polish)
- Dark Theme

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Designed with future features in mind

- CRUD Comments
- Admin dashboard (statistics, management)
- Integrate with some newsletter platform(s?)
- Allow easy integration with external content providers by API
- Integrate donations
- Media manager (photos)
- Series (gorup posts into series with defined name and order)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## TODO

### Mockups & visually defined project boundaries
- [X] Guest: Homepage
- [X] Guest: Publications (Shorts & Articles)
- [X] Guest: Post
- [ ] Guest: Archive
- [ ] Guest: Newsletter
- [ ] Guest: Contact
- [ ] Guest: Search
- [ ] Admin: Publications management
- [ ] Admin: Blog Settings
- [ ] Admin: Publications Logs
- [ ] Admin: Audit Log
- [ ] Admin: Dashboard with stats


### Next
- [ ] Big Picture
- [ ] Database Schema
- [ ] Implementation

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## License

[MIT](https://choosealicense.com/licenses/mit/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
