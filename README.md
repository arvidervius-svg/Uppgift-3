import random as rand

nivå = int(input("Vilken svårighetsgrad vill du ha? (1 eller 2)\n"))

if nivå == 1:
    i = 1
    a = 0
    tal1 = rand.sample(range(1, 7), 4)
    print(tal1)
    talen = (tal1[0], tal1[1], tal1[2], tal1[3])
    print(*talen)
    while i != 13:
        svar = input("\nTalen?\n")
        gissning = [int(x) for x in svar.split()]
        
        if gissning[0] == tal1[0]:  
            print("✔", end ="")
        if gissning[1] == tal1[1]:
            print("✔", end ="")
        if gissning[2] == tal1[2]:
            print("✔", end ="")
        if gissning[3] == tal1[3]:
            print("✔", end ="")
        
        if gissning == tal1:
            print("\n Du vann")
            break
        if i == 12:
            print("\n Du förlorade, slut på gissningar.")
            break
        i += 1  
    
if nivå == 2:
    i = 1
    a = 0
    tal1 = rand.randint(1, 8) # Ändrade till 1-8 så nivå 2 blir svårare!
    tal2 = rand.randint(1, 8)
    tal3 = rand.randint(1, 8)
    tal4 = rand.randint(1, 8)
    print(tal1, tal2, tal3, tal4)
    while i != 13:
        tal = input(" " "Talen?\n")
        gissning = tuple(int(tal) for tal in tal.split())
        
        if gissning[0] == tal1:
            print("✔", end ="")
        elif gissning[0] == tal2:
            print("X", end ="")
        elif gissning[0] == tal3:
            print("X", end ="")
        elif gissning[0] == tal4:
            print("X", end ="")
        if gissning[1] == tal2:
            print("✔", end ="")
        elif gissning[1] == tal1:
            print("X", end ="")
        elif gissning[1] == tal3:
            print("X", end ="")
        elif gissning[1] == tal4:
            print("X", end ="")
        if gissning[2] == tal3:
            print("✔", end ="")
        elif gissning[2] == tal1:
            print("X", end ="")
        elif gissning[2] == tal2:
            print("X", end ="")
        elif gissning[2] == tal4:
            print("X", end ="")
        if gissning[3] == tal4:
            print("✔", end ="")
        elif gissning[3] == tal1:
            print("X", end ="")
        elif gissning[3] == tal2:
            print("X", end ="")
        elif gissning[3] == tal3:
            print("X", end ="")
        
        if gissning == (tal1, tal2, tal3, tal4):
            print("\n Du vann")
            break
        if i == 12:
            print("\n Du förlorade, slut på gissningar.")
            break
        
        i += 1
        a += 1
        print(f"\n Antal gissningar: {a}")
