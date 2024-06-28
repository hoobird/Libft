# Libft

## Your very first own library

### Description
Libft is a project aimed at creating a custom C library containing a variety of general-purpose functions. This library will be an essential tool for future C programming assignments, providing implementations of standard functions as well as additional utilities.

### Requirements
- C compiler (e.g., `gcc`)
- Makefile
- Git for version control

### Functions

#### Part 1 - Libc Functions
| Prototype | Description |
|-----------|-------------|
| `int ft_toupper(int c);` | Converts a lowercase letter to uppercase. |
| `int ft_isalpha(int c);` | Checks if a character is an alphabetic letter. |
| `int ft_isdigit(int c);` | Checks if a character is a digit (0-9). |
| `int ft_tolower(int c);` | Converts an uppercase letter to lowercase. |
| `int ft_isalnum(int c);` | Checks if a character is an alphanumeric character. |
| `int ft_isascii(int c);` | Checks if a character is an ASCII character. |
| `int ft_isprint(int c);` | Checks if a character is printable. |
| `size_t ft_strlen(const char *s);` | Calculates the length of a string. |
| `char *ft_strchr(const char *s, int c);` | Locates the first occurrence of a character in a string. |
| `char *ft_strrchr(const char *s, int c);` | Locates the last occurrence of a character in a string. |
| `int ft_strncmp(const char *s1, const char *s2, size_t n);` | Compares two strings up to `n` characters. |
| `void *ft_memset(void *b, int c, size_t len);` | Fills memory with a constant byte. |
| `void ft_bzero(void *s, size_t n);` | Sets all bytes in a block of memory to zero. |
| `void *ft_memchr(const void *s, int c, size_t n);` | Locates a byte in a block of memory. |
| `void *ft_memcpy(void *dst, const void *src, size_t n);` | Copies memory from source to destination. |
| `int ft_memcmp(const void *s1, const void *s2, size_t n);` | Compares two blocks of memory. |
| `void *ft_memmove(void *dst, const void *src, size_t len);` | Moves memory from source to destination. |
| `char *ft_strnstr(const char *haystack, const char *needle, size_t len);` | Locates a substring in a string, with a length limit. |
| `size_t ft_strlcpy(char *dst, const char *src, size_t dstsize);` | Copies a string to a buffer, ensuring null-termination. |
| `size_t ft_strlcat(char *dst, const char *src, size_t dstsize);` | Appends a string to a buffer, ensuring null-termination. |
| `int ft_atoi(const char *str);` | Converts a string to an integer. |
| `void *ft_calloc(size_t count, size_t size);` | Allocates memory and initializes it to zero. |
| `char *ft_strdup(const char *s1);` | Duplicates a string, allocating memory for the new string. |

#### Part 2 - Additional Functions
| Prototype | Description |
|-----------|-------------|
| `char *ft_substr(char const *s, unsigned int start, size_t len);` | Allocates and returns a substring from the string `s`. The substring begins at index `start` and is of maximum size `len`. |
| `char *ft_strjoin(char const *s1, char const *s2);` | Allocates and returns a new string, which is the result of the concatenation of `s1` and `s2`. |
| `char *ft_strtrim(char const *s1, char const *set);` | Allocates and returns a copy of `s1` with the characters specified in `set` removed from the beginning and the end of the string. |
| `char **ft_split(char const *s, char c);` | Allocates and returns an array of strings obtained by splitting `s` using the character `c` as a delimiter. The array must end with a NULL pointer. |
| `char *ft_itoa(int n);` | Allocates and returns a string representing the integer `n`. Negative numbers must be handled. |
| `char *ft_strmapi(char const *s, char (*f)(unsigned int, char));` | Applies the function `f` to each character of the string `s`, passing its index as the first argument and the character itself as the second. Allocates and returns a new string resulting from the successive applications of `f`. |
| `void ft_striteri(char *s, void (*f)(unsigned int, char*));` | Applies the function `f` on each character of the string passed as an argument, passing its index as the first argument. Each character is passed by address to `f` to be modified if necessary. |
| `void ft_putchar_fd(char c, int fd);` | Outputs the character `c` to the given file descriptor. |
| `void ft_putstr_fd(char *s, int fd);` | Outputs the string `s` to the given file descriptor. |
| `void ft_putendl_fd(char *s, int fd);` | Outputs the string `s` to the given file descriptor, followed by a newline. |
| `void ft_putnbr_fd(int n, int fd);` | Outputs the integer `n` to the given file descriptor. |

#### Bonus Functions (List Manipulation)
| Prototype | Description |
|-----------|-------------|
| `t_list *ft_lstnew(void *content);` | Allocates and returns a new node. The member variable `content` is initialized with the value of the parameter `content`. The variable `next` is initialized to NULL. |
| `void ft_lstadd_front(t_list **lst, t_list *new);` | Adds the node `new` at the beginning of the list. |
| `int ft_lstsize(t_list *lst);` | Counts the number of nodes in a list. |
| `t_list *ft_lstlast(t_list *lst);` | Returns the last node of the list. |
| `void ft_lstadd_back(t_list **lst, t_list *new);` | Adds the node `new` at the end of the list. |
| `void ft_lstdelone(t_list *lst, void (*del)(void *));` | Takes as a parameter a node and frees the memory of the node’s content using the function `del` given as a parameter and free the node. The memory of `next` must not be freed. |
| `void ft_lstclear(t_list **lst, void (*del)(void *));` | Deletes and frees the given node and every successor of that node, using the function `del` and `free(3)`. Finally, the pointer to the list must be set to NULL. |
| `void ft_lstiter(t_list *lst, void (*f)(void *));` | Iterates the list `lst` and applies the function `f` on the content of each node. |
| `t_list *ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *));` | Iterates the list `lst` and applies the function `f` on the content of each node. Creates a new list resulting from the successive applications of the function `f`. The `del` function is used to delete the content of a node if needed. |

### How to Run

1. **Clone the Repository**
   ```bash
   git clone <repository_url>
   cd libft
   ```

2. **Compile the Library**
   - Run the following command to compile the basic library:
     ```bash
     make all
     ```
   - Run the following command to compile the basic + bonus library:
       ```bash
       make bonus
       ```
   - Run the following command to compile the basic + bonus + getnextline library:
     ```bash
     make new
     ```
3. **Library libft.a will be created** 
