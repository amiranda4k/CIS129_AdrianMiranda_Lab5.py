# CIS129_AdrianMiranda_Lab5.py.
# Adrian Miranda
# Wed Mar 27
# Description: This program allows a grocery store to track the total number of bottles
# returned over seven days, calculates the total payout, and asks if there's more data.


# Step 1: Declare variables
total_bottles = 0 
counter = 1        
today_bottles = 0 
total_payout = 0.0 
keep_going = "y"  

# Step 2: Main loop to run the program again if the user has more data
while keep_going.lower() == "y":
    total_bottles = 0
    total_payout = 0.0
    
    # Step 3: Loop through each day of the week to collect bottle return data
    for counter in range(1, 8):  
        today_bottles = int(input(f"Enter number of bottles for day #{counter}: "))
        total_bottles += today_bottles
    
    
    total_payout = total_bottles * 0.10  
    
    print(f"The total number of bottles collected is {total_bottles}")
    print(f"The total paid out is ${total_payout:.2f}")

    keep_going = input("Do you want to enter another week’s worth of data? (Enter y or n): ")
