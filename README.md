# -from functools import reduce


def square_numbers(numbers: list) -> list:
    return list(map(lambda x: x ** 2, numbers))


def filter_even_numbers(numbers: list) -> list:
    return filter(lambda x: x % 2 == 0, numbers)


def multiply_numbers(numbers: list) -> int:
    return reduce(lambda x, y: x * y, numbers)


def sum_of_squares_of_even_numbers(numbers: list) -> int:
    numbers = filter(lambda x: x % 2 == 0, numbers)
    numbers = list(map(lambda x: x ** 2, numbers))
    return reduce(lambda x, y: x + y, numbers)


def word_length_map(input_string):
    dictionary = dict()
    a = any(map(lambda s: dictionary.update({s: len(s)}), input_string.split()))
    return dictionary
