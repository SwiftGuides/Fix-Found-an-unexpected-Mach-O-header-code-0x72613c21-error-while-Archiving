# Fix-Found-an-unexpected-Mach-O-header-code-0x72613c21-error-while-Archiving
This will fix "Found an unexpected Mach-O header code: 0x72613c21" while archiving the build

#### Error Image :- 

![alt text](https://i.stack.imgur.com/7TiFe.png)

1. First Check if there are any static Frameworks present in your project . You can follow [this](https://github.com/SwiftGuides/How-to-Check-Static-and-Dynamic-Framework) guide .

2. If any Static Libraries are found then thats the culprit of your error .

3. To remove the error Go to Build Phases & Embedded Frameworks and then remove the static Framework from the list .

4. After that add That Framework in "Link Binary with libraries" under "Build Phases" section.

5. Go to General Tab and make that static Framework "Do not Embed" under section "Frameworks, Libraries & Embedded Content"

6. Now cleean build and Derived Data and Make Archive again.

7. Its done. Now you can finally export your archives. 
