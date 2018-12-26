# Kings-Queens
Complex number guessing game.
import random

kings = 0

queens = 0

guess = 0

while True:
		
	number = int(random.randint(100, 1000))
	
	listnum = [int(x) for x in str(number)]
	
	if listnum[0] == listnum[1] or listnum[2] == listnum[1] or listnum[2] == listnum[0]:
			 
		pass
	
	else:
		
		try:
		
			guess = int(input("Guess the 3 digit number: "))
			
			listguess = [int(x) for x in str(guess)]	
			
			print(listguess)		
			
		except:
				
			print("Error 101: Invalid number")
				
			break

		if (listnum[0] == listguess[0]):
	
			kings =+ 1
    
			listnum[0] = 'a'
    
			listguess[0] = 'b'
    
		if (listnum[1] == listguess[1]):
	
			kings += 1
    
			listnum[1] = 'c'
    
			listguess[1] = 'd'
    
		if (listnum[2] == listguess[2]):
		
			kings += 1
    
			listnum[2] = 'e'
    
			listguess[2] = 'f'
    
		if (listnum[0] == listguess[1]) or (listnum[0] == listguess[2]):
	
 		   queens += 1
    
		if (listnum[1] == listguess[0]) or (listnum[1] == listguess[2]):
	
  	
  		   queens += 1
    
		if (listnum[2] == listguess[0]) or (listnum[2] == listguess[1]):
	
 	  	 queens += 1
 	  	 
		print("The number was: " + str(number))
		
		print("Your guess was: " + str(guess))

		if (kings == 1) and (kings == queens):
	
		    print("You have " + str(kings) + " king and " + str(queens) + " queen")
    
		elif kings == 1:
	
		    print("You have " + str(kings) + " king and " + str(queens) + " queens")
    
		elif queens == 1:
	
		    print("You have " + str(kings) + " kings and " + str(queens) + " queen")
    
		else:
	
		    print("You have " + str(kings) + " kings and " + str(queens) + " queens")
