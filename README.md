Java Thread Synchronization

This project demonstrates multithreading and synchronization in Java. It simulates concurrent deposits and withdrawals on shared bank accounts while ensuring data consistency through synchronized methods and synchronized blocks.

Overview
The application creates multiple threads that operate on shared account objects. Each account is accessed by one depositor thread and one withdrawer thread. Without synchronization, concurrent modifications lead to race conditions and incorrect balances. With proper synchronization, all accounts maintain consistent final values.

Project Structure
Task4/
  Account.java
  AccountManager.java
  Depositor.java
  Withdrawer.java
  before.txt        # Output before fixing synchronization
  after.txt         # Output after applying synchronized methods

Task5/
  Account.java
  AccountManager.java
  Depositor.java
  Withdrawer.java
  after.txt         # Output after applying synchronized blocks

Task4 Description
Task 4 uses method-level synchronization. All methods that modify shared account data are declared "synchronized", ensuring mutual exclusion when threads access critical sections. The result is consistent account balances across all threads.

"before.txt" shows incorrect behavior without synchronization.
"after.txt" shows correct behavior after applying synchronized methods.

Task5 Description
Task 5 uses block-level synchronization. Instead of synchronizing entire methods, only the specific critical code sections are synchronized using synchronized blocks. This provides finer control and can improve performance in certain cases.

"after.txt" confirms correct behavior with synchronized blocks.

How to Run
Navigate to either Task4 or Task5 and run:

javac *.java
java AccountManager

Concepts Demonstrated
- Java concurrency and multithreading
- Race conditions and atomicity issues
- Identification of critical sections
- Method-level synchronization
- Block-level synchronization
- Differences between synchronized methods and synchronized blocks

Technologies Used
-----------------
- Java SE
- Java Threads
- Synchronized methods and blocks
