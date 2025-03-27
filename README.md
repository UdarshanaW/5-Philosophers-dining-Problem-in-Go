# 5-Philosophers-dining-Problem-in-Go
Solution to 5 philosophers dining problem using a host channel in Go

Dining Philosophers Problem in Go

Overview
This project is an implementation of the classic Dining Philosophers Problem in Go, with some constraints and modifications:

- Five philosophers share five chopsticks.
- Each philosopher eats only three times.
- Chopsticks are picked up in any order (not the lowest-numbered first).
- Philosophers require permission from a host, which controls concurrency.
- The host allows a maximum of two philosophers to eat simultaneously.

Features
1. Deadlock-Free: The implementation ensures deadlock-free execution by controlling concurrency through a host goroutine.
2. Finite Eating: Each philosopher eats exactly three times before completing.
3. Flexible Chopstick Locking: Chopsticks are not locked in a predefined order.
4. Concurrency Control: A host goroutine allows only two philosophers to eat concurrently using a channel mechanism.

Requirements
- Go Programming Language: Make sure you have Go installed on your machine. You can download it from golang.org.

How to Run
1. Clone this repository or copy the code.
2. Save the code in a file named main.go.
3. Open a terminal and navigate to the directory containing main.go.
4. Run the program with:
   go run main.go
5. Observe the output as philosophers eat and release chopsticks.

Output Format
The output shows when a philosopher starts and finishes eating. For example:
starting to eat 1
finishing eating 1
starting to eat 2
finishing eating 2
...

Key Components
- Philosopher Struct: Encapsulates a philosopher's attributes such as ID, chopsticks, meals eaten, and the host's permission channel.
- Chopstick Struct: Represents a chopstick as a sync.Mutex.
- Host Goroutine: Manages concurrency by using a channel to allow only two philosophers to eat simultaneously.

Constraints
- Philosophers can eat only three times.
- A maximum of two philosophers can eat concurrently.

Notes
- The program avoids deadlocks and starvation.
- Philosophers pick up chopsticks in an arbitrary order.

License
This project is open-source and can be modified or distributed under the MIT License.
