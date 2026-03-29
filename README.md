# Smart-system-cpp
A simple C++ student system with login, study material, quiz, calculator, and number checking features.
<br>
Author - Abdullah Younus
#include <iostream>
#include <string>
using namespace std;

/* ---------- STUDENT DATA ---------- */
string regNo[49] = {
"2025F-BS-IT-001","2025F-BS-IT-002","2025F-BS-IT-003","2025F-BS-IT-005",
"2025F-BS-IT-006","2025F-BS-IT-007","2025F-BS-IT-009","2025F-BS-IT-010",
"2025F-BS-IT-012","2025F-BS-IT-013","2025F-BS-IT-016","2025F-BS-IT-017",
"2025F-BS-IT-018","2025F-BS-IT-021","2025F-BS-IT-022","2025F-BS-IT-026",
"2025F-BS-IT-027","2025F-BS-IT-028","2025F-BS-IT-030","2025F-BS-IT-032",
"2025F-BS-IT-033","2025F-BS-IT-034","2025F-BS-IT-036","2025F-BS-IT-038",
"2025F-BS-IT-039","2025F-BS-IT-040","2025F-BS-IT-043","2025F-BS-IT-044",
"2025F-BS-IT-045","2025F-BS-IT-046","2025F-BS-IT-051","2025F-BS-IT-052",
"2025F-BS-IT-057","2025F-BS-IT-060","2025F-BS-IT-062","2025F-BS-IT-063",
"2025F-BS-IT-064","2025F-BS-IT-065","2025F-BS-IT-066","2025F-BS-IT-067",
"2025F-BS-IT-068","2025F-BS-IT-069","2025F-BS-IT-070","2025F-BS-IT-071",
"2025F-BS-IT-074","2025F-BS-IT-076","2025F-BS-IT-077","2025F-BS-IT-078",
"2025F-BS-IT-079"
};

string names[49] = {
"Daniyal","HAMAIL","MOEEZ JAVAID","HAMNA TABBASUM",
"MUHAMMAD BILAL AHMAD","ZAYAN NADEEM","SANA TAUQEER","SIDRA",
"MUHAMMAD FARRUKH NAEEM","MUHAMMAD ABDULLAH FAISAL","SAIM SARFRAZ",
"MUHAMMAD HARIS SHABBIR","MUHAMMAD UMER","MUHAMMAD ADIL",
"AYESHA SIDDIQI","MUHAMMAD ABDULLAH YOUNUS","ZOHA ARIF","HIRA NADEEM",
"MUHAMMAD AYYAN ARHAM","FATIMA SARFRAZ","CH. MUHAMMAD HUSSAIN",
"ABDULLAH SHAHID","SHAHZAIB ZAHOOR","MAIRA FIAZ","ARFA RASHID",
"MUHAMMAD HAMZA MUNAF","FIZA SHAHID","ABDULLAH ASMAT","UME ZUMARA",
"ZAINAB CHAUDHARY","ZAID UL MUNIR","Mahad Mirza","HASSAN MASOOD",
"ABDULLAH AZHAR","ZAINAB SARFRAZ","IBTISAM UL HASSAN ZAIDI",
"MUHAMMAD SHAHEER","KABIR AHMED GILLANI","MOMINA","KINZA SHAHID",
"MUHAMMAD REHAN QAISER","M ABDULLAH MUJEER CHAUDHARY","MUHAMMAD UMER",
"WARDA SARSHAR","MUHAMMAD ZAIN UL ABIDDIN","MUHAMMAD SAAD LATIF",
"REHAN QAISER","SABIR ULLAH","BADAR"
};

string password = "372006";

/* ---------- LOGIN ---------- */
int login(string r, string p) {
    for(int i = 0; i < 49; i++) {
        if(r == regNo[i] && p == password)
            return i;
    }
    return -1;
}

