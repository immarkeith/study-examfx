class Flashcard:
    def __init__(self, word, meaning):
        self.word = word
        self.meaning = meaning

    def __str__(self):
        return self.word + " (" + self.meaning + ")"

flash = []
print("Welcome to the flashcard application!")

while True:
    word = input("Enter the word or question: ")
    meaning = input("Enter the meaning or answer: ")
    flash.append(Flashcard(word, meaning))
    
    option = int(input("Enter 0 to add another card, or 1 to stop: "))
    if option:
        break

print("\nYour Flashcards:")
for card in flash:
    print(">", card)
