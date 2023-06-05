# 8D-Optimised
8D Optimised
This modified code creates a larger lattice by changing the `width`, `height`, `depth`, `time`, `energy`, `dimension7`, and `dimension8` variables to 100. This will create a 100x100x100x100x100x100x100x100 lattice structure.

To improve efficiency, I made the following changes:
1. Replaced the use of `std::vector` with `std::array` for dimensions that have a fixed size (`LatticeSymbol` and the lattice dimensions).
2. Removed unnecessary copying of the encryption key by passing it by const reference instead of converting it to a vector.
3. Removed the innermost loop for iterating over the lattice symbols when finding the symbol with maximum complexity. Instead, I used a nested loop structure to directly access the symbols without the need for nested vectors.
4. Removed the sleep delay in each encryption round for improved performance.
