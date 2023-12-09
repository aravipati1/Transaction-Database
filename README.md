# README for InMemoryDB

## Overview
The InMemoryDB class is a simple in-memory database implementation in Python, providing basic functionalities such as storing key-value pairs, and supporting transactions including begin, commit, and rollback.

## Features
- `get(key)`: Retrieve the value for a given key.
- `put(key, value)`: Store the key-value pair.
- `begin_transaction()`: Start a new transaction.
- `commit()`: Commit the current transaction.
- `rollback()`: Rollback the current transaction.

## How to Run the Code

### Prerequisites
Ensure that you have Python installed on your system. The code is compatible with Python 3.x. No external libraries are required.

### Setup
1. Save the provided Python code in a file, e.g., `in_memory_db.py`.
2. You can use any text editor or Python IDE.

### Running the Code
1. Open a terminal or command prompt.
2. Navigate to the directory where the `in_memory_db.py` file is saved.
3. Run the script using Python. For example:
   ```bash
   python in_memory_db.py
   ```
   (Note: This step will not produce any output as the script contains only class definitions. You need to create a script that imports and uses this class to see it in action.)

### Example Usage
Create a new Python script in the same directory, e.g., `test_db.py`. In this script, you can import the `InMemoryDB` class and use it as follows:

```python
from in_memory_db import InMemoryDB

# Create an instance of InMemoryDB
db = InMemoryDB()

# Start a transaction
db.begin_transaction()

# Perform operations
db.put("key1", "value1")
print(db.get("key1"))  # Output: value1

# Commit the transaction
db.commit()

# Trying to get the value after commit
print(db.get("key1"))  # Output: value1

# Start another transaction
db.begin_transaction()

# Perform more operations
db.put("key2", "value2")
print(db.get("key2"))  # Output: value2

# Rollback this transaction
db.rollback()

# Trying to get the value after rollback
print(db.get("key2"))  # Output: None
```

Run this script as described above to test the functionality of the InMemoryDB class.

### Note
- The class does not persist data to disk; all data is lost when the program exits.
- Exception handling is built into the methods to ensure proper usage of transactions.

# This assignment could be improved and made an official assignment with better and more simplistic directions. As of right now, this assignment seems very vague and it would be confusing for
# students that are encountering it as an official assignment. To make it more streamlined and specific, you could define the data types for the assignment by explicitly stating the expected data types for keys and values.
# Additionally, this assignment would benefit with a better grading criteria, such as considering more aspects of the code such as code quality, functionality, efficiency, and robustness.
