using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Exam3
{
    class Exam3
    {
        static void Main(string[] args)
        {
            string season = Console.ReadLine().ToLower();
            double km = double.Parse(Console.ReadLine());
            double sum = 0;
            double percentige = 0;

            if (season == "summer")
            {
                if (km <= 5000)
                {
                    sum = (km * 0.90) * 4;
                    percentige = (sum * 10) / 100;
                    sum -= percentige; 
                }
                else if (km > 5000 && km <= 10000)
                {
                    sum = (km * 1.10) * 4;
                    percentige = (sum * 10) / 100;
                    sum -= percentige;
                }
                else 
                {
                    sum = (km * 1.45) * 4;
                    percentige = (sum * 10) / 100;
                    sum -= percentige;
                }
            }
            else if (season == "winter")
            {
                if (km <= 5000)
                {
                    sum = (km * 1.05) * 4;
                    percentige = (sum * 10) / 100;
                    sum -= percentige;
                }
                else if (km > 5000 && km <= 10000)
                {
                    sum = (km * 1.25) * 4;
                    percentige = (sum * 10) / 100;
                    sum -= percentige;
                }
                else
                {
                    sum = (km * 1.45) * 4;
                    percentige = (sum * 10) / 100;
                    sum -= percentige;
                }
            }
            else if (season == "spring" || season == "autumn")
            {
                if (km <= 5000)
                {
                    sum = (km * 0.75) * 4;
                    percentige = (sum * 10) / 100;
                    sum -= percentige;
                }
                else if (km > 5000 && km <= 10000)
                {
                    sum = (km * 0.95) * 4;
                    percentige = (sum * 10) / 100;
                    sum -= percentige;
                }
                else
                {
                    sum = (km * 1.45) * 4;
                    percentige = (sum * 10) / 100;
                    sum -= percentige;
                }
            }

            Console.WriteLine("{0:f2}", sum);
        }
    }
}
