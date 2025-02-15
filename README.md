# Uncommon Go Error: Panic from accessing uninitialized map

This repository demonstrates a common, yet often overlooked, error in Go: accessing a map without checking for nil.  Attempting to assign or read from a nil map results in a runtime panic.

The `bug.go` file showcases the problematic code.  The solution, provided in `bugSolution.go`, highlights how to safely handle maps to prevent unexpected panics.

This is a subtle error that can be easily missed, particularly in larger codebases.  Always check if a map is initialized before accessing it to avoid these types of crashes.

## How to Reproduce

1. Clone the repository.
2. Navigate to the project directory.
3. Run `go run bug.go`.  This will result in a runtime panic.
4. Run `go run bugSolution.go`. This demonstrates the safe way to handle map access.
