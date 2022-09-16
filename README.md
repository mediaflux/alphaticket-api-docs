# AlphaTicket API

Use the AlphaTicket API to integrate movie data directly into your website or app. AlphaTicket and your website or app back-end will communicate by sending HTTP requests back and forth.

This page provides an overview of the AlphaTicket API. The topics in the chapter deal with a number of specific aspects of the API. We recommend to read these topics entirely.
The API is continuously being developed without breaking changes.

As the API grows this documentation will be migrated to Swagger.

If you have any questions about integrating our API, please [contact us](mailto:info@media-flux.com). We are happy to help!

## Good to know

- JSON parameters marked as *(optional)* will be omitted from the JSON object.

  This means the data is not available (yet), is not applicable or is not (yet) set by the exhibitor.

  Make sure your UI can handle if any or all optional data is missing. 

## Contents

- Schemas
    - [Movie](#movie-schema)
    - [Schedule](#schedule-schema)
- References
    - [Visibility](#visibility-reference)
    - [Genre](#genre-reference)

## Schemas

### Movie Schema

Example data

    {
      "id": 555,
      "slug": "minions-the-rise-of-gru",
      "originalTitle": "Minions: The Rise of Gru",
      "originalLanguage": "en",
      "runtime": 87,
      "nation": ["USA"],
      "directors": ["Kyle Balda"],
      "actors": ["Steve Carell", "Pierre Coffin", "Taraji P. Henson"],
      "release": "2022-07-06",
      "rating": ["6", "violence", "fear"],
      "visibility": ["SITE", "SIGNAGE", "POS", "SCANNER", "PORTAL", "API"],
      "tags": ["Family"],
      "notice": "Laatste week",
      "imdb": "tt5113044",
      "createdAt": "2022-06-01T06:00:00+00:00",
      "updatedAt": "2022-06-01T06:12:00+00:00",
      "genres": ["animation", "adventure", "comedy"],
      "versions": ["OV-NL-FR", "VLS-XX"],
      "links": {
        "imdb": "https://www.imdb.com/title/tt5113044",
        "facebook": "https://www.facebook.com/minions/",
        "instagram": "https://www.instagram.com/minions/",
        "website": "https://www.minionsmovie.com/",
        "twitter": "https://twitter.com/minions/",
        "youtube": "https://www.youtube.com/illumination"
      },
      "langs": {
        "nl": {
          "title": "Minions: Hoe Gru Superschurk Werd",
          "overview": "Als fan van een superschurkengroep die bekend staat als de Vicious 6, bedenkt Gru een plan om kwaadaardig genoeg te worden om zich bij hen aan te sluiten, met de steun van zijn volgelingen, de Minions.",
          "poster": {
            "medium": "https://app.fluxticket.com/storage/movie/555/poster/nl/1/md.jpg",
            "large": "https://app.fluxticket.com/storage/movie/555/poster/nl/1/lg.jpg",
            "original": "https://app.fluxticket.com/storage/movie/555/poster/nl/1/original.jpg",
            "hash": "5097076a0599f491bf0fcc10022c6bcd",
            "updatedAt": "2022-06-01T06:00:00+00:00"
          },
          "trailer": {
            "provider": "local",
            "url": "https://app.fluxticket.com/storage/movie/555/trailer/en/1.mp4",
            "updatedAt": "2022-06-01T06:00:00+00:00"
          },
          "backgrounds": [
            {
              "url": "https://app.fluxticket.com/storage/movie/555/background/nl/1.jpg",
              "hash": "f336245244e15e69a42710bafa827b62",
              "createdAt": "2022-06-01T06:00:00+00:00"
            },
            {
              "url": "https://app.fluxticket.com/storage/movie/555/background/nl/2.jpg",
              "hash": "bfbeba2b252bc8c7b6b842339fe7e43d",
              "createdAt": "2022-06-01T06:00:00+00:00"
            }
          ],
          "streaming": [
            {
              "provider": "picl",
              "url": "https://picl.be/films/[picl_movie_title]/kijken/?theater=[picl_referrer_id]"
            }
          ]
        },
        "fr": {
          "title": "Les Minions 2 - Il était une fois Gru",
          "tagline": "L'ascension d'un super-vilain.",
          "overview": "Alors que les années 70 battent leur plein, Gru qui grandit en banlieue au milieu des jeans à pattes d’éléphants et des chevelures en fleur, met sur pied un plan machiavélique à souhait pour réussir à intégrer un groupe célèbre de super méchants, connu sous le nom de Vicious 6, dont il est le plus grand fan. Il est secondé dans sa tâche par les Minions, ses petits compagnons aussi turbulents que fidèles. Avec l’aide de Kevin, Stuart, Bob et Otto – un nouveau Minion arborant un magnifique appareil dentaire et un besoin désespéré de plaire - ils vont déployer ensemble des trésors d’ingéniosité afin de construire leur premier repaire, expérimenter leurs premières armes, et lancer leur première mission. Lorsque les Vicious 6 limogent leur chef, le légendaire \" Wild Knuckles \", Gru passe l’audition pour intégrer l’équipe. Le moins qu’on puisse dire c’est que l’entrevue tourne mal, et soudain court quand Gru leur démontre sa supériorité et se retrouve soudain leur ennemi juré.",
          "poster": {
            "medium": "https://app.fluxticket.com/storage/movie/555/poster/fr/1/md.jpg",
            "large": "https://app.fluxticket.com/storage/movie/555/poster/fr/1/lg.jpg",
            "original": "https://app.fluxticket.com/storage/movie/555/poster/fr/1/original.jpg",
            "hash": "7d573d28161fccff1154a3f60077b66c",
            "updatedAt": "2022-06-01T06:00:00+00:00"
          },
          "trailer": {
            "provider": "local",
            "url": "https://app.fluxticket.com/storage/movie/555/trailer/1.mp4",
            "updatedAt": "2022-06-01T06:00:00+00:00"
          },
          "backgrounds": [
            {
              "url": "https://app.fluxticket.com/storage/movie/555/background/1.jpg",
              "hash": "bc8f132c8c4c9f8b66bb25c6491b949f",
              "createdAt": "2022-06-01T06:00:00+00:00"
            },
            {
              "url": "https://app.fluxticket.com/storage/movie/555/background/2.jpg",
              "hash": "2e8d0c9833bede71fb945050d8d8934c",
              "createdAt": "2022-06-01T06:00:00+00:00"
            }
          ]
        }
      },
      "_deepLinks": {
        "site": "https://tickets.cinema.com/movies/view/minions-the-rise-of-gru",
        "portal": "https://portal.fluxticket.com/movies/555"
      }
    }

___

`id` - `bigInt` The identifier uniquely referring to this movie.

`slug` - `string` Unique slug refering to this movie. Value never changes.

`originalTitle` - `string` Official title of the movie

`originalLanguage` - `string` Official spoken language. [RFC 5646](https://www.rfc-editor.org/rfc/rfc5646) code as defined by the [ISDCF](https://registry-page.isdcf.com/languages/) ([JSON codes](https://registry.isdcf.com/languages))

`runtime` - `int` *(optional)* Runtime of the movie in minutes.

`nation` - `array[string]` *(optional)* List of origin countries. ISO 3166-3 code based on [this list](https://raw.githubusercontent.com/webpatser/laravel-countries/master/src/Webpatser/Countries/Models/countries.json)

`directors` - `array[string]` *(optional)* List of directors.

`actors` - `array[string]` *(optional)* List of actors.

`release` - `date` *(optional)* National release date (based on cinema country), in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) date format `YYYY-MM-DD`.

`rating` - `array[string]` *(optional)*  National rating (sources: [Belgium](https://www.kijkwijzer.be/) - [Luxembourg](https://www.alia.lu/en/cinema)). `null` if rating is pending

`visibility` - `array[string]` List of visibilities, see [Visibility reference](#visibility-reference) for more info

`tags` - `array[string]` *(optional)* List of custom movie tags. Can be any kind of string.

`notice` - `string` *(optional)* Important message to be shown to the visitor in regard to this movie.

`imdb` - `string` *(optional)* IMDB ID.

`createdAt` - `datetime` The movie date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format

`updatedAt` - `datetime` The movie date and time of the last update, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. The value is updated for any change to this object.

`deletedAt` - `datetime` *(optional)* The date and time when this movie was deleted, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format.

`genres` - `array[string]` *(optional)* List of movie genres, see [Genre reference](#genre-reference) for more info.

`versions` - `array[string]` *(optional)* List of scheduled versions to play, in [ISDCF Language](https://registry-page.isdcf.com/illustratedguide/) format. Only optional when there are no schedules for this movie.

`links` - `object` *(optional)* Keyed object with **optional** external links. Possible keys: `["imdb", "website", "facebook", "instagram", "twitter", "youtube"]`

`langs.[locale]` - `object` Keyed object with translated metadata and assets. Key is the language locale. Only containes translations for your cinema enabled languages. Currently
supported: `["en", "nl", "fr", "de"]`

`langs.[locale].title` - `string` Translated title

`langs.[locale].tagline` - `string` *(optional)* Short tagline

`langs.[locale].overview` - `string` *(optional)* Plot of the movie or omitted if no plot is available (exceptional but possible)

`langs.[locale].poster` - `object` *(optional)* Object containing different sizes of the poster. Omitted if no poster is available (exceptional but possible)

`langs.[locale].poster.[size]` - `string` Possible sizes: `["medium", "large", "original"]`. Value is the URL to the asset that needs to be downloaded locally (hotlinking is not allowed).

`langs.[locale].poster.hash` - `string` Unique hash for this poster. When syncing the backgrounds the hash can be used to determine if the asset needs to be downloaded.

`langs.[locale].poster.updatedAt` - `datetime` Last date and time the poster was updated, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format.

`langs.[locale].trailer` - `object` *(optional)* Object containing a link to the trailer.

`langs.[locale].trailer.provider` - `string` Possible values: `["local", "youtube"]`. When value is `local` the asset needs to be downloaded locally (hotlinking is not allowed).

`langs.[locale].trailer.url` - `string` URL of the trailer

`langs.[locale].trailer.updatedAt` - `datetime` Last date and time the trailer was updated, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format.

`langs.[locale].backgrounds` - `array[object]` *(optional)* Array containing background objects. 

`langs.[locale].backgrounds.[index].url` - `string` URL of the background

`langs.[locale].backgrounds.[index].hash` - `string` Unique hash for this background. When syncing the backgrounds the hash can be used to determine if the asset needs to be downloaded.

`langs.[locale].backgrounds.[index].createdAt` - `datetime` Date and time the background was published, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format.

`langs.[locale].streaming` - `array[object]` *(optional)* Array containing links to external streaming providers where this movie can be watched.

`langs.[locale].streaming.[index].provider` - `string` Name of provider. Currently only `picl` is supported

`langs.[locale].streaming.[index].url` - `string` Deeplink to the streaming website page. Currently only external websites are supported.

`_deepLinks` - `object` Object containing several usefull deeplinks

`_deepLinks.site` - `object` Deeplink to the movie page on the AlphaTicket site.

`_deepLinks.portal` - `object` Deeplink to the movie page on the AlphaTicket portal. This link requires authentication.

### Schedule Schema

    [
      {
        "id": 100,
        "movieId": 555,
        "version": "VLS-XX",
        "start": "2022-09-07T12:00:00+00:00",
        "soldOut": true,
        "soldOutOnline": true,
        "createdAt": "2022-06-01T06:00:00+00:00",
        "updatatedAt": "2022-06-01T06:12:00+00:00",
        "_deepLinks": {
          "checkout": "https://tickets.cinema.com/buy/tickets/100",
          "portal": "https://portal.fluxticket.com/schedules/100"
        }
      },
      {
        "id": 101,
        "movieId": 555,
        "version": "OV-NL-FR",
        "start": "2022-09-07T14:00:00+00:00",
        "soldOutOnline": true,
        "createdAt": "2022-06-01T06:00:00+00:00",
        "updatatedAt": "2022-06-01T06:12:00+00:00",
        "_deepLinks": {
          "checkout": "https://tickets.cinema.com/buy/tickets/101",
          "portal": "https://portal.fluxticket.com/schedules/101"
        }
      },
      {
        "id": 102,
        "movieId": 555,
        "version": "OV-NL-FR",
        "start": "2022-09-07T18:00:00+00:00",
        "createdAt": "2022-06-01T06:00:00+00:00",
        "updatatedAt": "2022-06-01T06:12:00+00:00",
        "deletedAt": "2022-07-10T14:12:00+00:00",
        "_deepLinks": {
          "checkout": "https://tickets.cinema.com/buy/tickets/101",
          "portal": "https://portal.fluxticket.com/schedules/101"
        }
      }
    ]

___

`id` - `bigInt` The identifier uniquely referring to this schedule.

`movieId` - `bigInt` Relation to the Movie identifier

`version` - `string` Scheduled version, in [ISDCF Language](https://registry-page.isdcf.com/illustratedguide/) format

`start` - `datetime` Start time of the schedule, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. The value is updated for any change to this object.

`soldOut` - `boolean` *(optional)* `true` when the schedule is completely sold out, paramater is omitted when `false`

`soldOutOnline` - `boolean` *(optional)* `true` when the schedule is sold out **online**. When `soldOut` is omitted this means there are still tickets available at the box office. Paramater is omitted when `false`

`visibility` - `array[string]` List of visibilities, see [Visibility reference](#visibility-reference) for more info

`createdAt` - `datetime` The schadule date and time of creation, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format

`updatedAt` - `datetime` The schedule date and time of the last update, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format. The value is updated for any change to this object.

`deletedAt` - `datetime` *(optional)* The date and time when this schedule was deleted, in [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format.

`_deepLinks` - `object` Object containing several usefull deeplinks

`_deepLinks.checkout` - `object` Deeplink to the schedule checkout page on the AlphaTicket site.

`_deepLinks.portal` - `object` Deeplink to the schedule page on the AlphaTicket portal. This link requires authentication.

## References

### Visibility reference

- `SITE` If set, item should be shown on the website
- `SIGNAGE` If set, item should be shown on any digital signage
- `POS` If set, item should be available from any POS system (Point-Of-Sale / Box-office)
- `SCANNER` If set, item should be available from any mobile scanner
- `PORTAL` If set, item should be available in the AlphaTicket portal
- `API` If set, item should be available from the API

### Genre reference

Genres is a fixed list of the values below. These are meant to be translated.

    ["action", "adventure", "animation", "comedy", "crime", "documentary", "drama", "family", "fantasy", "history", "horror", "music", "mystery", "romance", "science-fiction", "thriller", "war", "western"]

