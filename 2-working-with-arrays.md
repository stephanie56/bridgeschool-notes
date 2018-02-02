# Working with Arrays

## Map
## Filter
## Reduce


```javascript
const listOfPets = [
    {name: 'Rover', species: 'cat', isAdopted: false, age: 5},
    {name: 'Whiskers', species: 'dog', isAdopted: true, age: 5},
    {name: 'Snuggles', species: 'raccoon', isAdopted: true, age: 7},
    {name: 'Beaks', species: 'dog', isAdopted: true, age: 1},
    {name: 'Paws', species: 'snake', isAdopted: false, age: 13},
    {name: 'Splashy', species: 'cat', isAdopted: false, age: 4},
    {name: 'Bashful', species: 'dragon', isAdopted: false, age: 40},
    ];

    let allDogs = listOfPets.filter(pet => pet.species === 'dog');
    let allCats = listOfPets.filter(pet => pet.species === 'cat');
    let notDogsOrCats = listOfPets.filter(pet => pet.species != 'dog' && pet.species != 'cat');

    let namingFunction = ({name, species, age}) => `${name} the ${species} is ${age} year(s) old!`;
```
```javascript
const mostPopularMovies = [{
    title: 'Rogue One: A Star Wars Story',
    rating: 8.1,
    rank: 1,
}, {
    title: 'Passengers',
    rating: 7.1,
    rank: 2,
}, {
    title: 'La La Land',
    rating: 8.8,
    rank: 3,
}, {
    title: 'Assassins Creed',
    rating: 6.5,
    rank: 4,
}, {
    title: 'Sing',
    rating: 7.3,
    rank: 5,
}, {
    title: 'Suicide Squad',
    rating: 6.4,
    rank: 6,
}, {
    title: 'The Girl on the Train',
    rating: 6.6,
    rank: 7,
}, {
    title: 'The Magnificent Seven',
    rating: 7.0,
    rank: 8,
}, {
    title: 'Underworld: Blood Wars',
    rating: 6.4,
    rank: 9,
}, {
    title: 'Arrival',
    rating: 8.3,
    rank: 10,
}];

function getMovieNames(movies) {
    // write a function that returns an array of only move titles
    return movies.map(map => map.title);
}

function getGreatMovies(movies) {
    // great movies have a rating above an 8.0
    // write a function that returns only great movies
    return movies.filter(movie => movie.rating > 8);
}

function getGreatMovieNames(movies) {
    // write a function that reutrns an array that contains
    // only great movie names
    return getGreatMovies(movies).map(greatMovie => greatMovie.title);
}
```
