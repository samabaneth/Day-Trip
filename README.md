# Day-Trip
import random
locations = ["Seattle", "San Francisco", "Los Angeles", "Salt Lake City"]
print(locations)

restaurants = ["The Pink Door", "Sotto Mare", "Musso and Frank Grill", "Veneto"]
print (restaurants)

transit = ["Train", "Lyft", "Bus", "Bike"]
print(transit)

activities = ["Shopping", "Go to a museum ", "Go to the beach", "Hiking"]
print(activities)


list = (locations[0] + ", " + restaurants[0] + ", " + transit[0] + ", " + activities[0])

list_1 = (locations[1] + ", " + restaurants[1] + ", " + transit [1] + ", " + activities[1])

list_2 = (locations[2] + ", " + restaurants[2] + ", " + transit [2] + ", " + activities[2])

list_3 = (locations[3] + ", " + restaurants[3] + ", " + transit [3] + ", " + activities[3])

grand_list = [list, list_1, list_2, list_3]
print(grand_list)


def day_trip():
    confirm_bool = True
    while confirm_bool:
        day_trip = random.choice(grand_list)
        user_input = input (f"{day_trip} was selected, would you like to proceed? ")
        if user_input == "no":
            day_trip = random.choice(grand_list)
        else:
            print(f"{day_trip} has been selected!")
            confirm_bool = False
day_trip()

