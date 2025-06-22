
# 🔒 Singleton Pattern

### 🧠 Intent:
Ensure a class has only one instance and provide a global access point to it.

---

### 🛠️ Real-life Example:
Printer class in an office – only one printer instance is used by all employees.

---

### ✅ Use Case:
- Logger
- DB Connection Pool
- Configuration Manager

---

### 💡 Key Idea:
- Private constructor
- Static method for instance
- Lazy initialization

---

### 💻 Code (Python)

```python
class Singleton:
    _instance = None

    def __new__(cls):
        if cls._instance is None:
            cls._instance = super(Singleton, cls).__new__(cls)
        return cls._instance
