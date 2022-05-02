# Calculator-by-class-
You can choose what you want from calculator .
Main class
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace calculator
{
    internal class Program
    {
        static void Main(string[] args)
        {
            calculator sq = new calculator();
            Console.WriteLine("***** What you want from Calculator *****" +
                "\n1.Addition" +
                "\n2.Multiplication" +
                "\n3.Division" +
                "\n4.Substraction" +
                "\n*************************************");
            int enter = int.Parse(Console.ReadLine());
            switch(enter)
            {
                case 1:
                    Console.WriteLine("Enter two numbers");
                    Console.WriteLine("------------------------------------------");
                    int num1 = Convert.ToInt32(Console.ReadLine());
                    Console.WriteLine("First Number is:" + num1);
                    int num2 = Convert.ToInt32(Console.ReadLine());
                    Console.WriteLine("********************************************");
                    Console.WriteLine("Second Number is:" + num2);
                    Console.WriteLine("********************************************");
                    Console.WriteLine("Sum of two number is:" + sq.sum(num1, num2));
                    break;
                
                case 2:
                    Console.WriteLine("Enter two numbers");
                    Console.WriteLine("------------------------------------------");
                    int mul1 = Convert.ToInt32(Console.ReadLine());
                    Console.WriteLine("First Number is:" + mul1);
                    int mul2 = Convert.ToInt32(Console.ReadLine());
                    Console.WriteLine("********************************************");
                    Console.WriteLine("Second Number is:" + mul2);
                    Console.WriteLine("********************************************");
                    Console.WriteLine("Multiplication of two number is:" + sq.mul(mul1, mul2));
                    break;
                case 3:
                    Console.WriteLine("Enter two numbers");
                    Console.WriteLine("------------------------------------------");
                    int div1 = Convert.ToInt32(Console.ReadLine());
                    Console.WriteLine("First Number is:" + div1);
                    int div2 = Convert.ToInt32(Console.ReadLine());
                    Console.WriteLine("********************************************");
                    Console.WriteLine("Second Number is:" + div2);
                    Console.WriteLine("********************************************");
                    Console.WriteLine("Division of two number is:" + sq.div(div1, div2));
                    break;
                case 4:
                    Console.WriteLine("Enter two numbers");
                    Console.WriteLine("------------------------------------------");
                    int sub1 = Convert.ToInt32(Console.ReadLine());
                    Console.WriteLine("First Number is:" + sub1);
                    int sub2 = Convert.ToInt32(Console.ReadLine());
                    Console.WriteLine("********************************************");
                    Console.WriteLine("Second Number is:" + sub2);
                    Console.WriteLine("********************************************");
                    Console.WriteLine("Substraction of two number is:" + sq.sub(sub1, sub2));
                    break;
              default: 
                    Console.WriteLine("Invalid Number");
                    break;

            }
        }
    }
}
#Calculator Method
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

namespace calculator
{
    public class calculator
    {
     public int sum(int n1,int n2)
        {
            return n1+ n2;
        }
     public int mul(int n1,int n2)
        {
            return n1 * n2;
        }
        public float div(float n1f,float n2f)
        {  if (n1f > n2f)
            {
                
                return n1f / n2f;
            }
        else
                Console.WriteLine("For division first number should be greator then second");
            return 0;
        }
        public int sub(int num1, int num2)
        {
            if (num1 > num2)
            {
                return num1 - num2;
            }
            return num2 - num1;
        }
    }
}
