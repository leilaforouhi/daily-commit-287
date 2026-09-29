def find_longest_sequence(numbers):
    if not numbers:
        return 0

    longest = 1
    current = 1

    for index in range(1, len(numbers)):
        if numbers[index] > numbers[index - 1]:
            current += 1
        else:
            current = 1

        longest = max(longest, current)

    return longest


if __name__ == "__main__":
    values = [1, 3, 5, 2, 4, 6, 8, 3, 7]

    print("Values:", values)
    print("Longest increasing sequence:", find_longest_sequence(values))
