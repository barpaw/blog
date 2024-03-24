<a name="readme-top"></a>

[![100commitow.pl](https://img.shields.io/badge/Participant-100commitow.pl-000000)](http://100commitow.pl)


# Blog

![Logo](docs/images/logo/logo_big.png?raw=true)

A simple open-source blog web application that can be almost entirely managed from the Git repository. 
###### The blog database synchronizes with changes in the Git repository specified in the application settings. The blog automatically imports and synchronizes data in a specific format (template) from defined branches of the Git repository.



## Main concepts

The git repository defined in the application settings will serve as a database of posts, authors, settings, etc. The application will synchronize and update data from the git repository from time to time. For immediate updates, it will also be possible to use webhooks for this purpose.

#### Posts 
* Posts commited on specified branch `posts/(...)` will be automatically imported and can be manually or automatically published.

* Each post should be a separate branch in the repository (Branch is the unique identifier of a post).

* Each post should have a specific structure defined in the markdown file.

#### Authors 

* Each author should have a specific structure defined in the markdown file.

#### Series

* Each series should have a specific structure defined in the markdown file.

#### Announcement

* Announcement should have a specific structure defined in the markdown file.

#### Settings

* Settings should have a specific structure defined in the markdown file.

#### Ads

* Ads should have a specific structure defined in the markdown file.

## Branch names used by app and commit templates

| Branch name | Description | Template |
| ---------------------------------------------------------------- | ---------- | ----------- |
| post/(...)                                                   | Posts will be imported from this branch.| [TODO](https://github.com/)     |
| categories                                                   | Categories will be imported from this branch.| [TODO](https://github.com/)     |
| tags                                                   | Tags will be imported from this branch.| [TODO](https://github.com/)     |
| author/(...) | Authors will be imported from this branch. | [TODO](https://github.com/)     |
| series/(...) | Series will be imported from this branch. | [TODO](https://github.com/)  |
| announcement | Announcement will be imported from this branch. | [TODO](https://github.com/)  |
| settings                                              | Settings will be imported from this branch. | [TODO](https://github.com/)  |
| ads                                              | Ads will be imported from this branch. | [TODO](https://github.com/)  |
| terms                                              | Terms will be imported from this branch. | [TODO](https://github.com/)  |
| contact                                              | Contact will be imported from this branch. | [TODO](https://github.com/)  |

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
- Message bus ([MassTransit](https://github.com/MassTransit/MassTransit) & RabbitMQ)

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
- Allow easy integration with external content providers by API
- Integrate donations
- Series (gorup posts into series with defined name and order)

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
- [X] Guest: Search
- [ ] Admin: Dashboard with stats
- [ ] Admin: Blog Settings
- [ ] Admin: Publications management
- [ ] Admin: Authors management
- [ ] Admin: Series management
- [ ] Admin: Message inbox
- [ ] Admin: Synchronization Logs
- [ ] Admin: Audit Logs


### Next
- [ ] Big Picture
- [ ] Database Schema
- [ ] Implementation

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## License

[MIT](https://choosealicense.com/licenses/mit/)

<p align="right">(<a href="#readme-top">back to top</a>)</p>
