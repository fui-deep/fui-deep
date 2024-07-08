- 👋 Hi, I’m @fui-deep
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
fui-deep/fui-deep is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->import random

import random

def hangman():
    words = ['python', 'hangman', 'programming', 'code']
    word = random.choice(words)
    guesses = ''
    attempts = 6

    while attempts > 0:
        for char in word:
            if char in guesses:
                print(char, end=' ')
            else:
                print('_', end=' ')
        print()

        guess = input("Guess a letter: ")
        guesses += guess

        if guess not in word:
            attempts -= 1

        if set(word) <= set(guesses):
            print("Congratulations! You guessed the word.")
            break
        elif attempts == 0:
            print("Sorry, you ran out of attempts. The word was", word)

hangman()
    
