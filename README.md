# ParseMaster: A PLY-Based Lexical Analyzer and Parser

## 📌 Overview
ParseMaster is a **Python-based lexical analyzer and parser** built using **PLY (Python Lex-Yacc)**. It processes C- (C Minus) language code, tokenizes input, and constructs an **Abstract Syntax Tree (AST)**. This project is a crucial step in building **interpreters and compilers**.

## 🎯 Objective
The goal of this project is to develop a **robust lexical and syntax analyzer** that can process and understand the structure of C- programs.

### Key Features:
- **Tokenization**: Identifies keywords, identifiers, constants, operators, and symbols.
- **Abstract Syntax Tree (AST)**: Constructs a structured tree representation of the code.
- **Syntax Error Detection**: Provides error messages for invalid syntax.
- **Line Number Tracking**: Helps in debugging by tracking line numbers.
- **Efficient Parsing**: Implements a recursive descent parser for structured analysis.

## 🚀 How It Works
1. **Lexical Analysis**: Converts source code into tokens.
2. **Parsing**: Uses grammar rules to build the AST.
3. **Error Handling**: Detects and reports syntax errors.

## 🏗️ Project Structure
```
|-- Parser.py  # Main lexical analyzer and parser script
|-- cminusinput1.c  # Sample source code for testing
|-- cminusinput2.c  # Sample source code for testing
|-- cminusinput3.c  # Sample source code for testing
|-- parser.out  # Parser out file
|-- parsetab.py  # parsetab file
|-- Parser-Report.pdf  # Report
|-- README.md  # Documentation
```

## 🛠️ Technologies Used
- **Python** for processing.
- **PLY (Python Lex-Yacc)** for lexical and syntax analysis.
- **Abstract Syntax Tree (AST)** for structured parsing.

## 📖 Getting Started
### Prerequisites
- Python 3.8+
- Install PLY:
  ```bash
  pip install ply
  ```

### Running the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/HareenaChowdary/ParseMaster.git 
   cd ParseMaster
   ```
2. Run the parser:
   ```bash
   python Parser.py
   ```

## 🧐 Example Output
Given the following input in `cminusinput1.c`:
```c
int main() {
  int x = 10;
  x = x + 5;
  return x;
}
```
ParseMaster will output the following AST:
```bash
Program :
  ProcedureDecl :
    FunctionDecl :
      Type : int
      IDENTIFIER : main
    ProcedureBody :
      StatementList :
        Assignment :
          Variable : x
          AddExpr :
            Constant : 10
        Assignment :
          Variable : x
          AddExpr :
            Variable : x
            Constant : 5
        ReturnStatement :
          Variable : x
```

## 🤝 Contributing
Pull requests are welcome! If you find a bug or want to enhance the functionality, feel free to contribute.

## 📧 Contact
Looking for collaboration? Reach out on [LinkedIn](https://www.linkedin.com/in/hareena-chowdary-polavaram/).

---
🚀 **ParseMaster – Turning Code into Structured Syntax!**

