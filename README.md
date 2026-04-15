# PES Version Control System (PES-VCS) Lab Report

## Overview

This project implements a simplified version control system similar to Git. It supports:

* Content-addressable object storage
* Tree-based directory structure
* Staging area (index)
* Commit creation and history tracking
* Log traversal

---

## Phase 1: Object Storage

### Description

In this phase, we implemented a content-addressable object store using SHA-256 hashing. Each object is stored based on its hash in `.pes/objects`.

---

### Screenshot 1A: Test Objects Output

![Phase 1A](screenshots/p1a.jpeg)

---

### Screenshot 1B: Object Directory Structure

![Phase 1B](screenshots/p1b.jpeg)

---

##  Phase 2: Tree Objects

### Description

Tree objects represent directory structures. Each tree contains entries mapping filenames to object hashes.

---

### Screenshot 2A: Tree Test Output

![Phase 2A](screenshots/p2a.jpeg)

---

### Screenshot 2B: Raw Tree Object (xxd)

![Phase 2B](screenshots/p2b.jpeg)

---

## Phase 3: Index (Staging Area)

### Description

The index acts as a staging area, tracking files before committing. It stores file metadata and hashes.

---

### Screenshot 3A: pes init → add → status
![Phase 3A](screenshots/p3a.jpeg)


---

### Screenshot 3B: Index File Contents
![Phase 3B](screenshots/p3b.jpeg)


---

## Phase 4: Commits & History

### Description

Commits capture snapshots of the project. Each commit stores:

* Tree reference
* Parent commit
* Author and timestamp
* Commit message

---

### Screenshot 4A: Commit Log

![Phase 4A](screenshots/p4a.jpeg)

---

### Screenshot 4B: Object Growth

![Phase 4B](screenshots/p4b.jpeg)

---

### Screenshot 4C: HEAD and Branch Reference

![Phase 4C](screenshots/p4c.jpeg)

---

## Analysis Questions

### Q5.1: What is Branching?

Branching allows multiple lines of development by creating pointers to commits. It enables independent development without duplicating data.

---

### Q5.2: How does branching work internally?

Branches are simply references (pointers) to commits. When a new commit is made, the branch pointer moves forward to the new commit.

---

### Q5.3: Advantages of branching

* Parallel development
* Easy feature testing
* Safe experimentation without affecting main code

---

### Q6.1: What is Garbage Collection?

Garbage collection removes objects that are no longer reachable from any commit or reference, freeing storage.

---

### Q6.2: Why is Garbage Collection needed?

Over time, unused objects accumulate (e.g., deleted commits). Garbage collection ensures efficient storage usage.

---

## Conclusion

This project demonstrates the core principles of version control systems:

* Efficient storage using hashing
* Snapshot-based commits
* Branching through references
* History traversal

The implementation successfully mimics key Git functionalities in a simplified manner.

---
