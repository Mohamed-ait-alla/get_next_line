# get_next_line

`get_next_line` is a 42 school project that implements a function to read a file line by line from a given file descriptor.  
The function returns each line of text, one at a time, including the newline character, and handles reading across multiple calls efficiently.

---

## 📌 Function Prototype

   ```
    char *get_next_line(int fd);
   ```

- **fd:** The file descriptor to read from.
- **Return**: returns the line readed,  or `NULL` if there are no more lines or an error occurs.

## 🧠 Concepts Covered
- **File I/O with read() system call function**
- **Managing a static buffer across function calls**
- **Dynamic memory allocation**
- **Handling edge cases (EOF, no newline, very long lines)**
- **Manual string manipulation**

## 🛠️ Usage

1. **clone the repository:**
```bash
 git clone https://github.com/Mohamed-ait-alla/get_next_line.git
 cd get_next_line
```
2. **compile code:**
