import random as rand

nivå = int(input("Vilken svårighetsgrad vill du ha? (1 eller 2)\n"))

if nivå == 1:
    i = 0
    a = 0
    tal1 = rand.sample(range(1, 7), 4)
    print(*tal1)
    
    while i != 13:
        svar = input("\nTalen?\n")
        gissning = [int(x) for x in svar.split()]
        
        for pos in range(4):
            if gissning[pos] == tal1[pos]:
                print("✔", end="")
            elif gissning[pos] in tal1:
                print("X", end="")
        
        i += 1
        a += 1
            
        
        if gissning == tal1:
            print("\nDu vann!")
            break
        if i == 12:
            print("\nDu förlorade, du har gissat 12 gånger.")
            break
            print(f"\nAntal gissningar: {i}")
            
        print(f"\nAntal gissningar: {a}")
        


elif nivå == 2:
    i = 1
    a = 0
    facit = [rand.randint(1, 8) for _ in range(4)]
    print(*facit)
    
    while i != 13:
        tal = input("\nTalen?\n")
        gissning = [int(x) for x in tal.split()]
        
        facit_kvar = facit.copy()
        gissning_kvar = gissning.copy()
        
        for pos in range(4):
            if gissning[pos] == facit[pos]:
                print("✔", end="")
                facit_kvar[pos] = None
                gissning_kvar[pos] = None
                
        for pos in range(4):
            if gissning_kvar[pos] is not None and gissning_kvar[pos] in facit_kvar:
                print("X", end="")
                facit_kvar.remove(gissning_kvar[pos])
        
        print(f"\nAntal gissningar: {a}")
        if gissning == facit:
            print("\nDu vann!")
            break
        if i == 12:
            print("\nDu förlorade, slut på gissningar.")
            break
        
        
        i += 1
        a += 1
        
