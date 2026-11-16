nivå = int(input("Vilken svårighetsgrad vill du ha?"))
if nivå == 1:
    
elif nivå == 2:
    import random as rand
    i = 1
    a = 0
    tal1 = rand.randint(1, 6)
    tal2 = rand.randint(1, 6)
    tal3 = rand.randint(1, 6)
    tal4 = rand.randint(1, 6)
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
            print("✔", end ="")
    
        if i == 12:
            print("\n Du förlorade, slut på gissningar.")
            break
        if gissning == (tal1, tal2, tal3, tal4):
            print("\n Du vann")
            break
    
        i += 1
        a += 1
        print(f"\n Antal gissningar: {a}")
    


