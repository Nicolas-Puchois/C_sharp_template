# Menu Template

<details style="border: 1px solid #aaa; border-radius: 4px; padding: .5em .5em 0;">
  <summary style="font-weight: bold; margin: -.5em -.5em 0; padding: .5em; cursor: pointer;">Programe.cs</summary>

```C#
bool appWorking = true;
while (appWorking)
{
    Menu.MenuSelect("main");
    switch (Console.ReadLine())
    {
        case "1":
            break;
        case "2":
            break;
        case "3":
            break;
        case "4":
            break;
        case "exit":
            Environment.Exit(0);
            break;
        default:
            Console.WriteLine("Error:Command not supported or incorect");
            break;
    }
}
```
</details>
<details style="border: 1px solid #aaa; border-radius: 4px; padding: .5em .5em 0;">
  <summary style="font-weight: bold; margin: -.5em -.5em 0; padding: .5em; cursor: pointer;">Menu Class</summary>

### Menu Classes
```C#
internal class Menu
{
    public static void MenuSelect(string choixDeMenu)
    {
        switch (choixDeMenu)
        {
            #region Principale
            case "main":
                Console.Clear();
                Console.Write("====|Section|====\n\n" +
                    "[1] \n" +
                    "[2] \n" +
                    "[3] \n" +
                    "[4] \n" +
                    "[5] \n" +
                    "[6] \n" +
                    "-------------------------\nEntry:");
                break;
            #endregion
        }
    }
}
```
</details>

### entry verification
<details style="border: 1px solid #aaa; border-radius: 4px; padding: .5em .5em 0;">
  <summary style="font-weight: bold; margin: -.5em -.5em 0; padding: .5em; cursor: pointer;">String to split</summary>

```c#

theStringYouNeedToSplit = Console.ReadLine();
if(theStringYouNeedToSplit != null || theStringYouNeedToSplit != "")
{
    try
    { 
        List<string> theStringYouSplited = new List<string>(theStringYouNeedToSplit.Split("what char of string is the spliter"));
        string firstpartofthestring = theStringYouSplited[0];
        string secondpartofthestring = theStringYouSplited[1];
        ...
    }
    catch (Exception)
    {
        Console.WriteLine("Error:incorrect Syntax ");
        //you can use a goto to go back to the part where you ask tu enter a value
    }
}
else
{
    Console.WriteLine("Error:need to enter a value");
    //you can use a goto to go back to the part where you ask tu enter a value
}
```
</details>

<details style="border: 1px solid #aaa; border-radius: 4px; padding: .5em .5em 0;">
  <summary style="font-weight: bold; margin: -.5em -.5em 0; padding: .5em; cursor: pointer;">Basic String</summary>

```c#
Entry = Console.ReadLine();
if(Entry == null || Entry == "")
{
    Console.WriteLine("Error:need to enter a value");
    //you can use a goto to go back to the part where you ask tu enter a value
}

```
</details>

<details style="border: 1px solid #aaa; border-radius: 4px; padding: .5em .5em 0;">
  <summary style="font-weight: bold; margin: -.5em -.5em 0; padding: .5em; cursor: pointer;">Basic int</summary>
  
```c#
  bool isTheEntryAInt = int.TryParse(Console.ReadLine(), out entryParsedIntoInt);
if(!entryParsedIntoInt)
{
    Console.WriteLine("Error:this entry is not a int");
    //you can use a goto to go back to the part where you ask tu enter a value
}
```
  
</details>

<details style="border: 1px solid #aaa; border-radius: 4px; padding: .5em .5em 0;">
  <summary style="font-weight: bold; margin: -.5em -.5em 0; padding: .5em; cursor: pointer;">Yes or No</summary>
  
```c#

switch(Console.ReadLine())
{
    bool answer
    case "Yes":
    case "yes":
    case "Y":
    case "y":
        answer = true;
        Console.ReadKey();
        break;
    case "non":
        answer = false;
        Console.ReadKey();
        //you can use a return / break / goto to go to the desired part of the code
    default:
        Console.WriteLine("Error:not a valide entry");
        Console.ReadKey();
        //you can use a goto to go back to the part where you ask tu enter a value
}
```
  
</details>