/* ---------- PF STUDY ---------- */
void pfMenu(); 
/* ---------- ICT STUDY ---------- */
void ictMenu() {
    int c;
    cout << "\nICT STUDY\n";
    cout << "1 ICT\n2 IT\n3 Hardware\n4 Software\n5 Input Output\n6 Internet\n";
    cin >> c;

    if(c == 1) {
        cout << "ICT means Information and Communication Technology.\n";
        cout << "Used in education and business.\n";
        cout << "Combines communication and IT.\n";
        cout << "Fast information sharing.\n";
        cout << "Used in daily life.\n";
        cout << "Modern world depends on ICT.\n";
    }
    else if(c == 2) {
        cout << "IT means Information Technology.\n";
        cout << "Related to computers.\n";
        cout << "Deals with software.\n";
        cout << "Manages data.\n";
        cout << "Part of ICT.\n";
        cout << "Used by programmers.\n";
    }
    else if(c == 3) {
        cout << "Hardware are physical parts.\n";
        cout << "Keyboard, mouse, CPU.\n";
        cout << "Can be touched.\n";
        cout << "Without hardware no computer.\n";
        cout << "Executes software.\n";
        cout << "Needs care.\n";
    }
    else if(c == 4) {
        cout << "Software are programs.\n";
        cout << "Tell hardware what to do.\n";
        cout << "System and application types.\n";
        cout << "Cannot be touched.\n";
        cout << "Make computer useful.\n";
        cout << "Examples Windows, Word.\n";
    }
    else if(c == 5) {
        cout << "Input devices send data.\n";
        cout << "Keyboard and mouse.\n";
        cout << "Output shows result.\n";
        cout << "Monitor and printer.\n";
        cout << "Work together.\n";
        cout << "User interaction.\n";
    }
    else if(c == 6) {
        cout << "Internet connects world.\n";
        cout << "Used for communication.\n";
        cout << "Online learning.\n";
        cout << "Email and social media.\n";
        cout << "Saves time.\n";
        cout << "Provides information.\n";
    }
    else {
        cout << "Invalid choice\n";
    }
}

/* ---------- QUIZ ---------- */
int quiz() {
    int type, a, score = 0;

    cout << "\nSelect Quiz\n1 ICT Quiz\n2 PF Quiz\n";
    cin >> type;

    if(type == 1) {
        cout << "ICT Quiz\n";
        cout << "1 ICT stands for?\n1 IT\n2 Information and Communication Technology\n";
        cin >> a; if(a == 2) score++;

        cout << "2 Input device?\n1 Keyboard\n2 Monitor\n";
        cin >> a; if(a == 1) score++;

        cout << "3 Internet used for?\n1 Cooking\n2 Communication\n";
        cin >> a; if(a == 2) score++;

        cout << "4 Software means?\n1 Programs\n2 Hardware\n";
        cin >> a; if(a == 1) score++;

        cout << "Score: " << score << "/4\n";
    }
    else if(type == 2) {
        cout << "PF Quiz\n";
        cout << "1 Loop runs at least once?\n1 for\n2 do while\n";
        cin >> a; if(a == 2) score++;

        cout << "2 int x = 5 is?\n1 Variable\n2 Loop\n";
        cin >> a; if(a == 1) score++;

        cout << "Score: " << score << "/2\n";
    }
    else {
        cout << "Invalid choice\n";
    }
    return score;
}

/* ---------- MOTIVATION ---------- */
void motivation() {
    cout << "\nMOTIVATION\n";
    cout << "Practice daily.\n";
    cout << "Mistakes are learning.\n";
    cout << "Do not give up.\n";
    cout << "Understand logic.\n";
    cout << "Be consistent.\n";
    cout << "Success needs patience.\n";
}

/* ---------- CALCULATOR ---------- */
void calculator() {
    double a, b;
    char op;
    cout << "Enter number operator number: ";
    cin >> a >> op >> b;

    if(op == '+') cout << a + b;
    else if(op == '-') cout << a - b;
    else if(op == '*') cout << a * b;
    else if(op == '/') {
        if(b != 0) cout << a / b;
        else cout << "Division not allowed";
    }
    else cout << "Invalid operator";
}

