# program-using-string
String Example
public class StringPrograms {
public static void main(String[] args) {
Scanner scanner = new Scanner(System.in);
System.out.print("Enter the first string: ");
String str1 = scanner.nextLine();
System.out.print("Enter the second string: ");
String str2 = scanner.nextLine();
System.out.println("\nChoose a string operation:");
System.out.println("1. Find Length");
System.out.println("2. Convert to Uppercase");
System.out.println("3. Convert to Lowercase");
System.out.println("4. Reverse the String");
System.out.println("5. Concatenate Strings");
System.out.println("6. Compare Strings");
System.out.println("7. Check if Substring Exists");
System.out.println("8. Replace a Character");
System.out.println("9. Find Character at Index");
System.out.println("10. Split the String");
System.out.println("11. Trim Whitespaces");
System.out.println("12. Check if String is Empty");
System.out.println("13. Convert to Character Array");
System.out.println("14. Exit");
int choice;
do {
System.out.print("\nEnter your choice:");
choice = scanner.nextInt();
scanner.nextLine();
switch (choice) {
case 1:
System.out.println("Length of first string: " + str1.length());
System.out.println("Length of second string: " + str2.length());
break;
case 2:
System.out.println("First string in uppercase: " + str1.toUpperCase());
System.out.println("Second string in uppercase: "+ str2.toUpperCase());
break;
case 3:
System.out.println("First string in lowercase: " + str1.toLowerCase());
System.out.println("Second string in lowercase: " + str2.toLowerCase());
break;
case 4:
System.out.println("Reversed first string: " + new StringBuilder(str1).reverse());
System.out.println("Reversed second string: " + new StringBuilder(str2).reverse());
break;
case 5:
System.out.println("Concatenated string: " + str1.concat(str2));
break;
case 6:
int comparison = str1.compareTo(str2);
if (comparison == 0) {
System.out.println("Strings are equal.");

} else if (comparison &gt; 0) {
System.out.println(&quot;First string is lexicographically greater.&quot;);
} else {
System.out.println(&quot;Second string is lexicographically greater.&quot;);
}
break;
case 7:
System.out.print(&quot;Enter a substring to check in the first string: &quot;);
String substring = scanner.nextLine();
if (str1.contains(substring)) {
System.out.println(&quot;Substring exists in the first string: &quot; +
str1.contains(substring));
} else {
System.out.println(&quot;Substring does not exist in the first string.&quot;);
}
break;
case 8:
System.out.print(&quot;Enter the character to replace: &quot;);
char oldChar = scanner.next().charAt(0);
System.out.print(&quot;Enter the new character: &quot;);
char newChar = scanner.next().charAt(0);
System.out.println(&quot;First string after replacement: &quot; + str1.replace(oldChar,
newChar));
System.out.println(&quot;Second string after replacement: &quot; + str2.replace(oldChar,
newChar));
break;
case 9:
System.out.print(&quot;Enter the index to find the character (0-based): &quot;);
int index = scanner.nextInt();
try {
System.out.println(&quot;Character at index &quot; + index + &quot; in first string: &quot; +
str1.charAt(index));
System.out.println(&quot;Character at index &quot; + index + &quot; in second string: &quot; +
str2.charAt(index));
} catch (IndexOutOfBoundsException e) {
System.out.println(&quot;Index out of range!&quot;);
}
break;
case 10:

System.out.print(&quot;Enter the delimiter to split the first string: &quot;);
String delimiter = scanner.nextLine();
String[] parts = str1.split(delimiter);
System.out.println(&quot;First string split into parts:&quot;);
for (String part : parts) {
System.out.println(part);
}
String[] parts2 = str2.split(delimiter);
System.out.println(&quot;Second string split into parts:&quot;);
for (String part : parts2) {
System.out.println(part);
}
break;
/* For example, if str1 = “apple,banana,orange” and the user inputs , (comma) as the
delimiter.
The string will be split into the array [“apple”, “banana”, “orange”]
Each of these substrings will be printed in the new line:
apple
banana
orange
*/
case 11:
System.out.println(&quot;First string after trimming: [&quot; + str1.trim() + &quot;]&quot;);
System.out.println(&quot;Second string after trimming: [&quot; + str2.trim() + &quot;]&quot;);
 System.out.println("First string after trimming: [" + str1.trim() + "]");
   System.out.println("Second string after trimming: [" + str2.trim() + "]");
                    break;
                case 12:
                    System.out.println("Is the first string empty? " + str1.isEmpty());
                    System.out.println("Is the second string empty? " + str2.isEmpty());
                    break;
                case 13:
                    System.out.println("Character array of first string:");
                    for (char c : str1.toCharArray()) {
                        System.out.print(c + " ");
                    }
                    System.out.println();
                    break;
                case 14:
                    System.out.println("Exiting...");
                    break;
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        } while (choice != 14);
        scanner.close();
    }
}
Enter the first string: welcome
Enter the second string: how are you

Choose a string operation:
1. Find Length
2. Convert to Uppercase
3. Convert to Lowercase
4. Reverse the String
5. Concatenate Strings
6. Compare Strings
7. Check if Substring Exists
8. Replace a Character
9. Find Character at Index
10. Split the String
11. Trim Whitespaces
12. Check if String is Empty
13. Convert to Character Array
14. Exit

Enter your choice: 1
Length of first string: 8
Length of second string: 11

Enter your choice: 2
First string in uppercase: WELCOME
Second string in uppercase: HOW ARE YOU
