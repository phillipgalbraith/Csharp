# C# 
for .NET Tutorials  
## Introduction
https://docs.microsoft.com/en-us/dotnet/csharp/tour-of-csharp/tutorials/

## .NET and CLR (Common Language Runtime )
Virtual machine component
Manages execution of .NET programs
JIT converts compiled code intoo machine instructions
includes memoy and thread management
all .NET is executed by CLR

## IDE for C# 
(integrated Development Environment - 
Visual Studio COmmunity  Build and Compile code)
Text/Code Editor with 

## path
source\repo\NumberGuesser\NumberGuesser\program.cs

## How to view output

Tools > Command Line > Developer Command Prompt
In DCP:
  csc Program.cs
  Program
  OR 
  Crl F5

  EXampe:
string name = "Phillip";
int age = "35";
     Console.WriteLine("{0} is {1}",name,age);
Crl F5


## Example of a .cs file
using System;

//Namespace
namespace NumberGuesser
{
    // Main Class
    class Program
    {
        //Entry Point Method
        static void Main(string[] args)
        {
            // Set app vars
            string appName = "Number Guesser";
            string appVersion = "1.0.0";
            string appAuthor = "Phillip";


            // Change text color
            Console.ForegroundColor = ConsoleColor.Green;
            
            //Write out the app info
            Console.WriteLine("{0}; Version {1} by {2}", appName, appVersion, appAuthor);

            // Reset text color
            Console.ResetColor();

            //Ask users name
            Console.WriteLine("What is your Name");
            //
            string inputName = Console.ReadLine();

            Console.WriteLine("Hello {0}, let's play a game...", inputName);


            // Init correct number
            int correctNumber = 7;

            // Init guess var
            int guessInt = 0;

            //Ask user to guess a number
            Console.WriteLine("Guess a number between 1 and 10");

            string inputGuess = Console.ReadLine();

            //While guess is not correct
            while (guessInt != correctNumber)
            {
                Console.WriteLine("Guess again.");

                inputGuess = Console.ReadLine();

                guessInt = int.Parse(inputGuess);
            }

            Console.WriteLine("{0} is correct. Good game, {1}.",inputGuess,inputName);
            

        }
    }
}