/* ---------- NUMBER CHECK ---------- */
void numberCheck() {
    int n;
    bool prime = true;

    cout << "Enter number: ";
    cin >> n;

    if(n % 2 == 0) cout << "Even\n";
    else cout << "Odd\n";

    if(n > 0) cout << "Positive\n";
    else if(n < 0) cout << "Negative\n";
    else cout << "Zero\n";

    if(n <= 1) prime = false;
    for(int i = 2; i * i <= n; i++) {
        if(n % i == 0) {
            prime = false;
            break;
        }
    }

    if(prime) cout << "Prime Number\n";
    else cout << "Not Prime Number\n";
}

/* ---------- MAIN ---------- */
int main() {
    string r, p;
    int attempts = 3, choice, score = 0;

    cout << "Enter Registration Number: ";
    cin >> r;

    while(attempts > 0) {
        cout << "Enter Password: ";
        cin >> p;

        int index = login(r, p);
        if(index != -1) {
            cout << "\nWELCOME\n";
            cout << "Name: " << names[index] << endl;
            cout << "Reg No: " << regNo[index] << endl;
            cout << "BS IT Student\n";
            cout << "University of Faisalabad\n";
            cout << "First Semester\n";
            cout << "Session 2025 to 2029\n";
            break;
        }
        else {
            attempts--;
            cout << "Wrong password. Attempts left: " << attempts << endl;
            if(attempts == 0) return 0;
        }
    }

    do {
        cout << "\n1 PF Study\n2 ICT Study\n3 Quiz\n4 Motivation\n5 Calculator\n6 Number Check\n7 Exit\n";
        cin >> choice;

        if(choice == 1) pfMenu();
        else if(choice == 2) ictMenu();
        else if(choice == 3) score = quiz();
        else if(choice == 4) motivation();
        else if(choice == 5) calculator();
        else if(choice == 6) numberCheck();

    } while(choice != 7);

    cout<<"\nProject Name:Smart System\n";
        cout<<"Developed By\n";
    cout<<"1:SIDRA(10)"<<endl<<"2:ABDULLAH(26)"<<endl<<"3:HIRA(28)"<<endl<<"4:MAIRA(38)"<<endl;

    return 0;
}
void pfMenu() {
    int c;
    cout << "\nPROGRAMMING FUNDAMENTALS\n";
    cout << "1 Syntax\n2 Variables\n3 If Else\n4 Loops\n5 Functions\n6 Arrays\n";
    cin >> c;

    if(c == 1) {
        cout << "Syntax means rules of writing code.\n";
        cout << "Every language has its own syntax.\n";
        cout << "Wrong syntax causes errors.\n";
        cout << "Statements end with semicolon.\n";
        cout << "Brackets define blocks.\n";
        cout << "Example: int a = 10;\n";
    }
    else if(c == 2) {
        cout << "Variables store data in memory.\n";
        cout << "Each variable has a data type.\n";
        cout << "int, float, char, string are common.\n";
        cout << "Names should be meaningful.\n";
        cout << "Value can be changed.\n";
        cout << "Example: int age = 18;\n";
    }
    else if(c == 3) {
        cout << "If else is used for decisions.\n";
        cout << "Condition is checked.\n";
        cout << "True runs if block.\n";
        cout << "False runs else block.\n";
        cout << "Improves logic.\n";
        cout << "Used in real programs.\n";
    }
    else if(c == 4) {
        cout << "Loops repeat code.\n";
        cout << "for, while, do while loops.\n";
        cout << "Reduce repetition.\n";
        cout << "for loop when count known.\n";
        cout << "while on condition.\n";
        cout << "do while runs once.\n";
    }
    else if(c == 5) {
        cout << "Functions are reusable blocks.\n";
        cout << "Make program organized.\n";
        cout << "Reduce code size.\n";
        cout << "Can return values.\n";
        cout << "Improve readability.\n";
        cout << "main is a function.\n";
    }
    else if(c == 6) {
        cout << "Arrays store multiple values.\n";
        cout << "Same data type.\n";
        cout << "Index starts from zero.\n";
        cout << "Useful for large data.\n";
        cout << "Stored in memory.\n";
        cout << "Example: int marks[5];\n";
    }
    else {
        cout << "Invalid choice\n";
    }
}
