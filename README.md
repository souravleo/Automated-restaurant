print("SFC restaurant")
total=0
d={"Mutton":0,"Chicken":0,"Nuggets":0,"Mushroom":0}
m=150
chicken=120
o=130
p=60
while 1:
    print('''Press 1 for mutton biriyani-150rs per plate
           press 2 for chicken biriyani-120rs per plate
           press 3 for chicken nuggets-130rs per 8 pieces
           press 4 for mushroom biriyani-60rs per plate
           press 5 to show the cart
           press 6 to pay for the total''')
    n=int(input("Press here:"))
    if n==1:
        a=int(input("No.of Plates: "))
        add=int(input("Press1 to add to the cart\n Press 2 to remove from the cart:"))
        if add==1:
            d["Mutton"]= m*a
            total+=(m*a)
            continue
        elif add==2:
            if total==0:
                print("Nothing to remove")
            else:
                d["Mutton"]= m*a
                total-=(m*a)
                continue

    elif n==2:
        b=int(input("No.of Plates: "))
        add=int(input("Press1 to add to the cart\n Press 2 to remove from the cart:"))
        if add==1:
            d["Chicken"]=chicken*b
            total+=(chicken*b)
            continue
        elif add==2:
            if total==0:
                print("Nothing to remove")
            else:
                d["Chicken"]=chicken*b
                total-=(chicken*b)
                continue

            
    
    elif n==3:
        c=int(input("No.of Plates: "))
        add=int(input("Press1 to add to the cart\n Press 2 to remove from the cart:"))
        if add==1:
            d["Nuggets"]=o*c
            total+=(o*c)
            continue
        elif add==2:
            if total==0:
                print("Nothing to remove")
            else:
                d["Nuggets"]=o*c
                total-=(o*c)
                continue

        
    elif n==4:
        mush=int(input("No.of Plates:"))
        add=int(input("Press1 to add to the cart\n Press 2 to remove from the cart:"))
        if add==1:
            d["Mushroom"]= p*mush
            total+=(p*mush)
            continue
        elif add==2:
            if total==0:
                print("Nothing to remove")
            else:
                d["Mushroom"]= p*mush
                total-=(p*mush)
                continue
    elif n==5:
        for i in d:
            print(f"{i}={d[i]}")
        print(f"total={total}")
    elif n==6:
        if total==0:
            print("Grand total=0:")
            option=int(input("press 1 to continue\n press 2 to exit\npress here:"))
            if option==1:
                continue
            elif option==2:
                print("Thank you visit again!")
                break

        else:
            gst=12
            delivery_charge=30
            grand_total= total+(gst/100)*total+delivery_charge
            print(f"GST={gst}\nDelivery charge={delivery_charge}\ntotal={total}\nGrand total={grand_total}\n")
            option=int(input("press 1 to continue\n press 2 to pay and exit\npress here:"))
            if option==1:
                continue
            elif option==2:
                print("Paid sucessfully\nThank you visit again!")
                break
    else:
        print("Enter valid option")
        continue
