# Movie Reel

### 1. C4Q Movie Reel

Access Code has partnered with a local media company that specializes in movie databases named *Reel Good Media*. *Reel Good* is a scrappy young startup that's looking to add to its mobile presence with a clean, functional app that can display info they store in their database. In this partnership, Access Code will help Reel Good develop their app to their specifications.

In this first draft of the app, Reel Good wants a simple prototype that they can test and give feedback on. According to Reel Good, their ideal MVP ([minimum viable product](https://en.wikipedia.org/wiki/Minimum_viable_product)) would have:

1. A `UITableView` to list data from a subset of their database info
2. `UITableViewCell`s large enough to be able to list the `title`, `year` and `synopsis` of their movies


### 2. Movie Data

For this project, we'll need a model that includes:

- A `Movie` class 
- The data including all of the movies

<details>
<summary>class Movie</summary>

```swift
class Movie {
    var name: String
    var year: Int
    var genre: String
    var cast: [String]
    var locations: [String]
    public var description: String
    init(name: String, year: Int, genre: String, cast: [String], locations: [String], description: String) {
        self.name = name
        self.year = year
        self.genre = genre
        self.cast = cast
        self.locations = locations
        self.description = description
    }
}
```
</details>

<details>
<summary>Movie Data</summary>

```swift
struct MovieData {
    static let movies: [Movie] = [
        Movie(name: "Minions",
              year: 2015,
              genre: "animation",
              cast: ["Sandra Bullock", "Jon Hamm", "Michael Keaton"],
              locations: ["New York", "Los Angeles"],
              description: "Evolving from single-celled yellow organisms at the dawn of time, Minions live to serve, but find themselves working for a continual series of unsuccessful masters, from T. Rex to Napoleon. Without a master to grovel for, the Minions fall into a deep depression. But one minion, Kevin, has a plan."),
        Movie(name: "Shrek",
              year: 2001,
              genre: "animation",
              cast: ["Mike Myers", "Eddie Murphy", "Cameron Diaz"],
              locations: ["Fairyland", "Los Angeles"],
              description: "Once upon a time, in a far away swamp, there lived an ogre named Shrek whose precious solitude is suddenly shattered by an invasion of annoying fairy tale characters. They were all banished from their kingdom by the evil Lord Farquaad. Determined to save their home -- not to mention his -- Shrek cuts a deal with Farquaad and sets out to rescue Princess Fiona to be Farquaad\"s bride. Rescuing the Princess may be small compared to her deep, dark secret."),
        Movie(name: "Zootopia",
              year: 2016,
              genre: "animation",
              cast: ["Ginnifer Goodwin", "Jason Bateman", "Idris Elba"],
              locations: ["New York", "Toronto"],
              description: "From the largest elephant to the smallest shrew, the city of Zootopia is a mammal metropolis where various animals live and thrive. When Judy Hopps becomes the first rabbit to join the police force, she quickly learns how tough it is to enforce the law."),
        Movie(name: "Avatar",
              year: 2009,
              genre: "action",
              cast: ["Sam Worthington", "Zoe Saldana", "Sigourney Weaver"],
              locations: ["Space", "Los Angeles"],
              description: "On the lush alien world of Pandora live the Na\"vi, beings who appear primitive but are highly evolved. Because the planet\"s environment is poisonous, human/Na\"vi hybrids, called Avatars, must link to human minds to allow for free movement on Pandora. Jake Sully, a paralyzed former Marine, becomes mobile again through one such Avatar and falls in love with a Na\"vi woman. As a bond with her grows, he is drawn into a battle for the survival of her world."),
        Movie(name: "The Dark Knight",
              year: 2008,
              genre: "action",
              cast: ["Christian Bale", "Heath Ledger", "Aaron Eckhart"],
              locations: ["Gotham", "Justice League of America"],
              description: "With the help of allies Lt. Jim Gordon and DA Harvey Dent, Batman has been able to keep a tight lid on crime in Gotham City. But when a vile young criminal calling himself the Joker suddenly throws the town into chaos, the caped Crusader begins to tread a fine line between heroism and vigilantism."),
        Movie(name: "Transformers",
              year: 2007,
              genre: "action",
              cast: ["Shia LaBeouf", "Megan Fox", "Josh Duhamel"],
              locations: ["Tokyo", "Sapporo"],
              description: "The fate of humanity is at stake when two races of robots, the good Autobots and the villainous Decepticons, bring their war to Earth. The robots have the ability to change into different mechanical objects as they seek the key to ultimate power. Only a human youth, Sam Witwicky can save the world from total destruction."),
        Movie(name: "Titanic",
              year: 1997,
              genre: "drama",
              cast: ["Leonardo DiCaprio", "Kate Winslet", "Billy Zane"],
              locations: ["Liverpool", "Belfast", "New York", "Arctic"],
              description: "The ill-fated maiden voyage of the R.M.S. Titanic; the pride and joy of the White Star Line and, at the time, the largest moving object ever built. She was the most luxurious liner of her era -- the \"ship of dreams\" -- which ultimately carried over 1,500 people to their death in the ice cold waters of the North Atlantic in the early hours of April 15, 1912."),
        Movie(name: "The Hunger Games",
              year: 2012,
              genre: "drama",
              cast: ["Jennifer Lawrence", "Josh Hutcherson", "Liam Hemsworth"],
              locations: ["New York", "Wisconsin"],
              description: "Katniss Everdeen voluntarily takes her younger sister\"s place in the Hunger Games, a televised competition in which two teenagers from each of the twelve Districts of Panem are chosen at random to fight to the death."),
        Movie(name: "American Sniper",
              year: 2014,
              genre: "drama",
              cast: ["Bradley Cooper", "Sienna Miller", "Kyle Gallner"],
              locations: ["Los Angeles", "Detroit", "Morocco"],
              description: "Navy S.E.A.L. sniper Chris Kyle\"s pinpoint accuracy saves countless lives on the battlefield and turns him into a legend. Back home to his wife and kids after four tours of duty, however, Chris finds that it is the war he can\"t leave behind.")
    ]
}
```
</details>

- Make a file named Movie.swift and copy the Movie class above there
- Make a file named Data.swift and copy the Data class there


