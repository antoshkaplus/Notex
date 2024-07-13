* Mutual Exclusion - Critical sections of different threads do not overlap.
* Freedom from Deadlock - If some thread attmpts to acquire the lock, then some thread will 
    succeed in acquiring the lock
* Freedom from Starvation - Every thread that attmpts to acquire the lock eventually succeeds.

### Concurrent Objects:
* Objects or fields that are accessed independently should be aligned and padded 
  so that they end up on different cache lines.
* If a lock protects data that is frequently modified then keep the lock and the data on
  distinct cache lines, so that threads trying to aquire the lock do not interfere 
  with the lock-holders access to the data.
* Split object into thread-local pieces.
* Read-only fields should separate from fields modified frequently
  (if list modified frequently - align and pad to fit cache line).
* If a lock protects data that is frequently uncontended, then try to
  keep the lock and the data on the same cache line.
* The performance of multiprocessor programs is highly dependent on
  synergy with underlying hardware.

### Correctness conditions:
* Quiescent consistency 
* Sequencial consistency
* Linerizability

### Progress guarantees:
* blocking
* nonblocking

### Function:
* precondition - describes object state before invoking the method
* postcondition -  describes, once method returns, the object's state and return value
* side effect - a change in object's state.