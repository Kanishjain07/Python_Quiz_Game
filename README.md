# kanish
# code for quiz in python
questions = [
  ["What is the capital of France?","Madrid","Berlin","Rome","Paris",4],
  ["Which planet is known as the Red Planet?","Venus","Mars","Jupiter","Saturn",2],
  ["Who wrote the famous play 'Romeo and Juliet'?","William Shakespeare","Jane Austen","Charles Dickens","Mark Twain",1],
  ["What is the chemical symbol for water?","Wo","H2O","H2","O2",2],
  ["What is the tallest mammal in the world?","Elephant","Giraffe","Hippopotamus","Rhinoceros",2]
]
levels = [1000, 2000, 3000, 5000, 10000]
money = 0

for i in range(len(questions)):
    question = questions[i]
    print(f"\n\nQuestion for Rs. {levels[i]}")
    print(f"Q.question[0]""\n")
    print(f"a. {question[1]}          b. {question[2]} ")
    print(f"c. {question[3]}          d. {question[4]} ")
    reply = int(input("Enter your answer (1-4) or 0 to quit:\n" ))

    if reply == 0:
        break

    if reply == question[-1]:
        print(f"Correct answer, you have won Rs. {levels[i]}")
        money = levels[i]
        if i == 4:
            money = 10000
        elif i == 9:
            money = 320000
        elif i == 14:
            money = 10000000
    else:
        print("Wrong answer!")
        break

print(f"Your take home money is Rs. {money}")
