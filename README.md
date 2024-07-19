using System;

class MainClass
{
    public static int StockPicker(int[] arr)
    {
        int maxProfit = -1;

        for (int i = 0; i < arr.Length; i++)
        {
            for (int j = i + 1; j < arr.Length; j++)
            {
                int profit = arr[j] - arr[i];

                if (profit > maxProfit)
                {
                    maxProfit = profit;
                }
            }
        }

        return maxProfit;
    }

    static void Main()
    {
        Console.WriteLine(StockPicker(new int[] { 44, 30, 24, 32, 35, 30, 40, 38, 15 }));
        Console.WriteLine(StockPicker(new int[] { 10, 9, 8, 2 }));
        Console.WriteLine(StockPicker(new int[] { 10, 12, 4, 5, 9 }));
    }
}
