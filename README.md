
[![100commitow.pl](https://img.shields.io/badge/Participant-100commitow.pl-000000)](http://100commitow.pl)



# Blog

Simple open-source blog web application.

![Blog home page](docs/images/home.png?raw=true)

## Architecture & Infrastructure

- Modular monolith
- Message bus ([MassTransit](https://github.com/MassTransit/MassTransit) & RabbitMQ)
- Uses [Keycloak](https://github.com/keycloak/keycloak) for Identity and Access Management (IDP)


## Features

- CRUD Posts/Categories/Tags
- Posts divided into two types: shorts and articles
- The post has one author, but posts can be published by different authors
- Posts are not created through the editor in the application, but by synchronizing with the indicated git repository and specific Markdown files
- Posts drafts, schedule publication
- Contact page
- Archive page
- Social media share 
- Time to read indicator
- Slug URL / Clean URL
- i18n (English & Polish)
- Dark Theme

## Designed with future features in mind

- CRUD Comments
- Admin dashboard (statistics, management)
- Integrate with some newsletter platform(s?)
- Allow easy integration with external content providers by API
- Integrate donations
- Media manager (photos)
- Series (gorup posts into series with defined name and order)

## License

[MIT](https://choosealicense.com/licenses/mit/)


