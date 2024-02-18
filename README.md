using System;

namespace PrimeNumberChecker
{
    class Program
    {
        static bool IsPrime(int number)
        {
            if (number <= 1)
                return false;

            for (int i = 2; i * i <= number; i++)
            {
                if (number % i == 0)
                    return false;
            }

            return true;
        }

        static void Main(string[] args)
        {
            Console.WriteLine("الأعداد الأولية من 1 إلى 100:");

            for (int num = 1; num <= 100; num++)
            {
                if (IsPrime(num))
                    Console.Write(num + " ");
            }

            Console.WriteLine("\nالأعداد الزوجية من 1 إلى 100:");

            for (int num = 1; num <= 100; num++)
            {
                if (num % 2 == 0)
                    Console.Write(num + " ");
            }

            Console.WriteLine("\nالأعداد الفردية من 1 إلى 100:");

            for (int num = 1; num <= 100; num++)
            {
                if (num % 2 != 0)
                    Console.Write(num + " ");
            }
        }
    }
}
