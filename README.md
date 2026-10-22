# xv6 Operating System Kernel Modification: Lazy Page Allocator ⚙️

An Operating System kernel modification project implementing a **Lazy Page Allocator** in the xv6 OS kernel using C and Vim in the terminal.

This project replaces default eager heap allocation with dynamic on-demand page fault handling, optimizing memory management and system resource efficiency.

---

## 🛠️ Features & Technical Details

* **Lazy Memory Allocation:** Intercepts `sbrk()` system calls so physical memory allocation is deferred until virtual memory pages are actually accessed.
* **Page Fault Handler:** Modified the kernel trap handler (`trap.c`) to handle page faults (`T_PGFLT`), allocate physical pages dynamically, and build page table mappings (`mappages()`).
* **Dual Allocator Support:** Integrated kernel system calls (`set_page_allocator()`) to dynamically toggle between the **DEFAULT** eager allocator and the **LAZY** allocator.
* **Core Kernel Files Modified:**
  * `proc.c` & `sysproc.c`: Adjusted process heap resizing logic (`growproc()`).
  * `trap.c`: Added trap logic to catch page faults and allocate pages on demand.
  * `vm.c`: Configured memory mapping routines (`allocuvm()`, `mappages()`).

---

## 🧪 Testing & Execution

The project includes custom user-space test suites (`proj2_test.c`) to verify memory growth, page fault triggering, page frame consumption, and invalid boundary protection.

### Running the Test Suite in xv6

Due to how state persists across test runs, tests should be executed in one of the following two supported sequences:

* **Sequence 1 (Direct Sequential Run):**
  ```bash
  proj2_test 0
  proj2_test 1
