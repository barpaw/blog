
[![100commitow.pl](https://img.shields.io/badge/Participant-100commitow.pl-000000)](http://100commitow.pl)



# Blog

Simple open-source blog web application.

![Blog home page](docs/images/home.png?raw=true)

## Architecture & Infrastructure

- Modular monolith
- Message bus ([MassTransit](https://github.com/MassTransit/MassTransit) & RabbitMQ)
- Uses [Keycloak](https://github.com/keycloak/keycloak) for Identity and Access Management (IDP)


## Features

- CRUD Posts/Comments/Series/Categories/Tags/Comments
- Posts divided into two types: shorts and articles
- The post has one author, but posts can be published by different authors
- Posts are not created through the editor in the application, but by synchronizing with the indicated git repository and specific Markdown files
- Social media share 
- Time to read
- Slug url
- SEO optimizations
- Posts drafts, schedule publication
- Two languages (EN/PL)
- Dark Theme
- Contact page
- Archive page
- Posts can be combined into a series (with name and order)
- Guest comments secured by captcha

## Designed with future features in mind

- Admin dashboard (statistics, management)
- Integrate with some newsletter platform(s?)
- Allow easy integration with external content providers by API
- Integrate donations
- Media manager (photos)
- Integration with comment service (Quora or Disqus)

## License

[MIT](https://choosealicense.com/licenses/mit/)


