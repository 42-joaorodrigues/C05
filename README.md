# C Piscine - C05

![42 Badge](https://img.shields.io/badge/42-C_Piscine-brightgreen)
![C Badge](https://img.shields.io/badge/Language-C-blue)
![Status Badge](https://img.shields.io/badge/Status-Completed-success)

## What I Learned

Through this C05 module at 42 School, I developed essential programming skills focusing on recursion and mathematical algorithms:

- **Recursion mastery** - Learned to think recursively and implement elegant recursive solutions
- **Iterative vs recursive approaches** - Compared performance and readability of both paradigms
- **Mathematical algorithm implementation** - Built factorial, power, Fibonacci, and prime number functions
- **Edge case handling** - Managed invalid inputs, negative numbers, and boundary conditions
- **Algorithm optimization** - Implemented efficient square root and prime checking algorithms
- **Complex problem solving** - Tackled the Ten Queens puzzle using backtracking recursion
- **Memory efficiency** - Understood stack usage implications of recursive calls
- **Input validation** - Implemented robust error checking for mathematical edge cases
- **Algorithmic thinking** - Developed systematic approaches to breaking down complex problems
- **Code clarity** - Wrote clean, readable implementations of mathematical concepts

This module strengthened my understanding of fundamental algorithms and recursive problem-solving techniques essential for advanced programming challenges.

## About the Project

C05 is a module focused on recursion and mathematical algorithms. It challenges students to implement both iterative and recursive versions of common mathematical functions, culminating in a complex backtracking algorithm for the Ten Queens puzzle.

## Implementation Details

The module consists of 9 exercises that progressively increase in complexity:

### Mathematical Functions

| Exercise | Function | Type | Description |
|----------|----------|------|-------------|
| ex00 | `ft_iterative_factorial` | Iterative | Calculate factorial using loops |
| ex01 | `ft_recursive_factorial` | Recursive | Calculate factorial using recursion |
| ex02 | `ft_iterative_power` | Iterative | Calculate power using loops |
| ex03 | `ft_recursive_power` | Recursive | Calculate power using recursion |

### Advanced Algorithms

| Exercise | Function | Description |
|----------|----------|-------------|
| ex04 | `ft_fibonacci` | Generate nth Fibonacci number recursively |
| ex05 | `ft_sqrt` | Find integer square root or return 0 |
| ex06 | `ft_is_prime` | Check if a number is prime |
| ex07 | `ft_find_next_prime` | Find next prime number >= given value |
| ex08 | `ft_ten_queens_puzzle` | Solve Ten Queens puzzle using backtracking |

## Function Prototypes

```c
// Mathematical operations
int ft_iterative_factorial(int nb);
int ft_recursive_factorial(int nb);
int ft_iterative_power(int nb, int power);
int ft_recursive_power(int nb, int power);

// Advanced algorithms
int ft_fibonacci(int index);
int ft_sqrt(int nb);
int ft_is_prime(int nb);
int ft_find_next_prime(int nb);
int ft_ten_queens_puzzle(void);
```

## Key Concepts Implemented

### Factorial Functions (ex00, ex01)
- **Iterative approach**: Uses loops for calculation
- **Recursive approach**: Self-calling function with base case
- **Edge cases**: Returns 0 for negative inputs
- **Overflow handling**: Undefined behavior for large inputs

### Power Functions (ex02, ex03)
- **Special case**: 0^0 = 1 by convention
- **Negative powers**: Returns 0 for negative exponents
- **Optimization**: Early termination for power of 0

### Fibonacci Sequence (ex04)
- **Recursive implementation**: Must use recursion as specified
- **Sequence definition**: Starts with 0, 1, 1, 2, ...
- **Error handling**: Returns -1 for negative indices
- **Base cases**: Handles index 0 and 1 explicitly

### Square Root (ex05)
- **Integer-only result**: Returns 0 if no perfect square
- **Efficient algorithm**: Avoids floating-point operations
- **Edge cases**: Handles negative inputs appropriately

### Prime Number Functions (ex06, ex07)
- **Primality testing**: Optimized algorithm checking up to √n
- **Edge cases**: 0 and 1 are not considered prime
- **Next prime**: Finds smallest prime ≥ input value

### Ten Queens Puzzle (ex08)
- **Backtracking algorithm**: Complex recursive solution
- **Constraint satisfaction**: No two queens can attack each other
- **Output format**: Displays all valid solutions as digit sequences
- **Return value**: Total number of solutions found

## Usage Examples

```c
#include <stdio.h>

// Example usage of the functions
int main(void)
{
    // Factorial examples
    printf("5! = %d\n", ft_iterative_factorial(5));    // Output: 120
    printf("5! = %d\n", ft_recursive_factorial(5));     // Output: 120
    
    // Power examples
    printf("2^8 = %d\n", ft_iterative_power(2, 8));     // Output: 256
    printf("2^8 = %d\n", ft_recursive_power(2, 8));     // Output: 256
    
    // Fibonacci example
    printf("F(10) = %d\n", ft_fibonacci(10));           // Output: 55
    
    // Square root example
    printf("√16 = %d\n", ft_sqrt(16));                  // Output: 4
    printf("√15 = %d\n", ft_sqrt(15));                  // Output: 0
    
    // Prime examples
    printf("Is 17 prime? %d\n", ft_is_prime(17));       // Output: 1
    printf("Next prime ≥ 14: %d\n", ft_find_next_prime(14)); // Output: 17
    
    // Ten Queens puzzle
    int solutions = ft_ten_queens_puzzle();
    printf("Total solutions: %d\n", solutions);          // Output: 724
    
    return (0);
}
```

## Technical Challenges Overcome

- **Recursion depth management** - Understanding stack limitations and optimizing recursive calls
- **Mathematical edge cases** - Handling special cases like 0^0, negative inputs, and overflow conditions
- **Algorithm efficiency** - Implementing optimized versions of mathematical operations
- **Backtracking complexity** - Mastering the Ten Queens puzzle's constraint satisfaction algorithm
- **Input validation** - Ensuring robust error handling for all mathematical functions
- **Code readability** - Balancing algorithmic efficiency with clear, maintainable code

## Compilation

```bash
# Compile individual exercises
cc -Wall -Wextra -Werror ex00/ft_iterative_factorial.c -o factorial
cc -Wall -Wextra -Werror ex08/ft_ten_queens_puzzle.c -o ten_queens

# Run Ten Queens puzzle
./ten_queens | head -10  # Show first 10 solutions
```

## Algorithm Complexity

| Function | Time Complexity | Space Complexity |
|----------|----------------|------------------|
| Factorial (iterative) | O(n) | O(1) |
| Factorial (recursive) | O(n) | O(n) |
| Power (iterative) | O(p) | O(1) |
| Power (recursive) | O(p) | O(p) |
| Fibonacci | O(2^n) | O(n) |
| Square root | O(√n) | O(1) |
| Prime check | O(√n) | O(1) |
| Ten Queens | O(n!) | O(n) |

---

*This project was completed as part of the 42 School C Piscine, demonstrating proficiency in recursive programming, mathematical algorithms, and complex problem-solving techniques.*

---

## License

This project is licensed under the [MIT License](./LICENSE).
