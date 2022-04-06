# Money Maker
 This program uses three coins to calculate the minimum coins to equal entered amount
using System;

namespace MoneyMaker
{
  class MainClass
  {
    public static void Main(string[] args)
    { /*This program uses three coins
      A bronze coin is worth 1 cent
      A silver coin is worth 5 cents
      A gold coin is worth 10 cents*/
      
      // Great the user and get input
      Console.WriteLine("Welcome to Money Maker!");
      Console.WriteLine("Enter an amount to convert to coins: ");
      string totalAsString = Console.ReadLine();
      Console.WriteLine(totalAsString);
      double total = Convert.ToDouble(totalAsString);
      Console.WriteLine($"{total} is equal to  ... ");
     
      // Define coin values
      int goldValue = 10;
      int silverValue = 5;

      // Calculate the change
      double goldCoins = Math.Floor(total / goldValue);
      double remainder = total % goldValue;

      double silverCoins = Math.Floor(remainder/silverValue);
      remainder = remainder % silverValue;

      //Print the results
      Console.WriteLine($"Gold coins: {goldCoins}");
      Console.WriteLine($"Silver coins: {silverCoins}");
      Console.WriteLine($"Bronze coins:  {remainder}");
      
    }
  }
}
