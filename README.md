# get_next_line-_tester_berlin_2025
42 get_next_line_tester

#### Run your own tests!

How to use.

Complie & run:
# 1. Compile with different BUFFER_SIZES
cc -Wall -Wextra -Werror -D BUFFER_SIZE=42 -g3 get_next_line.c get_next_line_utils.c main.c -o test_gnl
./test_gnl

cc -Wall -Wextra -Werror -D BUFFER_SIZE=1 -g3 get_next_line.c get_next_line_utils.c main.c -o test_gnl
./test_gnl

cc -Wall -Wextra -Werror -D BUFFER_SIZE=10000 -g3 get_next_line.c get_next_line_utils.c main.c -o test_gnl
./test_gnl

# 2. CRITICAL: Run with valgrind to detect memory leaks
valgrind --leak-check=full --show-leak-kinds=all --track-origins=yes ./test_gnl

# 3. Stricter valgrind check
valgrind --leak-check=full --show-leak-kinds=all --errors-for-leak-kinds=definite,indirect --error-exitcode=1 ./test_gnl

