# Phase 4 — Implementing a Heap Allocator

**Target period:** March – April 2027

## Focus

Build a small allocator to understand dynamic memory management at a lower level.

## Planned work

- Define the allocator's requirements and constraints.
- Choose and document a block representation.
- Implement allocation and deallocation.
- Handle alignment and allocation failure.
- Test fragmentation and edge cases.
- Document complexity, limitations, and design trade-offs.

## Testing expectations

Include tests for zero-size requests, small and large allocations, exhaustion, invalid usage according to the chosen API contract, alignment, and repeated allocation/deallocation patterns. Use sanitizers and other host tools where appropriate.
