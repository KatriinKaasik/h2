# Homework 2

This project is configured to work offline using local libraries in the `lib/` directory. All code resides in the default package.

## 📂 Project Structure

```
h2/
├── src/main/java/       # Application source code
│   └── IntSorting.java
├── src/test/java/       # Test code
│   ├── IntSortingTest.java
│   └── Aout.java        # Test helper utilities
├── lib/                 # Local libraries
│   ├── junit-4.13.2.jar
│   └── hamcrest-core-1.3.jar
├── bin/                 # Compiled class files
└──
```

## 🛠️ Command Line Instructions

Since the project uses the default package and local JAR files, commands differ by operating system (path separator: Windows `;` vs Linux/Mac `:`).

### Windows (Command Prompt / PowerShell)

```bash
# 1. Compile main code
javac -d bin src/main/java/*.java

# 2. Compile tests (requires lib folder and main code in bin)
javac -d bin -cp "lib/*;bin" src/test/java/*.java

# 3. Run application
java -cp bin IntSorting

# 4. Run JUnit tests
java -cp "bin;lib/*" org.junit.runner.JUnitCore IntSortingTest
```

### Linux and macOS

```bash
# 1. Compile main code
javac -d bin src/main/java/*.java

# 2. Compile tests (requires lib folder and main code in bin)
javac -d bin -cp "lib/*:bin" src/test/java/*.java

# 3. Run application
java -cp bin IntSorting

# 4. Run JUnit tests
java -cp "bin:lib/*" org.junit.runner.JUnitCore IntSortingTest
```

---

## 📋 Task Description

Description: https://enos.itcollege.ee/~japoia/algoritmid/ads_home2.html
Make sure that:
1. The insertion point is found by binary search.
2. The binary insertion sort method is significantly faster
 than the insertion sort method.
3. The tail of the sorted part of an array is shifted right
 using the System.arraycopy method - this makes your program
 much faster than in case you shift elements in loop.
4. If any sources are used, they are cited.

Kirjeldus: https://enos.itcollege.ee/~japoia/algoritmid/ads_home2.html
Kasutatud allikad tuleb viidata (programmi alguses kommentaaridena).
Elemendi lisamiskoht kahendpistemeetodis tuleb leida kahendotsingu abil.
Kahendpistemeetodi programm peab olema oluliselt kiirem tavalise
 pistemeetodi programmist.
Massiivi järjestatud osa (lisamiskoha järel) tuleb nihutada paremale
 kasutades meetodit System.arraycopy. See on palju efektiivsem
 pistekoha vabastamisest tsükli abil.

---

## ⚙️ Requirements

- **Java 8** or higher
