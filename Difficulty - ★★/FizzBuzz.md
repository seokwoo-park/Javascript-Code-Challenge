# Available books

## Difficulty ★★☆☆☆ (_Completed_)

### Summary

> FizzBuzz is a task where the programmer is asked to print numbers from 1 to 100, but here’s the catch,
> multiple of three should print “Fizz” and similarly print “Buzz” for multiples of 5 and lastly print “FizzBuzz” for multiples of three and five.

### Solution

```javascript
function fizzBuzz() {
  for (let i = 1; i < 101; i++) {
    const fizz = i % 3 == 0;
    const buzz = i % 5 == 0;
    const fizzBuzz = fizz && buzz;

    fizzBuzz
      ? console.log("fizzBuzz " + i)
      : fizz
      ? console.log("fizz " + i)
      : buzz
      ? console.log("buzz " + i)
      : console.log(i);
  }
}

fizzBuzz();
```

### Comment

> There's many solutions to solve 'FizzBuzz' I can't say my solution is the 100% perfect. however, it's easy and readable for me
