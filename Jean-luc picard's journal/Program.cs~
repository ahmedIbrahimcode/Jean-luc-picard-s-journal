using System;
using System.IO;

namespace Jean_Luc_Picard_s
{
    class Program
    {
        static void Main(string[] args)
        {

            //Getting the Date of Today
            DateTime currentDate = DateTime.Now;


            //Conversion into String
            string CurrentDate = currentDate.ToShortDateString();


            //Making the FileName
            string fileName = currentDate.ToShortDateString().Replace("/", "_") + ".txt";


            string fileinit = @"";

            //Making the File in the Current Directory
            string filePath = Path.Combine(fileinit, fileName);

            //Variable that will store the Whole Content
            string content = "";


            //Concatenating Captain's Log and Current Date on top of the File
            content += "Captain's log \n" + CurrentDate + "\n";

            Console.Write("Enter text in Jean-Luc Picard's Journal : ");


            //Getting String Input
            string input = Console.ReadLine();

            Console.WriteLine(input);

            //Bool variable to make sure the Content Should Store in File starting from 'Start'
            bool check = false;
            bool tempCheck = false;

            for (int i = 0; i < input.Length; i++)
            {
                if (input[i] == 's' || input[i] == 'S')
                {
                    if (input[i + 1] == 't' || input[i + 1] == 'T')
                    {
                        if (input[i + 2] == 'a' || input[i + 2] == 'A')
                        {
                            if (input[i + 3] == 'r' || input[i + 3] == 'R')
                            {
                                if (input[i + 4] == 't' || input[i + 4] == 'T')
                                {
                                    i = i + 5;  // Skipping the Index till  (star't') 
                                    check = true;
                                    tempCheck = true;
                                }
                            }

                        }
                    }
                }

                if (i == input.Length - 1)
                {
                    if (tempCheck == false)
                    {
                        Console.WriteLine("File Does not Contain Word 'Start'");
                        Console.WriteLine("Exitting the Program");
                        return;
                    }
                }


                if (check == true)
                {
                    while (true)
                    {

                        if (input[i] == 'E' || input[i] == 'e')
                        {
                            if (input[i + 1] == 'n' || input[i + 1] == 'N')
                            {
                                if (input[i + 2] == 'd' || input[i + 2] == 'D')
                                {
                                    check = false;
                                    break;
                                }
                            }

                        }

                        if (check)
                        {
                            content += input[i];
                        }

                        //Incrementing the index to read the whole content
                        i++;
                    }


                }
            }


            Console.WriteLine(content);


            //Writing the Whole Content to the File

            File.WriteAllText(filePath, content);

            Console.WriteLine("Content written to file successfully.");
        }
    }
}