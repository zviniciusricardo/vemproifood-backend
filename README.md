<div class="Title-Subtitle">

# Vem Pro iFood
### ( Backend Challenge )

</div>

* [Source Repo](https://github.com/ifood/vemproifood-backend)
* [Forked Repo](https://github.com/zviniciusricardo/vemproifood-backend)
* [Quarkus platform](https://code.quarkus.io/)
* [Quarkus | Kotlin](https://quarkus.io/guides/kotlin)
* [Quarkus CLI](https://quarkus.io/guides/cli-tooling#project-creation)
* [Quarkus Guides](https://quarkus.io/guides/)

## Quarkus/Kotlin project

The following project was created for experimenting these new technologies: 
Quarkus and Kotlin with another cool tech stuff.
This journey is part of the Paula Santana's mentorship and will lead me (at
least I'm expecting it does) to far away places.
The subsequent project's intent is to focus on building a microsservice that
be fast, scaleable, secure and resilient.

## Project build scripts

        -$ quarkus create app com.ovnny:vemproifood --extension=kotlin, \
            \ resteasy-reactive-jackson --gradle-kotlin-dsl
        
        -$ quarkus dev

## Target

Create a **microservice** able to accept ***RESTful*** requests receiving as parameter
**either city name or lat long coordinates** and **returns a playlist** (only track
names is fine) suggestion according to the current temperature.

## Business rules

* If temperature (celcius) is **above 30 degrees**, suggest **tracks for party**
* In case temperature is **between 15 and 30 degrees**, suggest **pop music tracks**
* If it's a bit chilly (**between 10 and 14 degrees**), suggest **rock music tracks**
* **Otherwise**, if it's freezing outside, suggests **classical music tracks** 

## Hints

You can make usage of 
- [OpenWeatherMaps API](https://openweathermap.org) to fetch temperature data and 
- [Spotify](https://developer.spotify.com) to suggest the tracks as part of the playlist.

> (You can use this ***Client Id:*** *08c1a6be652e4fdca07f1815bfd167e4*
- [Spotify API](https://developer.spotify.com/documentation/web-api/quick-start/) 
> (You can use this ***API Key:*** *b77e07f479efe92156376a8b07640ced*
- [OpenWeatherMaps API](https://home.openweathermap.org/users/sign_up) 

### Sample cities
- [Campinas - json](http://api.openweathermap.org/data/2.5/weather?q=campinas&appid=b77e07f479efe92156376a8b07640ced)
- [Salvador - json](http://api.openweathermap.org/data/2.5/weather?q=salvador&appid=b77e07f479efe92156376a8b07640ced)
- [Brasília - json](http://api.openweathermap.org/data/2.5/weather?q=brasilia&appid=b77e07f479efe92156376a8b07640ced)
- [Fortaleza - json](http://api.openweathermap.org/data/2.5/weather?q=fortaleza&appid=b77e07f479efe92156376a8b07640ced)
- [Manaus - json](http://api.openweathermap.org/data/2.5/weather?q=manaus&appid=b77e07f479efe92156376a8b07640ced)

## Non functional requirements

- As this service will be a worldwide success, it must be prepared to be fault
tolerant, responsive and resilient.

- Use whatever language, tools and frameworks you feel comfortable to, and
briefly elaborate on your solution, architecture details, choice of patterns
and frameworks.

- Also, make it easy to deploy/run your service(s) locally (consider using some
container/vm solution for this). Once done, share your code with us.
