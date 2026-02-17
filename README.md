PPt workshop is the pre-placement training offering by our college Seshadri Rao Gudlavalleru Engineering College.
Our college is mainly focusing on python coding.
Upto week-8 basic theory is coverted in 3rd semister.


link batch-3 : https://shorturl.at/IzFWI



class is a blueprint of objects
object is instance of a class

MAX_SPEED = 120
MIN_SPEED = 0

class Traffic:
    def __init__(self, speed, direction):
        self.speed = speed
        self.direction = direction

    def go(self):
        self.speed = self.speed + 10
        if self.speed > MAX_SPEED:
            self.speed = MAX_SPEED
        print(self.speed, self.direction)

    def pause(self):
        self.speed = self.speed // 2
        print(self.speed, self.direction)

    def stop(self):
        self.speed = MIN_SPEED
        print(self.speed, self.direction)

car = Traffic(40, "North")
bike = Traffic(20, "East")

car.go()
car.pause()
car.stop()


bike.go()
bike.pause()
bike.stop()

50 North
25 North
0 North
30 East
15 East
0 East


#single inheritance
class shape:
    def area(self):
        print("Area of shape is unknown")
    def sides(self):
        name="unknown"
        print("Shape is:",name)
        print("Number of sides is:0")
class Triangle(shape):
    def sides(self):
        name="triangle"
        print("Shape is:",name)
        print("Number of sides is: 3")
T=Triangle()
T.area()
T.sides()

Area of shape is unknown
Shape is: triangle
Number of sides is: 3

class Egg:
    def __init__(self, name="Egg", color="White", weight=0.5):
        self.name = name
        self.color = color
        self.weight = weight
        print(f"[{self.__class__.__name__}] Stage: {self.name}, Color: {self.color}, Weight: {self.weight}")

    def move(self):
        print(f"{self.name} does not move.")

    def feedOn(self):
        print(f"{self.name} feeds on yolk.")


class Larva(Egg):
    def __init__(self, name="Larva", color="Green", weight=2.0):
        super().__init__("Egg", "White", 0.5)   # Call Egg details
        self.name = name
        self.color = color
        self.weight = weight
        print(f"[{self.__class__.__name__}] Stage: {self.name}, Color: {self.color}, Weight: {self.weight} (inherits from Egg)")

    def move(self):
        print(f"{self.name} crawls.")

    def feedOn(self):
        print(f"{self.name} feeds on leaves.")


class Pupa(Larva):
    def __init__(self, name="Pupa", color="Brown", weight=1.5):
        super().__init__("Larva", "Green", 2.0)  # Call Larva (which calls Egg)
        self.name = name
        self.color = color
        self.weight = weight
        print(f"[{self.__class__.__name__}] Stage: {self.name}, Color: {self.color}, Weight: {self.weight} (inherits from Larva → Egg)")

    def move(self):
        print(f"{self.name} remains still.")

    def feedOn(self):
        print(f"{self.name} does not feed.")


class Insect(Pupa):
    def __init__(self, name="Butterfly", color="Colorful", weight=1.0):
        super().__init__("Pupa", "Brown", 1.5)   # Call Pupa (which calls Larva → Egg)
        self.name = name
        self.color = color
        self.weight = weight
        print(f"[{self.__class__.__name__}] Stage: {self.name}, Color: {self.color}, Weight: {self.weight} (inherits from Pupa → Larva → Egg)")

    def move(self):
        print(f"{self.name} flutters gracefully.")

    def feedOn(self):
        print(f"{self.name} feeds on nectar.")


# 🌱 Test lifecycle
print("\n--- Egg Stage ---")
egg = Egg()
egg.move()
egg.feedOn()

print("\n--- Larva Stage ---")
larva = Larva()
larva.move()
larva.feedOn()

print("\n--- Pupa Stage ---")
pupa = Pupa()
pupa.move()
pupa.feedOn()

print("\n--- Insect Stage ---")
insect = Insect()
insect.move()
insect.feedOn()









doc-link:













api-for every page to access a link is provided
api will be mediater between server and frontend and server and database
key terminolgies:
URL - endpoint- the destination address
