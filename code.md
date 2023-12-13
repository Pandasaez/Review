```csharp
using System;
using System.Collections.Generic;
using System.Linq;

namespace FINAL_PROJECT_ITE1
{
    // Definition of the Student class with properties representing student information
    class Student
    {
        // Properties representing student details
        public string StudentNumber { get; set; }
        public string Surname { get; set; }
        public string FirstName { get; set; }
        public string Occupation { get; set; }
        public char Gender { get; set; }
        public int CountryCode { get; set; }
        public int AreaCode { get; set; }
        public string PhoneNumber { get; set; }

        // Overrides the ToString method to provide a custom string representation of the object
        public override string ToString()
        {
            return $"{Surname}, {FirstName}, with student number {StudentNumber}, is a {Occupation.ToLower()}. " +
                   $"The given phone number is {PhoneNumber}, area code is {AreaCode}, country code is {CountryCode}";
        }
    }

    // Definition of the ASEANPhonebook class
    class ASEANPhonebook
    {
        // List to store Student objects
        private List<Student> students;

        // Constructor to initialize the list
        public ASEANPhonebook()
        {
            students = new List<Student>();
        }

        // Adds a student to the phonebook
        public void AddStudent(Student student)
        {
            students.Add(student);
        }

        // Retrieves a student by their student number
        public Student GetStudentByNumber(string studentNumber)
        {
            return students.FirstOrDefault(s => s.StudentNumber == studentNumber);
        }

        // Retrieves a list of students based on specified country codes
        public List<Student> GetStudentsByCountry(params int[] countryCodes)
        {
            // Checks if the country code array contains 6 (ALL)
            if (countryCodes.Contains(6))
                return students.OrderBy(s => s.Surname).ToList();

            // Filters students by specified country codes, orders them by surname, and converts to a list
            return students.Where(s => countryCodes.Contains(s.CountryCode))
                           .OrderBy(s => s.Surname)
                           .ToList();
        }
    }

    // Main program
    class Program
    {
        // Entry point of the program
        static void Main()
        {
            // Creates an instance of ASEANPhonebook
            ASEANPhonebook phonebook = new ASEANPhonebook();

            // Main program loop
            while (true)
            {
                // Displays the main menu options
                Console.WriteLine("MAIN MENU");
                Console.WriteLine("[1] Store to ASEAN phonebook");
                Console.WriteLine("[2] Edit entry in ASEAN phonebook");
                Console.WriteLine("[3] Search ASEAN phonebook by country");
                Console.WriteLine("[4] Exit");

                // Prompts the user for input
                Console.Write("Input a valid number given above: ");
                string choice = Console.ReadLine();

                // Switch statement to handle user choices
                switch (choice)
                {
                    case "1":
                        // Calls the method to store a new entry in the phonebook
                        StoreToPhonebook(phonebook);
                        break;
                    case "2":
                        // Calls the method to edit an existing entry in the phonebook
                        EditEntry(phonebook);
                        break;
                    case "3":
                        // Calls the method to search the phonebook by country
                        SearchByCountry(phonebook);
                        break;
                    case "4":
                        // Exits the program
                        Environment.Exit(0);
                        break;
                    default:
                        // Handles invalid input
                        Console.WriteLine("Invalid number. Please try again.");
                        break;
                }
            }
        }

        // Method to store new entries in the phonebook
        static void StoreToPhonebook(ASEANPhonebook phonebook)
        {
            // Loop to allow multiple entries
            do
            {
                // Creates a new Student object
                Student student = new Student();

                // Prompts the user for student information
                Console.Write("Enter student number: ");
                student.StudentNumber = Console.ReadLine();

                // ... (similar prompts for other student information)

                // Adds the student to the phonebook
                phonebook.AddStudent(student);

                // Asks the user if they want to enter another entry
                Console.Write("Do you want to enter another entry [Y/N]? ");
            } while (Console.ReadLine().ToUpper() == "Y");
        }

        // Method to edit an existing entry in the phonebook
        static void EditEntry(ASEANPhonebook phonebook)
        {
            // Prompts the user for the student number to edit
            Console.Write("Enter student number: ");
            string studentNumber = Console.ReadLine();

            // Retrieves the student with the specified number
            Student student = phonebook.GetStudentByNumber(studentNumber);

            // Handles the case where the student is not found
            if (student == null)
            {
                Console.WriteLine("Student not found.");
                return;
            }

            // Displays the existing information about the student
            Console.WriteLine($"Here is the existing information about {studentNumber}: {student}");

            // Loop to allow multiple edits
            while (true)
            {
                // Displays the menu for information to edit
                Console.WriteLine("\nWhich of the following information you want to change?");
                Console.WriteLine("[1] Student number [2] Surname [3] Gender [4] Occupation");
                Console.WriteLine("[5] Country code [6] Area code [7] Phone number [8] Go Back To Main Menu");

                // Prompts the user for the choice of information to edit
                Console.Write("Enter choice: ");
                int choice = int.Parse(Console.ReadLine());

                // Exits the loop if the user chooses to go back to the main menu
                if (choice == 8)
                    break;

                // Calls the method to edit the chosen information
                EditInformation(student, choice);
            }
        }

        // Method to edit specific information of a student
        static void EditInformation(Student student, int choice)
        {
            // Switch statement to handle different information choices
            switch (choice)
            {
                case 1:
                    Console.Write("Enter new student number: ");
                    student.StudentNumber = Console.ReadLine();
                    break;
                case 2:
                    Console.Write("Enter new surname: ");
                    student.Surname = Console.ReadLine();
                    break;
                // ... (similar cases for other information)
                default:
                    // Handles invalid choices
                    Console.WriteLine("Invalid choice. Please try again.");
                    break;
            }

            // Displays the updated information
            Console.WriteLine($"New Information: {student}");
        }

        // Method to map menu choice to country code
        static int GetCountryCode(int choice)
        {
            switch (choice)
            {
                case 1: return 63; // Republic of the Philippines
                case 2: return 66; // Kingdom of Thailand
                case 3: return 65; // Republic of Singapore
                case 4: return 62; // Republic of Indonesia
                case 5: return 60; // Federation of Malaysia
                default: return 0;
            }
        }

        // Method to search the phonebook by country
        static void SearchByCountry(ASEANPhonebook phonebook)
        {
            // List to store selected country codes
            List<int> countryCodes = new List<int>();

            // Loop to allow multiple country selections
            while (true)
            {
                // Displays country options
                Console.WriteLine("From which country:");
                Console.WriteLine("[1] Philippines [2] Thailand [3] Singapore [4] Indonesia [5] Malaysia [6] ALL [0] No More");

                // Prompts the user for country choice
                int choice = int.Parse(Console.ReadLine());

                // Exits the loop if the user chooses not to select more countries
                if (choice == 0)
                    break;

                // Adds the corresponding country code to the list
                countryCodes.Add(GetCountryCode(choice));
            }

            // Displays the selected country codes
            Console.WriteLine($"Country Codes: {string.Join(", ", countryCodes)}");

            // Retrieves students based on selected country codes
            List<Student> result = phonebook.GetStudentsByCountry(countryCodes.ToArray());

            // Displays the result count and the list of students
            Console.WriteLine($"Result Count: {result.Count}");

            if (result.Count > 0)
            {
                Console.WriteLine("Here are the students:");

                foreach (var student in result)
                {
                    Console.WriteLine(student);
                }
            }
            else
            {
                Console.WriteLine("No students found for the selected countries.");
            }
        }
    }
}
```