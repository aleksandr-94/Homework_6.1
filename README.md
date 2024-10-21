# Homework_6.1


import string


def letter_range(range_str):
    start, end = range_str.split('-')

    start_index = string.ascii_letters.index(start)
    end_index = string.ascii_letters.index(end)

    if start_index <= end_index:
        return string.ascii_letters[start_index:end_index + 1]
    else:
        return string.ascii_letters[start_index:] + string.ascii_letters[:end_index + 1]


print(letter_range("a-c"))  # abc
print(letter_range("a-a"))  # a
print(letter_range("s-H"))  # stuvwxyzABCDEFGH
print(letter_range("a-A"))  # abcdefghijklmnopqrstuvwxyzA
