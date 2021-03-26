# Main

using System;
using System.IO;

namespace Registro_v1
{
    class program
    {
        static void Main(string[] args)
        {
            #region ExternCode

            /*Stream fs = new FileStream("C:/Users/KingTarot/Desktop/1/All3/Programación/Codes/Registros/Datos.csv",FileMode.Create,FileAccess.Write);
            StreamWriter writer = new StreamWriter(fs);
            writer.WriteLine("ID, Name, LastName, age");
            writer.Close();
            fs.Close();*/

            #endregion

            #region vars

            //VARIABLES
            Console.Clear();
            string Id, Name, LaName, choice;
            byte age, X;
            #endregion

            #region Main
            
            System.Console.WriteLine("What do you want to do?");
            System.Console.WriteLine("1) Add");
            System.Console.WriteLine("2) List");
            System.Console.WriteLine("3) Search");

            X = Convert.ToByte(Console.ReadLine());
            string filePath = args[0];
            switch (X)
            {
                case 1:
                Console.Clear();
                System.Console.WriteLine("Write your ID: ");
                Id = Console.ReadLine();
                System.Console.WriteLine("Write your Name: ");
                Name = Console.ReadLine();
                System.Console.WriteLine("Write your LastName: ");
                LaName = Console.ReadLine();
                System.Console.WriteLine("How old are you? ");
                age = Convert.ToByte(Console.ReadLine());

            
                Console.Clear();
                System.Console.WriteLine("Do you want to save this info? Y/N");
                choice = Console.ReadLine().ToUpper();

                if(choice == "Y")
                {
                    Persona Anonimo = new Persona (Id,Name,LaName,age);
                    Console.Clear();
                    Anonimo.show();
                    System.Console.WriteLine("Is this the information that you want to save? Y/N");
                    choice = Console.ReadLine().ToUpper();

                    if(choice == "Y")
                    {
                        Anonimo.save(filePath);
                    }
                    else if(choice == "N")
                    {
                    
                    }
                    else 
                    {
                        System.Console.WriteLine("The answer is invalid");
                        Console.ReadKey();
                    
                    }
                }
                else if(choice == "N")
                {
                
                }
                else
                {
                    System.Console.WriteLine("This answer is invalid");
                    Console.ReadKey();
                
                }
                break;

                case 2:
                Console.Clear();
                System.Console.WriteLine("LIST");
                Stream fs = new FileStream(filePath, FileMode.Open, FileAccess.Read);
                StreamReader sr = new StreamReader(fs);
                System.Console.WriteLine(sr.ReadToEnd());
                break;

                case 3:
                Console.Clear();
                System.Console.WriteLine("What is the ID?");
                Id = Console.ReadLine();
                Perss pers = new Perss(Id, filePath);
                pers.Search();
                break;
            }
            #endregion
        }
    }
}

# Class1

using System;
using System.IO;

namespace Registro_v1
{
    class Persona
    {
        public string ID {get; set;}
        public string NAME{get;set;}
        public string LANAME{get;set;}
        public int AGE{get;set;}
        public string file{get;set;}

        public Persona(string id, string name, string Aname, int age)
        {
            ID = id;
            NAME = name;
            LANAME = Aname;
            AGE = age;
        }


        public void show()
        {
            Persona Anonis = new Persona(ID, NAME, LANAME, AGE);
            Console.Clear();
            System.Console.WriteLine(Anonis.ID);
            System.Console.WriteLine(Anonis.NAME);
            System.Console.WriteLine(Anonis.LANAME);
            System.Console.WriteLine(Anonis.AGE);
            System.Console.WriteLine("");
        }

        public void save(string file)
        {
            Stream fs = new FileStream(file,FileMode.Append,FileAccess.Write);
            StreamWriter writer = new StreamWriter(fs);
            writer.WriteLine(ID + ", " + NAME + ", " + LANAME + ", " + AGE);
            writer.Close();
            fs.Close();
            System.Console.WriteLine("Your information has been saved");
        }
    }
}

# Class2

using System;
using System.IO;

namespace Registro_v1
{
    class Perss
    {
        public string ID{get;set;}
        public string file{get;set;}

        public Perss(string ced, string fs)
        {
            ID = ced;
            file = fs;
        }

        public void Search()
        {
            

            string chain;
            string[] camps = new string[4];


            Stream fs = new FileStream(file,FileMode.Open,FileAccess.Read);
            StreamReader sr = new StreamReader(fs);

            chain = sr.ReadLine();
            while(chain != null)
            {
                Console.Clear();
                camps = chain.Split(',');
                if(camps[0].Trim().Equals(ID))
                {
                    
                    System.Console.WriteLine(camps[0]);
                    System.Console.WriteLine(camps[1]);
                    System.Console.WriteLine(camps[2]);
                    System.Console.WriteLine(camps[3]);
                    fs.Close();
                    sr.Close();
                    break;
                }
            }
        }
    }
}
