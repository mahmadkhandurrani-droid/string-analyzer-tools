# string-analyzer-tools
An automation beginner-friendly Python project that analyzes text by counting vowels, reversing sentences, and checking for palindromes. Built to practice string manipulation and functions.
# String Analyzer Project

def count_vowels(text):
    vowels = "aeiouAEIOU"
    count = 0
    for char in text:
        if char in vowels:
            count += 1
    return count


def reverse_sentence(text):
    return text[::-1]


def palindrome_check(text):
    # Remove spaces and convert to lowercase
    cleaned_text = text.replace(" ", "").lower()
    if cleaned_text == cleaned_text[::-1]:
        return True
    else:
        return False


def main():
    print("=== STRING ANALYZER ===")
    sentence = input("Enter a sentence: ")

    # Count vowels
    vowels = count_vowels(sentence)
    print("Number of vowels:", vowels)

    # Reverse sentence
    reversed_text = reverse_sentence(sentence)
    print("Reversed sentence:", reversed_text)

    # Palindrome check
    if palindrome_check(sentence):
        print("It is a Palindrome.")
    else:
        print("It is NOT a Palindrome.")


if __name__ == "__main__":
    main()
