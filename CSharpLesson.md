# <span>C#</span> Lesson

## Final Code
```cs
using System;
					
public class Program
{	
	public static int health = 3;
	
	public static void Main()
	{
		Console.WriteLine("You awake in a daze in the middle of the woods. A dilapidated shed stands to your right. What do you do?");
		Console.WriteLine();
		Console.WriteLine("A: Go into the shed");
		Console.WriteLine("B: Go into the woods");
		String answer = Console.ReadLine();
		
		if (answer == "A")
		{
			Console.WriteLine("There is a big monster in the shed and it kills you immediately.");
			GameOver();
		}
		else if (answer == "B")
		{
			Woods();
		}
	}
	
	public static void GameOver()
	{
		Console.WriteLine("GAME OVER");
	}
	
	public static void Woods()
	{
		Console.WriteLine("You venture out into the woods and find a tree with strange markings. What do you do?");
		Console.WriteLine();
		Console.WriteLine("A: Touch the tree");
		Console.WriteLine("B: Chop down the tree");
		String answer = Console.ReadLine();
		
		if (answer == "A")
		{
			Console.WriteLine("The markings begin to glow... you feel stronger.");
			health = health + 1;
		}
		else if (answer == "B")
		{
			Console.WriteLine("An angry tree spirit erupts from the stump and stuns you... you feel weaker.");
			health = health - 1;
		}
		
		Woods2();
	}
	
	public static void Woods2()
	{
		Console.WriteLine("You continue through the trees, and come upon a river. What do you do?");
		Console.WriteLine();
		Console.WriteLine("A: Try to cross it");
		Console.WriteLine("B: Walk along the shore");
		String answer = Console.ReadLine();
		
		if (answer == "A")
		{
			Console.WriteLine("While crossing the river, a large tree branch hits you in the face... you feel weaker.");
			health = health - 2;
			if (health < 1)
			{
				Console.WriteLine("You die.");
				GameOver();
			}
			else
			{
				Console.WriteLine("You successfully make it across the river!");
				Woods3();
			}
		}
		else if (answer == "B")
		{
			Console.WriteLine("While walking, you trip and fall to your death.");
			GameOver();
		}
			
	}
	
	public static void Woods3()
	{
		Console.WriteLine("You found the treasure!");	
	}
}
```