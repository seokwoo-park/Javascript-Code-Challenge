# Available books

## Difficulty ★☆☆☆☆ (_Completed_)

### Summary

> Unlike classical programming languages like Java or C++
> Javascript uses objects within a prototypal inheritance model
> In ES 2015 or ES6, the class keyword was introduced.

### Requirement

- Create a book class

  - Each book have Title, Author, ISBN, numCopies

- need a getAvailability() function

  - return "Out of stock" if 0 available copies, "Low stock" if < 10 copies and "In stock" otherwise

- need a sell(numSold) function.

  - this will take the number of copies sold and subtract it from the total number of copies.
  - if no argument is passed, default the number of copies to sell to one.

- need a restock(numCopies) function.

  - takes in a number of copies to restock and adds it to the total number of copies.
  - if no argument is passed, default the restock number to five.

- List of
  - USE JavaScript classes
  - Use a getter method

### My Solution

```typescript
interface BookType {
  title: string;
  author: string;
  ISBN: unknown;
  numCopies: number;
}

class Book implements BookType {
  title: string = "";
  author: string = "";
  ISBN: unknown;
  numCopies: number = 5;

  constructor(title: string, author: string, ISBN: number, numCopies: number) {
    this.title = title;
    this.author = author;
    this.ISBN = ISBN;
    this.numCopies = numCopies;
  }

  getAvailablity() {
    if (this.numCopies <= 0) {
      console.log("OUT OF STOCK");
    } else if (this.numCopies < 10) {
      console.log("Low stocks");
    } else {
      console.log("IN STOCK");
    }
  }

  sell(num: number = 1) {
    this.numCopies -= num;
    console.log(this.numCopies);
  }

  reStock(num: number = 5) {
    this.numCopies += num;
    console.log(this.numCopies);
  }
}

const book1 = new Book("Hunger Games", "Suzanne Collins", 123919, 3);
book1.getAvailablity();
book1.sell(5);
book1.reStock(5);
```
