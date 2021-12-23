# Gridiron

A framework for simple static sites. Built off of [11ty](https://www.11ty.dev) and [Tailwind](https://tailwindcss.com).

## Layouts

Structuring a site involves building a hierarchy of Markdown files, each given a layout. Supported layouts are listed below.

### simple

Straightforward, direct. Displays whatever is written in the standard style of the site.

### academic

A relevant landing page for an academic. Sections for displaying recent publications, news, service, and other sources of content.

Expects global data files with the following structure:

```()
_data
|-- academic
|   |-- news.*
|   |-- publications.*
|   +-- service.*
```

Each `*` above can be any data file format recognized by [11ty](https://www.11ty.dev/docs/data-global/), and formats are not required to be uniform.

#### News

For announcing awards, accomplishments, and accolades.

The `_data/academic/news.*` file provides a *list* of news items, each of which contains the following fields:

* `date`: Date object for when news was relevant.
* `headline`: The "title" of the news item.
* `description`: A byline, or the content of the news item.
* `notes`: A list of notes about the news item.

#### Publications

A list of publications, talks, presentations, and other academically-significant contributions to the literature.

The `_data/academic/publications.*` file has several fields containing list of *publication items*. They are:

* `talk`
* `journal`
* `conference`
* `article`
* `book`

Each publication item has the following fields:

* `date`: When the publication was made relevant.
* `title`: The title of the publication.
* `authors`: A list of authors, as simple strings.
* `location`: *Where* the publication was made relevant. Could be, e.g., the journal name, the conference name, or the talk venue.
* `source`: Reference to the publication, external or internal.
* `description`: Summary of the publication item; abstract, if relevant.
* `selected`: Flag indicating if the publication should be displayed on the landing page.
* `notes`: A list of notes about the publication item.

#### Service

Committee positions, conference session chairing, and the like.

The `_data/academic/service.*` file comprises service items with the following field:

* `date`: When the service was performed.
* `description`: Summary of the service performed.
* `notes`: A list of notes about the service item.
