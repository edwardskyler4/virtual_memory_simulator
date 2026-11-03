# User-Space Virtual Memory Simulator

This project is a Rust command-line application that simulates the core behavior of a virtual memory system. It translates virtual addresses into physical frames, maintains page-table mappings, handles page faults, replaces pages when physical memory is full, and reports memory-access statistics.

The simulator is intended to demonstrate virtual memory concepts without requiring kernel development or access to specialized hardware.

The project will meet the following requirements:

1. Represent virtual addresses as page numbers and page offsets.
2. Maintain a page table that maps virtual pages to physical frames.
3. Simulate read and write memory operations.
4. Detect and handle page faults for unmapped pages.
5. Manage a fixed number of simulated physical memory frames.
6. Implement FIFO page replacement when all frames are occupied.
7. Report statistics including page faults, page hits, evictions, and total memory accesses.

## Instructions for Build and Use

Steps to build and/or run the software:

1. Install Rust and Cargo from [rustup.rs](https://rustup.rs/).
2. Clone or download the project.
3. From the project directory, build the application:

   ```bash
   cargo build
   ```

Instructions for using the software:

1. Run the application with Cargo:

   ```bash
   cargo run
   ```

2. Provide a sequence of simulated read and write operations when prompted, or use the project’s sample workload.
3. Review the address-translation output and memory-access statistics.

## Development Environment

To recreate the development environment, you need the following software and/or libraries with the specified versions:

* Rust toolchain with Cargo
* Rust edition specified in `Cargo.toml`
* A terminal capable of running command-line programs

## Useful Websites to Learn More

I found these websites useful in developing this software:

* [The Rust Programming Language](https://doc.rust-lang.org/book/)
* [Rust Standard Library Documentation](https://doc.rust-lang.org/std/)
* [Operating Systems: Three Easy Pieces — Virtual Memory](https://pages.cs.wisc.edu/~remzi/OSTEP/vm-intro.pdf)

## Future Work

The following items I plan to fix, improve, and/or add to this project in the future:

* [ ] Implement and compare an LRU page-replacement algorithm.
* [ ] Add a simulated translation lookaside buffer (TLB).
* [ ] Track and display TLB hits and misses.
* [ ] Add simulated swap space represented by a file.
