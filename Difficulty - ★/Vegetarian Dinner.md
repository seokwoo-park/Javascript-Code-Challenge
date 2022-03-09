# Available books

## Difficulty ★☆☆☆☆ (_Completed_)

### Summary

> Arrays come with many built-in loops and functions that
> allow us to manipulate data.
>
> One of those functions is the array _.filter_ method.
>
> _.filter_ method, it's a callback function that gets run once for every item in array and overturns a new array of items that pass a certain criteria.

### Requirement

- some of customers need a vegetarian menu.
  - create a list of vegetarian menu items for them.
  - Each menu item is an object containing the dish name
  - a Boolean variable that indicates wheter dish is vegetarian
- You should dynamically generate the list items in the DOM

### My Solution

```typescript
interface DishType {
  name: string;
  vegetarian: boolean;
}

const dishes: DishType[] = [
  {
    name: "spaghetti",
    vegetarian: true,
  },
  {
    name: "Pork-ribs",
    vegetarian: false,
  },
  {
    name: "pizza",
    vegetarian: true,
  },
  {
    name: "Burger",
    vegetarian: false,
  },
  {
    name: "Sushi",
    vegetarian: true,
  },
];

function allMenuGenerator() {
  const allMenuNode = document.querySelector(".allMenu");
  dishes.forEach((item) => {
    const li = document.createElement("li");
    allMenuNode?.appendChild(li);
    li.innerHTML = item.name;
  });
}

function vegeMenuGenerator() {
  const veganMenu = dishes.filter((item) => item.vegetarian);
  const vegeMenuNode = document.querySelector(".vegeMenu");
  veganMenu.forEach((item) => {
    const li = document.createElement("li");
    vegeMenuNode?.appendChild(li);
    li.innerHTML = item.name;
  });
}

allMenuGenerator();
vegeMenuGenerator();
```
