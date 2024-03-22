using System;

class Program
{
    static void Main(string[] args)
    {
        Console.WriteLine("Enter the height of the triangle:");
        int height;
        if (int.TryParse(Console.ReadLine(), out height))
        {
            PrintTriangle(height);
        }
        else
        {
            Console.WriteLine("Invalid input. Please enter a valid integer.");
        }
    }

    static void PrintTriangle(int height)
    {
        for (int i = 1; i <= height; i++)
        {
            for (int j = 1; j <= height - i; j++)
            {
                Console.Write(" ");
            }

            for (int k = 1; k <= 2 * i - 1; k++)
            {
                Console.Write("*");
            }

            Console.WriteLine();
        }
    }
}