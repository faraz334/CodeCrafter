import random
import operator

# Define a dictionary with operators
operations = {
    "+": operator.add,
    "-": operator.sub,
    "*": operator.mul,
}

def generate_question():
    # Randomly choose two numbers and an operator
    num1 = random.randint(1, 10)
    num2 = random.randint(1, 10)
    operation = random.choice(list(operations.keys()))
    question = f"{num1} {operation} {num2}"
    answer = operations[operation](num1, num2)
    return question, answer

def math_quiz():
    print("Welcome to the Math Fun Quiz! Type 'exit' to quit.")
    score = 0
    attempts = 0
    
    while True:
        question, answer = generate_question()
        user_answer = input(f"What is {question}? ")
        
        if user_answer.lower() == 'exit':
            break
        
        # Check if the answer is correct
        try:
            if int(user_answer) == answer:
                print("Correct! 🎉")
                score += 1
            else:
                print(f"Oops! The correct answer was {answer}.")
            attempts += 1
        except ValueError:
            print("Please enter a valid number.")

    # Final score
    print(f"\nThanks for playing! Your score: {score}/{attempts}")
    if score == attempts:
        print("Perfect score! Well done! 🏆")
    elif score > attempts / 2:
        print("Good job! Keep practicing! 💪")
    else:
        print("Nice try! Practice makes perfect! 😊")

# Start the quiz
math_quiz()
