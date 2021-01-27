import random
from art import logo, vs
from game_data import data
from replit import clear

is_game_over = False
is_first_time = True

while not is_game_over:

  if is_first_time:
    user_score = 0
    print(logo)
    random_data_A = random.choice(data)
    follower_A_details =  ""
    for key in random_data_A:
      if key != "follower_count":
        follower_A_details += random_data_A[key] + ", "
  is_first_time = False
  
  random_data_B = random.choice(data)
  follower_B_details = ""
  for key in random_data_B:
    if key != "follower_count":
      follower_B_details+= random_data_B[key] + ", "
  
  if random_data_A == random_data_B:
    random_data_B = random.choice(data)

  follower_count_A = random_data_A['follower_count']
  follower_count_B = random_data_B['follower_count']
   
  print(f"Compare A: {follower_A_details}")
  print(vs)
  print(f"Against B: {follower_B_details}")

  guess = input("Who has more followers? Type 'A' or 'B': ").lower()
 
  if guess == 'A' and follower_count_A > follower_count_B:
    user_score += 1 
    follower_A_details = follower_B_details
    clear()
    print(logo)
    print(f"You are right. Current score: {user_score}")
  elif guess == 'B' and follower_count_A < follower_count_B:
    user_score += 1  
    follower_A_details = follower_B_details
    clear()
    print(logo)
    print(f"You are right. Current score: {user_score}")
  elif guess == 'A' and follower_count_A < follower_count_B:
    clear()
    print(logo)
    print(f"Sorry, that's wrong. Final score: {user_score}")
    is_game_over = True
  elif guess == 'B' and follower_count_A > follower_count_B:
    clear()
    print(logo)
    print(f"Sorry, that's wrong. Final score: {user_score}")
    is_game_over = True
