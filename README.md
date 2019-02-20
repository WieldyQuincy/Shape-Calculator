# Shape-Calculator
Makes the most common calculations for the selected shape

using System;

namespace myapp
{
    class Program
    {
        static void Main(string[] args)
        {

            Console.WriteLine("Enter userID: ");
            string userIDasString = Console.ReadLine();

            double userID = Convert.ToDouble(userIDasString);

            Console.WriteLine("Welcome!");

            bool isInternalUser = isUserAnInternalUser(userID);

            if (isInternalUser)
            {
                Console.WriteLine("Enter (1) for square, (2) for circle, (3) for cube, (4) for cylinder, or (5) for sphere: ");
                string shapeAsString = Console.ReadLine();

                double shape = Convert.ToDouble(shapeAsString);

                double usershape = chosenShape(shape);

                if (usershape == 10)
                {
                    Console.WriteLine("Please enter the width of your square: ");
                    string squareWidthAsString = Console.ReadLine();

                    double squareWidth = Convert.ToDouble(squareWidthAsString);

                    Console.WriteLine("Please enter the length of your square: ");
                    string squareLengthAsString = Console.ReadLine();

                    double squareLength = Convert.ToDouble(squareLengthAsString);

                    double squareArea = squareWidth * squareLength;
                    double squarePerimeter = 2 * (squareWidth + squareLength);
                    double diagonal = Math.Sqrt((squareLength * squareLength) + (squareWidth * squareWidth));

                    Console.WriteLine($"The area of your square is {squareArea}");
                    Console.WriteLine($"The perimeter of your square is {squarePerimeter}");
                    Console.WriteLine($"The diagonal length of your square is {diagonal}");
                    Console.WriteLine("Thank you for using Joshua's shape calculator \nPress any key to end the program");
                    Console.ReadKey();
                    Console.WriteLine("Goodbye!");
                }
                else if (usershape == 20)
                {
                    Console.WriteLine("Please enter the radius of your circle: ");
                    string circleRadiusAsString = Console.ReadLine();

                    double circleRadius = Convert.ToDouble(circleRadiusAsString);

                    double circleArea = Math.PI * circleRadius * circleRadius;
                    double circleCircumference = 2 * Math.PI * circleRadius;

                    Console.WriteLine($"The area of your circle is {circleArea}");
                    Console.WriteLine($"The circumference of your circle is {circleCircumference}");
                    Console.WriteLine("Thank you for using Joshua's shape calculator \nPress any key to end the program");
                    Console.ReadKey();
                    Console.WriteLine("Goodbye!");    
                }
                else if (usershape == 30)
                {
                    Console.WriteLine("Please enter the width of your box: ");
                    string boxWidthAsString = Console.ReadLine();

                    double boxWidth = Convert.ToDouble(boxWidthAsString);

                    Console.WriteLine("Please enter the length of your box: ");
                    string boxLengthAsString = Console.ReadLine();

                    double boxLength = Convert.ToDouble(boxLengthAsString);
                    
                    Console.WriteLine("Please enter the height of your box: ");
                    string boxHeightAsString = Console.ReadLine();

                    double boxHeight = Convert.ToDouble(boxHeightAsString);

                    double boxArea = 2 * (boxHeight * boxWidth) + 2 * (boxHeight * boxLength) + 2 * (boxWidth * boxLength);
                    double boxVolume = boxHeight * boxWidth * boxLength;

                    Console.WriteLine($"The area of your box is {boxArea}");
                    Console.WriteLine($"The volume of your box is {boxVolume}");
                    Console.WriteLine("Thank you for using Joshua's shape calculator \nPress any key to end the program");
                    Console.ReadKey();
                    Console.WriteLine("Goodbye!");
                }
                else if (usershape == 40)
                {
                    Console.WriteLine("Please enter the height of your cylinder: ");
                    string cylHeightAsString = Console.ReadLine();

                    double cylHeight = Convert.ToDouble(cylHeightAsString);

                    Console.WriteLine("Please enter the radius of your cylinder: ");
                    string cylRadiusAsString = Console.ReadLine();

                    double cylRadius = Convert.ToDouble(cylRadiusAsString);

                    double cylArea = 2 * Math.PI * cylRadius * (cylRadius + cylHeight);
                    double cylVolume = Math.PI * cylRadius * cylRadius * cylHeight;

                    Console.WriteLine($"The area of your cylinder is {cylArea}");
                    Console.WriteLine($"The volume of your cylinder is {cylVolume}");
                    Console.WriteLine("Thank you for using Joshua's shape calculator \nPress any key to end the program");
                    Console.ReadKey();
                    Console.WriteLine("Goodbye!");
                }
                else if (usershape == 50)
                {
                    Console.WriteLine("Please enter the radius of your sphere: ");
                    string sphereRadiusAsString = Console.ReadLine();

                    int sphereRadius = Convert.ToInt32(sphereRadiusAsString);

                    double sphereArea = 4 * Math.PI * sphereRadius * sphereRadius;
                    double sphereVolume = 4 * Math.PI * Math.Pow(sphereRadius, 3)  / 3;

                    Console.WriteLine($"The area of your sphere is {sphereArea}");
                    Console.WriteLine($"The volume of your sphere is {sphereVolume}");
                    Console.WriteLine("Thank you for using Joshua's shape calculator \nPress any key to end the program");
                    Console.ReadKey();
                    Console.WriteLine("Goodbye!");
                }

            }
            else
            {
                Console.WriteLine("Go away!");
            }

        } 

        private static bool isUserAnInternalUser(double userID)
        {
            bool userIsInternal = false;

            if (userID == 5)
            {
                userIsInternal = true;
            }
            return userIsInternal;
        }
        private static double chosenShape(double shape)
        {
            double usershape = 0;

            if (shape == 1)
            {
                usershape = 10;
            }
            else if (shape == 2)
            {
                usershape = 20;
            }
            else if (shape == 3)
            {
                usershape = 30;
            }
            else if (shape == 4)
            {
                usershape = 40;
            }
            else if (shape == 5)
            {
                usershape = 50;
            }
            return usershape;
        } 
    }
}

