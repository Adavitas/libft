# 📚 Libft

### Your very first own library - A collection of essential C functions recreated from scratch

[![42 School](https://img.shields.io/badge/42-School-000000?style=for-the-badge&logo=42&logoColor=white)](https://42.fr/)
[![Language](https://img.shields.io/badge/Language-C-blue?style=for-the-badge&logo=c)](https://en.wikipedia.org/wiki/C_(programming_language))
[![Norminette](https://img.shields.io/badge/Norminette-passing-success?style=for-the-badge)](https://github.com/42School/norminette)
[![Grade](https://img.shields.io/badge/Grade-125%2F100-success?style=for-the-badge)](https://github.com/Adavitas/libft)

---

## 📋 Table of Contents

• [About](#-about) • [Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Function Overview](#-function-overview) • [Bonus Functions](#-bonus-functions) • [Makefile Commands](#%EF%B8%8F-makefile-commands) • [Testing](#-testing) • [Author](#-author)

---

## 🎯 About

**Libft** is the first project in the 42 School curriculum - recreating standard C library functions from scratch plus additional utility functions. This library serves as your personal toolkit throughout the 42 journey.

**Key Learning Goals:**
• Understanding standard C library internals • Memory management and pointer manipulation • Clean, reusable code • Foundation for all future C projects

---

## ✨ Features

| **Core Functionality** | **Bonus Features** |
|------------------------|-------------------|
| ✅ 43 Standard libc functions | ✅ Linked list operations |
| ✅ String & memory manipulation | ✅ Dynamic list management |
| ✅ Character checking & conversion | ✅ List iteration & mapping |
| ✅ File descriptor output | ✅ Memory-safe list handling |

---

## 🚀 Installation

```bash
# Clone and compile
git clone https://github.com/Adavitas/libft.git
cd libft
make        # Creates libft.a
make bonus  # Includes bonus functions
```

---

## 💻 Usage

### Basic Integration
```c
#include "libft.h"

// Compile with: gcc -Wall -Wextra -Werror your_file.c -L. -lft -o program
```

### Quick Examples
```c
// String manipulation
char *sub = ft_substr("Hello, 42!", 7, 2);        // "42"
char **split = ft_split("one,two,three", ',');    // ["one", "two", "three"]

// Memory & conversion
char *num = ft_itoa(-42);                         // "-42"
int value = ft_atoi("  -123abc");                 // -123

// Linked list (bonus)
t_list *list = ft_lstnew("First");
ft_lstadd_back(&list, ft_lstnew("Second"));
```

---

## 📖 Function Overview

### Part 1 - Libc Functions (23 functions)

| Category | Functions |
|----------|-----------|
| **Character Checks** | `ft_isalpha` `ft_isdigit` `ft_isalnum` `ft_isascii` `ft_isprint` |
| **String Operations** | `ft_strlen` `ft_strchr` `ft_strrchr` `ft_strncmp` `ft_strnstr` `ft_strlcpy` `ft_strlcat` `ft_strdup` |
| **Memory Functions** | `ft_memset` `ft_bzero` `ft_memcpy` `ft_memmove` `ft_memchr` `ft_memcmp` `ft_calloc` |
| **Conversions** | `ft_atoi` `ft_toupper` `ft_tolower` |

### Part 2 - Additional Functions (11 functions)

| Category | Functions |
|----------|-----------|
| **String Creation** | `ft_substr` `ft_strjoin` `ft_strtrim` `ft_split` `ft_itoa` |
| **String Apply** | `ft_strmapi` `ft_striteri` |
| **File Output** | `ft_putchar_fd` `ft_putstr_fd` `ft_putendl_fd` `ft_putnbr_fd` |

---

## 🌟 Bonus Functions

### Linked List Structure
```c
typedef struct s_list
{
    void            *content;
    struct s_list   *next;
}                   t_list;
```

### Functions (9 functions)
`ft_lstnew` `ft_lstadd_front` `ft_lstadd_back` `ft_lstsize` `ft_lstlast` `ft_lstdelone` `ft_lstclear` `ft_lstiter` `ft_lstmap`

---

## 🛠️ Makefile Commands

| Command | Description |
|---------|-------------|
| `make` | Compile mandatory functions |
| `make bonus` | Compile with bonus functions |
| `make clean` | Remove object files |
| `make fclean` | Remove objects and library |
| `make re` | Rebuild everything |

**Compilation:** `-Wall -Wextra -Werror`

---

## 🧪 Testing

### Quick Test
```c
#include "libft.h"
#include <stdio.h>

int main(void)
{
    printf("strlen: %zu\n", ft_strlen("Hello"));
    printf("atoi: %d\n", ft_atoi("-42"));
    
    char *str = ft_itoa(-12345);
    printf("itoa: %s\n", str);
    free(str);
    
    char **split = ft_split("one,two,three", ',');
    for (int i = 0; split[i]; i++)
    {
        printf("split[%d]: %s\n", i, split[i]);
        free(split[i]);
    }
    free(split);
    return (0);
}
```

### Recommended Testers
- **[Francinette](https://github.com/xicodomingues/francinette)** - Comprehensive 42 tester
- **[libft-unit-test](https://github.com/alelievr/libft-unit-test)** - Unit testing
- **[Tripouille](https://github.com/Tripouille/libftTester)** - Popular tester
- **Valgrind** - Memory leak detection

---

## 👨‍💻 Author

**Aleksandre Davitashvili (Adavitas)** - 42 Wolfsburg Student

[![GitHub](https://img.shields.io/badge/GitHub-Adavitas-181717?style=for-the-badge&logo=github)](https://github.com/Adavitas)

---

## 📝 License

This project is part of the 42 School curriculum.

---

<div align="center">

### Made with ❤️ at 42 Wolfsburg

![42 Wolfsburg](https://img.shields.io/badge/42-Wolfsburg-000000?style=for-the-badge&logo=42&logoColor=white)

</div>
