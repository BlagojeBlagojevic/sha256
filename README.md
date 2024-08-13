
---

# SHA-256 Hash Implementation

This project provides a C implementation of the SHA-256 hashing algorithm. SHA-256 is part of the SHA-2 family of cryptographic hash functions and is widely used for secure data hashing and digital signatures.

## Features

- **SHA-256 Algorithm**: Implements the SHA-256 hash function as defined by the [SHA-2 standard](https://en.wikipedia.org/wiki/SHA-2).
- **Inline Functions**: Provides efficient hash computation using inline functions.
- **Error Handling**: Includes basic error handling for memory allocation issues.

## File Overview

### `hash.h`

- **Header File**: Contains definitions, macro functions, and function prototypes for the SHA-256 hash implementation.
- **Macros**: Defines helper macros for bitwise operations, rotations, and bit manipulation.
- **Types**: Defines the `HASH_CTX` structure for maintaining the state of the hash computation.



- **SHA-256 Functions**:
  - `HASH_Init()`: Initializes the hash context.
  - `HASH_Transform()`: Processes a 512-bit block of data.
  - `HASH_Update()`: Updates the hash context with new data.
  - `HASH_Final()`: Finalizes the hash computation and produces the final hash value.
  - `HASH()`: Convenience function to hash a string and return the hash as a hexadecimal string.

## Usage

To use the SHA-256 hashing functions in your C project:

1. **Include the Header File**:

   ```c
   #define HASH_IMPLEMENTATION
   #include "hash.h"
   ```

2. **Hash a String**:

   ```c
   #include <stdio.h>
   #include <stdlib.h>
   #include <string.h>
   #include "hash.h"

   int main() {
       char *input = "Hello, world!";
       char *hashStr = HASH(input);
       printf("Hash: %s\n", hashStr);
       free(hashStr);
       return EXIT_SUCCESS;
   }
   ```

## Compilation

To compile the code:

```bash
gcc -o hash_program hash.c -O2
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Wikipedia - SHA-2](https://en.wikipedia.org/wiki/SHA-2): For the detailed explanation of SHA-256.
  
---

