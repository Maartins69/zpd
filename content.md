### Izveidot number guessing spēli ar python programmēšanas valodu

### Saturs
### 1. Aprakstīt spēli 
### 2. Spēles loģika

Dators ģenerē vienu skaitli no 1 līdz 100
Spēle notiek pēc šī koda:
```py
import random

number = random.randint(1, 100)
guess = 0
tries = []

while guess != number:
    if guess < number:
        print("Pamēģini lielāku skaitli.")
    else:
        print("Pamēģini mazāku skaitli.")

    guess = int(input("Uzmini skaitli: "))
    tries.append(guess)
else:
    print(f"You win from {len(tries)} tries")
    print("Here is your guessing history:")
    print(tries)

    sum_of_difference = 0

    for t in tries:
        sum_of_difference += abs(t - number)
        
        print(f"Average difference was{sum_of_difference/len(tries)}")

```
### 3. un t.t.
