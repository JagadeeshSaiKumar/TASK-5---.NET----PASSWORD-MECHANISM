using System.ComponentModel.DataAnnotations;
using System.Threading;
class task5
{
    public static void Main(string[] args)
    {
        int b = 30;
        string e, d;
        Console.ForegroundColor = ConsoleColor.Magenta;
        Console.WriteLine("                                                     Welcome To DEVCARE            ");
        Console.WriteLine("────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────");
        Console.WriteLine();
        Console.WriteLine("Choose your device :");
        Console.WriteLine("1─>Mobile");
        Console.WriteLine("2─>Desktop");
        int c=Convert.ToInt32(Console.ReadLine());
        int at = 4;
        if (c == 1)
        {
            Console.ForegroundColor = ConsoleColor.Cyan;
            Console.Write("create a Pin with numbers of length 4 - 6 : ");
            int a = Convert.ToInt16(Console.ReadLine());
            Console.WriteLine();
            int f = a;
            int rev = 0;
            while (f > 0)
            {
                f /= 10;
                rev++;

            }
            while(rev<4)
            {

                rev = 0;
                Console.Clear();
                Console.Write("create a Pin with numbers of length 4 - 6 : ");
                a = Convert.ToInt16(Console.ReadLine());
                f = a;
                while(f > 0)
                {
                    f /= 10;rev++;
                }
            }
            Console.Write("Enter Pin to login : ");
            int p = Convert.ToInt16(Console.ReadLine());
            int i = 1;
            while (p != a)
            {
                Console.Clear();
                Console.WriteLine("Incorrect Pin !");
                Console.WriteLine("You have "+at+" attempts");
                at--;
                Console.Write("Again Enter Password to login : ");
                p = Convert.ToInt16(Console.ReadLine());
                i++;
                while (i > 4 && b >= 0)
                {
                    Console.Clear();
                    Console.WriteLine("Try again after " + b + " seconds");
                    b--;
                    Thread.Sleep(1000);
                    if (b == 0)
                    {
                        i = 0;
                        at = 5;
                    }

                }

                b = 30;

            }
            Console.ForegroundColor = ConsoleColor.Red;
            Console.WriteLine("                                     Welcome to mobile Login");

        }
        else
        {
            Console.ForegroundColor = ConsoleColor.Blue;
            Console.Write("create a Password : ");
            e = Console.ReadLine();
            Console.WriteLine();
            Console.Write("Enter Password to login : ");
            d = Console.ReadLine();
            int i = 1;
            while (d != e)
            {
                Console.Clear();
                Console.WriteLine("Incorrect Pin !");
                Console.WriteLine("You have " + at + " attempts");
                at--;
                Console.Write("Again Enter Password to login : ");
                d = Console.ReadLine();
                i++;
                while (i > 4 && b >= 0)
                {
                    Console.Clear();
                    Console.WriteLine("Try again after " + b + " seconds");
                    b--;
                    Thread.Sleep(1000);
                    if (b == 0)
                    {
                        i = 0;
                        at = 5;
                    }

                }

                b = 30;

            }
            Console.WriteLine();
            Console.WriteLine();
            Console.ForegroundColor = ConsoleColor.Red;
            Console.WriteLine("                                     Welcome to Desktop Login");
        }

    }
}
