# Stingray.jl

## Installation and Running Tests

### Prerequisites
Make sure you have Julia 1.7.0 installed. You can download it from the following link:

[Download Julia 1.7.0](https://julialang.org/downloads/)

### Steps to Clone and Run Tests

1. **Open VS Code**
2. **Clone the Repository**
   ```sh
   git clone https://github.com/JawadAhmadCS/Stingray.jl
   ```
3. **Open the Project Folder in VS Code**
4. **Open Julia REPL**
   - Press `Ctrl + Shift + P`
   - Search for `julia:start REPL` and select it
5. **Navigate to the Cloned Repository in REPL**
   ```julia
   cd("C:\\Users\\mjawa\\Pictures\\git\\Stingray.jl")
   ```
6. **Activate and Install Dependencies**
   ```julia
   import Pkg
   Pkg.activate(".")
   Pkg.instantiate()
   ```
7. **Run Tests**
   ```julia
   using Pkg
   Pkg.test("Stingray")

# CheetSheet
```
include("docs/make.jl")
   ```

```
include("test/test_lightcurve.jl")
```
