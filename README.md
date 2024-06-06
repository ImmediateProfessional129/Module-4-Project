# Module-4-Project
This is a GitHub repository link for COP2360-1 Module 4 Project Assignment
using System;

//namespace CSharpArithmeticsDivision
//{
  class Program
  {
  static void Main()
  {
    Console.WriteLine ("Enter products of two numbers");
    int m = Convert.ToInt32(Console.ReadLine());
    int n = Convert.ToInt32(Console.ReadLine());
    int p = m * n;
    Console.WriteLine ("Product of two numbers is " + p);
    //string input1 = Console.ReadLine();

    Console.WriteLine ("Enter the first number");
    string input1 = Console.ReadLine();

    Console.WriteLine ("Enter the second number");
    string input2 = Console.ReadLine();

    try
    {
      int num1 = Convert.ToInt32(input1);
      int num2 = Convert.ToInt32(input2);

      int result = num1 / num2;
      Console.WriteLine($"The result for this division is: {result}");
       Console.WriteLine($"The result for other exception is: {result / 2.5}");
    }
    catch (FormatException ex)
    {
        Console.WriteLine("One or both of the inputs are not invalid integers.");
        Console.WriteLine($"Detailed error message: {ex.Message}");
    }
    catch (DivideByZeroException ex)
    {
      Console.WriteLine("Error! Division by zero is not allowed.");
      Console.WriteLine($"Detailed error message: {ex.Message}" );
    }
    try
    {
      int num1 = Convert.ToInt32(input1);
      int num2 = Convert.ToInt32(input2);

      int result = num1 / num2;
      Console.WriteLine($"The result for this division is: {result}");
       Console.WriteLine($"The result for other exception is: {result / 2.5}");
    }
    catch (Exception ex)
    {
      Console.WriteLine("An unexpected error occcured.)");
      Console.WriteLine($"Detailed error message: {ex.Message}");
    }

    Console.WriteLine("Press any key to exit");
    Console.ReadKey();
    }

    static int DivideStrings(string number1, string number2)
    {
      int input1 = int.Parse(number1);
      int input2 = int.Parse(number2);

      if (input2 == 0)
      {
        throw new DivideByZeroException("Division by zero cannot be used.");
        }

        return input1 / input2;
      }
    }
  //}
