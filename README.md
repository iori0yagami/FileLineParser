How It Works
Buffer Management: The function uses a buffer to store data read from the file descriptor in chunks. A static variable (or similar mechanism) keeps track of where the previous read stopped, ensuring the function can continue reading from where it left off.

Dynamic Memory Allocation: For each line, the function allocates memory dynamically to hold the string. This ensures that each line returned is independently stored and can be freed after use.

Handling Multiple Calls: The function can be called multiple times on the same file descriptor, and each call will return a single line from the file until the end of the file is reached.

Edge Case Handling:

Files with no newlines or multiple newlines.
Empty lines or lines with just a newline character.
End of file condition (EOF).
Memory management to avoid leaks.
Functionality
The core function get_next_line has the following features:

Reads lines: Each call to the function returns a single line from the file.
Handles EOF: Returns 0 when the end of the file is reached.
Error Handling: Returns -1 if an error occurs during reading.
Memory Efficient: Allocates memory only as needed for each line and frees it after use.
Contributing
Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

Acknowledgments
Thanks to 42 for creating this challenging and fun project.
Inspiration from various file I/O functions and memory management tutorials.
