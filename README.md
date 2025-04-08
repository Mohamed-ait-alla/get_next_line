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

1. **Clone the repository:**
```bash
 git clone https://github.com/Mohamed-ait-alla/get_next_line.git
 cd get_next_line
```
2. **Include the header file:**
```c
#include "includes/get_next_line.h"
```
3. **Compile you file with `get_next_line` sources:**
```bash
cc -Wall -Wextra -Werror your_file.c srcs/get_next_line.c srcs/get_next_line_utils.c -o your_program
```
💡 You can define `BUFFER_SIZE` at compile time if needed:
```bash
cc -D BUFFER_SIZE=42 -Wall -Wextra -Werror your_file.c srcs/get_next_line.c srcs/get_next_line_utils.c -o your_program
```
### Example of your_file.c
```c
#include "includes/get_next_line.h"

int main() {
    int fd = open("example.txt", O_RDONLY);
    char *line;

    while ((line = get_next_line(fd)) != NULL) {
        printf("%s\n", line);
        free(line);
    }

    close(fd);
    return 0;
}
```
This will read example.txt line by line and print each line to the console.
## 🚀 Bonus Part

- Handle **multiple file descriptors** at the same time without interfering with each other.
- Use **only one static variable** to manage the state for all file descriptors.
## 🏁 License
This project is part of the 42 School curriculum.
