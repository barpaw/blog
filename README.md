<a name="readme-top"></a>

[![100commitow.pl](https://img.shields.io/badge/Participant-100commitow.pl-000000)](http://100commitow.pl)


# Blog

![Logo](docs/images/logo/logo_big.png?raw=true)

A simple open-source blog web application that can be entirely managed from the Git repository. 

###### The blog database synchronizes with changes in the Git repository specified in the application settings. The blog automatically imports and synchronizes data in a specific format (templates) from the Git repository.

## Main concepts

The git repository defined in the application settings will serve as a database of content and settings. The application will synchronize and update data from the git repository from time to time. For immediate updates, it will also be possible to use webhooks for this purpose.

## Templates and repository structure used by app

| Name            | Type | Description                                    | Template |
|-----------------|------|------------------------------------------------|----------|
| content/{series-order_series-name}/posts/      | dir  | Posts will be imported from this folder and will be associated with the series.  | [Example](docs/templates/content/0_NONE/posts/)     |
| files/{folder_name}    | dir  | Includes (frontend static blog content) and other files (assets), e.g. images, will be imported from this folder.     | [Example](docs/templates/files/)      |
| authors.yml    | file  | Authors will be imported from this file.     | [Example](docs/templates/authors.yaml)     |
| categories.yml      | file  | Categories will be imported from this file.  | [Example](docs/templates/categories.yaml)     |
| series.yml    | file  | Data related to series (collections) of posts will be imported from this file.      | [Example](docs/templates/series.yaml)     |
| settings.yml        | file  | Blog-related settings will be imported from this file.   | [Example](docs/templates/settings.yaml)     |


<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Mockups
* [Homepage](docs/images/mockups/homepage/homepage.png)
* [Publications Grid](docs/images/mockups/publications_grid/publications_grid.png)
* [Post](docs/images/mockups/post/post.png)
* [Series Grid](docs/images/mockups/series_grid/series_grid.png)
* [Series](docs/images/mockups/series/series.png)
* [Search](docs/images/mockups/search/search.png)
* [Archive](docs/images/mockups/archive/archive.png)
* [Contact](docs/images/mockups/contact/contact.png)
* [Privacy Policy / Terms](docs/images/mockups/privacypolicy/privacypolicy.png)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Architecture & Infrastructure

- Modular monolith
- Multi-tenancy
- Message bus ([MassTransit](https://github.com/MassTransit/MassTransit) & RabbitMQ)
- Workers
- Outbox pattern
- Postgresql Database
- MinIO - Object Storage
  

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Entities

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Features

- CRUD Posts/Categories/Tags/Series/Files/Repos
- Posts divided into two types: shorts and articles
- The post has one author, but they may be different authors
- Social media share 
- Time to read indicator
- Slug URL / Clean URL
- i18n (English & Polish)
- Dark Theme
- Series (gorup posts into series with defined name and order)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Designed with future features in mind

- CRUD Comments
- Admin dashboard (statistics, management)
- Allow easy integration with external content providers by API
- Integrate donations

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## TODO

### Mockups & visually defined project boundaries

- [X] Guest: Homepage
- [X] Guest: Publications Grid (Posts = Shorts & Articles)
- [X] Guest: Post
- [X] Guest: Series Grid
- [X] Guest: Series 
- [X] Guest: Archive
- [X] Guest: Privacy policy / Terms
- [X] Guest: Contact
- [X] Guest: Searchceramiczny Porothermceramiczny Porotherm



### Planning

- [X] Repository Changes Synchronization
- [ ] Database Schema (in progress...)
- [ ] Big Picture

### Validator script

- [ ] Validator script should check for all embedded files have unique name & should generate a list of all file names
- [ ] Validator script should generate file with unique list of all tags
- [ ] Validate file names and posts/series order

### Next
- [ ] Implementation

### Implementation
- [ ] Project Core (logs, swagger, entity framework, mass transit)
- [ ] Project structure
- [ ] Entities and data access 
- [ ] Workers and stuff for repositories synchronization
- [ ] API 

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Inspirations

## License

[MIT](https://choosealicense.com/licenses/mit/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
