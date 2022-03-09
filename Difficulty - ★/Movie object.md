# Movie object

## Difficulty ★☆☆☆☆ (_Completed_)

### Summary

> Unlike other programming languages,
> JavaScript uses objects to construct inheritance.
>
> Each object has a private property which links to another object.
> This object is known as its prototype.
>
> This prototype object has a prototype of its own,
> and this chain continues until an object with a null prototype has been reached.

### Requirement

- create movie object that takes in five arguments
  - Title, Director, Genre, Release year, Rating.
- The movie prototype should have a function called getOverview()
  - logs the following overview for each film's information

### My Solution

```typescript
class Movie {
  title: string;
  director: string;
  genre: string;
  releaseYear: number;
  rating: number;
  getOverview?: () => void;

  constructor(
    title: string,
    director: string,
    genre: string,
    releaseYear: number,
    rating: number
  ) {
    this.title = title;
    this.director = director;
    this.genre = genre;
    this.releaseYear = releaseYear;
    this.rating = rating;
  }
}

const movie1 = new Movie("Interstellar", "Christopher Nolan", "SF", 2014, 8.7);

Movie.prototype.getOverview = function () {
  console.log(
    `${this.title}, a ${this.genre} film directed by ${this.director} was released in ${this.releaseYear}.
     It received a rating of ${this.rating}`
  );
};

movie1.getOverview(); //OUTPUT : Interstellar, a SF film directed by Christopher Nolan was released in 2014. It received a rating of 8.7
```
