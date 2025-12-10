# get_next_line-_tester_berlin_2025
42 get_next_line_tester

Run your own tests!

How to use.

Complie & run:

# Test with default BUFFER_SIZE (42)
cc -Wall -Wextra -Werror -D BUFFER_SIZE=42 get_next_line.c get_next_line_utils.c main.c -o test_gnl
./test_gnl

# Test with BUFFER_SIZE=1 (edge case)
cc -Wall -Wextra -Werror -D BUFFER_SIZE=1 get_next_line.c get_next_line_utils.c main.c -o test_gnl
./test_gnl

# Test with large BUFFER_SIZE
cc -Wall -Wextra -Werror -D BUFFER_SIZE=1000000 get_next_line.c get_next_line_utils.c main.c -o test_gnl
./test_gnl

Memory Leak Check:

valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes ./test_gnl
