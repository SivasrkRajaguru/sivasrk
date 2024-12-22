# sivasrkhwuhiwe

import random

class QuizGame:
    def __init__(self, questions):
        self.questions = questions
        self.score =import random

class QuizGame:
    def __init__(self, questions):
        self.questions = questions
        self.score = 0

    def display_question(self, question):
        print(question['text'])
        for i, option in enumerate(question['options'], 1):
            print(f"{i}. {option}")

    def check_answer(self, question, answer):
        if answer == question['answer']:
            print("Correct!")
            self.score += 1
        else:
            print("Incorrect!")
        print()

    def play(self):
        random.shuffle(self.questions)
        for question in self.questions:
            self.display_question(question)
            user_input = input("Enter your answer (1, 2, 3, or 4): ")
            try:
                user_answer = int(user_input)
                if 1 <= user_answer <= 4:
                    self.check_answer(question, question['options'][user_answer - 1])
                else:
                    print("Invalid input! Please enter a number between 1 and 4.")
            except ValueError:
                print("Invalid input! Please enter a number.")
        print(f"Game Over! Your score is: {self.score}/{len(self.questions)}")

# Sample questions (replace with your own)
questions = [
    {
        'text': "What is the capital of France?",
        'options': ["Paris", "London", "Berlin", "Rome"],
        'answer': "Paris"
    },
    {
        'text': "Which planet is known as the Red Planet?",
        'options': ["Jupiter", "Mars", "Venus", "Mercury"],
        'answer': "Mars"
    },
    # Add more questions here...
]

# Start the game
quiz_game = QuizGame(questions)
quiz_game.play() 0

    def display_question(self, question):
        print(question['text'])
        for i, option in enumerate(question['options'], 1):
            print(f"{i}. {option}")

    def check_answer(self, question, answer):
        if answer == question['answer']:
            print("Correct!")
            self.score += 1
        else:
            print("Incorrect!")
        print()

    def play(self):
        random.shuffle(self.questions)
        for question in self.questions:
            self.display_question(question)
            user_input = input("Enter your answer (1, 2, 3, or 4): ")
            try:
                user_answer = int(user_input)
                if 1 <= user_answer <= 4:
                    self.check_answer(question, question['options'][user_answer - 1])
                else:
                    print("Invalid input! Please enter a number between 1 and 4.")
            except ValueError:
                print("Invalid input! Please enter a number.")
        print(f"Game Over! Your score is: {self.score}/{len(self.questions)}")

# Sample questions (replace with your own)
questions = [
    {
        'text': "What is the capital of France?",
        'options': ["Paris", "London", "Berlin", "Rome"],
        'answer': "Paris"
    },
    {
        'text': "Which planet is known as the Red Planet?",
        'options': ["Jupiter", "Mars", "Venus", "Mercury"],
        'answer': "Mars"
    },
    # Add more questions here...
]

# Start the game
quiz_game = QuizGame(questions)
quiz_game.play()
