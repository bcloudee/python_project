import random

class Character:
    # __init__ is constructor that is automatically invoked when an object is created
    def __init__(self, name, health, attack): 
        self.name = name
        self.health = health
        self.attack = attack
        print("{0} began to explore the forest.".format(self.name))
        print("[Health {0}, Attack damage {1}]\n".format(self.health, self.attack))

    def attack_monster(self, monster):
        damage = random.randint(2, self.attack)
        print("{0} received {1} damage from {2}".format(monster.name, damage, self.name))
        return monster.take_damage(damage) #  
      # Retrun statement exit the function execution based on certain condition
   
    def take_damage(self, damage):
        self.health -= damage
        if self.health <= 0:
            print("\n{0} has 0 health left...\
                  \n{0}, you lost the battle...\
                  \n{0} couldn't escaped the forest...".format(self.name))
            return # 
        else:
            print("{0} : {1} health remaining".format(self.name, self.health))
            return # 

class Monster: 
    def __init__(self, name, health, damage): 
        self.name = name 
        self.health = health
        self.damage = damage
        print("Wild {0} appeared!".format(self.name))
        print("[Health {0}, Attack damage a {1}]\n".format(self.health, self.damage))

    def attack_character(self, character):
        damage = random.randint(2, self.damage)
        print('\n"{0}" received {1} damage from a {2}'.format(character.name, damage, self.name))
        return character.take_damage(damage)#
    
    def take_damage(self, damage):
        self.health -= damage  
        if self.health <= 0:
            print("\n{0} defeated the enemy!\
                  \n{0} escaped the forest safely!".format(Main_character.name))###
            return #
        else:
            print("{0} : {1} health remaining".format(self.name, self.health)) ##
            return  #

#Object (animal1, etc) created from class
    #animal1 is instance of Monster
Main_character = Character("Ash", 100, 15) 

animal1 = Monster("Tiger", 70, 14) 
animal2 = Monster("Lizard", 50, 12) 


#Event
while Main_character.health > 0 and (animal1.health > 0 or animal2.health > 0):
    if animal1.health > 0:
        Main_character.attack_monster(animal1)
        if animal1.health <= 0:
            break # Escape repeat statement 
        animal1.attack_character(Main_character)
        if Main_character.health <= 0:
            break
    if animal2.health > 0:
        Main_character.attack_monster(animal2)
        if animal2.health <= 0:
            break
        animal2.attack_character(Main_character)
        if Main_character.health <= 0:
            break
