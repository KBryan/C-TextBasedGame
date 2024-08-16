# C-TextBasedGame

# C# Tutorial: Building a Text-Based Game
* Welcome to this C# tutorial where we'll learn the essential concepts of C# by creating a simple text-based game. This hands-on approach will allow you to understand core programming principles while building a fun and interactive game. By the end of this tutorial, you'll have a solid grasp of C# fundamentals and a working game you can expand upon.

# Table of Contents:
* Introduction to C#
* Setting Up the Development Environment
* Creating the Game Structure
* Variables and Data Types
* User Input and Output
* Control Flow (If-Else Statements)
* Loops (For, While)
* Functions and Methods
* Arrays and Lists
* Classes and Objects
* Game Logic and State Management
* Enhancing the Game (Adding Features)
* Conclusion and Next Steps

# 1. Introduction to C#

* C# (pronounced "C-sharp") is a versatile programming language developed by Microsoft. It's widely used for building applications, games, and more. In this tutorial, we'll focus on using C# to create a text-based adventure game, which will help you learn the language's basics.

# 2. Setting Up the Development Environment
* To start coding in C#, you'll need an Integrated Development Environment (IDE). Visual Studio is a popular choice, but you can also use Visual Studio Code with the C# extension.

* Download and install Visual Studio or Visual Studio Code.
* Create a new Console Application project.
* This will set up a basic C# environment where we can start coding.

# 3. Creating the Game Structure
* Let's start by setting up the basic structure of our game. In this game, the player will explore a simple text-based world, make choices, and interact with the environment.

```csharp
using System;

namespace TextBasedGame
{
    class Program
    {
        static void Main(string[] args)
        {
            // Display the game title
            Console.WriteLine("Welcome to the Adventure Game!");
            Console.WriteLine("Your journey begins...");

            // Start the game loop
            StartGame();
        }

        static void StartGame()
        {
            // Game logic will go here
        }
    }
}
```

* This basic structure includes the Main method, which is the entry point of the game. We also have a placeholder StartGame method where we'll add our game logic.

# 4. Variables and Data Types
* In C#, variables store data that the game will use. We'll define variables to keep track of the player's name, health, and other attributes.

```csharp
static void StartGame()
{
    string playerName;
    int playerHealth = 100;

    Console.WriteLine("Enter your character's name:");
    playerName = Console.ReadLine();

    Console.WriteLine($"Welcome, {playerName}! Your health is {playerHealth}.");
}
```

* Here, we define a string to store the player's name and an int to represent their health.

# 5. User Input and Output
* Interacting with the player is essential in a text-based game. We'll use Console.ReadLine() to get input and Console.WriteLine() to display messages.

```csharp
Console.WriteLine("What would you like to do?");
Console.WriteLine("1. Explore the forest");
Console.WriteLine("2. Rest at the camp");

string choice = Console.ReadLine();

if (choice == "1")
{
    Console.WriteLine("You venture into the dark forest...");
}
else if (choice == "2")
{
    Console.WriteLine("You rest and regain some health.");
}
```

# 6. Control Flow (If-Else Statements)
* Control flow allows you to make decisions in your game. You can guide the player's path based on their choices using if-else statements.

```csharp
if (choice == "1")
{
    Console.WriteLine("You encounter a wild animal!");
}
else if (choice == "2")
{
    Console.WriteLine("You find a peaceful spot to rest.");
}
else
{
    Console.WriteLine("Invalid choice. Please try again.");
}
```

# 7. Loops (For, While)
* Loops allow you to repeat actions in your game, such as repeatedly asking the player for input or navigating through a series of challenges.

```csharp
bool gameRunning = true;

while (gameRunning)
{
    // Game loop logic
    Console.WriteLine("What would you like to do?");
    string action = Console.ReadLine();

    if (action == "exit")
    {
        gameRunning = false;
    }
    else
    {
        // Handle other actions
    }
}
```

# 8. Functions and Methods
* Functions help you organize your code and make it reusable. We'll create functions for common tasks like checking the player's health or handling battles.

```csharp
static void CheckPlayerHealth(int health)
{
    if (health <= 0)
    {
        Console.WriteLine("You have been defeated.");
    }
    else
    {
        Console.WriteLine($"Your health is {health}.");
    }
}
```

# 9. Arrays and Lists
* Arrays and lists allow you to store multiple items, such as a list of inventory items or enemies.

```csharp
string[] inventory = { "Sword", "Shield", "Potion" };

Console.WriteLine("Your inventory:");
foreach (string item in inventory)
{
    Console.WriteLine(item);
}
```

# 10. Classes and Objects
* Classes are blueprints for creating objects. We'll define a Player class to encapsulate the player's attributes and methods.

```csharp
class Player
{
    public string Name { get; set; }
    public int Health { get; set; }

    public Player(string name)
    {
        Name = name;
        Health = 100;
    }

    public void TakeDamage(int damage)
    {
        Health -= damage;
    }
}
```

# 11. Game Logic and State Management
* As you develop the game, you'll need to manage the game's state, such as the player's progress, location, and interactions with the world.

```csharp
enum GameState
{
    Exploring,
    Battling,
    Resting
}

GameState currentState = GameState.Exploring;

switch (currentState)
{
    case GameState.Exploring:
        Console.WriteLine("You are exploring the area.");
        break;
    case GameState.Battling:
        Console.WriteLine("You are in a battle!");
        break;
}
```

# 12. Enhancing the Game (Adding Features)
* Once the basics are in place, you can enhance the game by adding more features, such as:

* Combat System: Introduce battles with enemies.
* Inventory Management: Allow players to collect and use items.
* Multiple Locations: Expand the game world with different areas to explore.
* Quests and Objectives: Add goals for the player to achieve.
