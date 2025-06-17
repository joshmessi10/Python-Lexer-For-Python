# 🗂️ Lexical Analyzer in Python
## 🤖 What is a Lexical Analyzer?

A **lexical analyzer** (also known as a *lexer* or *scanner*) is the first phase of a compiler. It takes a stream of characters (typically source code) and groups them into **tokens**, which are sequences of characters with a collective meaning.  
For example, in the statement `x = 5 + y`, the lexer would produce tokens such as `<id,x>`, `<assign,=>`, `<num,5>`, `<plus,+>`, and `<id,y>`.

This process allows the next stages of compilation (like parsing and semantic analysis) to work with a simplified and structured version of the input code.

---

## 🎯 Project Objective

This project is designed to take a source code file written in Python and perform **lexical analysis** on it.

A Python program is implemented that receives a `.py` file as input and produces a `.txt` file as output, containing the lexical analysis results.

---

## 🧷 Requirements

### ✅ Dependencies

- **Python 3** or higher must be installed on your system.

---

## 👾 How to Use

1. Download all provided project files.
2. Edit the file `codigo.py` to include your own Python code, or use the provided example.
3. Run the following command in your terminal:

```
python3 analizador_lexico.py codigo.py
```

The lexical analysis result will be saved in the output file named: "resultado_lexico.txt"

---

## 📄 Example:

*codigo.py*

```
class Animal(object): 
    makes_noise:bool = False 
     
    def make_noise(self: "Animal") -> object: 
        if (self.makes_noise): 
            print(self.sound()) 
     
    def sound(self: "Animal") -> str: 
        return "???" 
     
class Cow(Animal): 
    def __init__(self: "Cow"):                  
        self.makes_noise = True 
     
    def sound(self: "Cow") -> str: 
        return "moo" 
     
c:Animal = None 
c = Cow() 
c.make_noise()             # Prints "moo" ''
```

resultado_lexico.txt
```
<class,1,1>
<id,Animal,1,7>
<tk_par_izq, 1, 13>
<object,1,14>
<tk_par_der, 1, 20>
<tk_dos_puntos, 1, 21>
<id,makes_noise,2,5>
<tk_dos_puntos, 2, 16>
<bool,2,17>
<tk_asig, 2, 22>
<False,2,24>
<def,4,5>
<id,make_noise,4,9>
<tk_par_izq, 4, 19>
<self,4,20>
<tk_dos_puntos, 4, 24>
<tkn_cadena,"Animal",4,26>
<tk_par_der, 4, 34>
<tk_ejecuta, 4, 36>
<object,4,39>
<tk_dos_puntos, 4, 45>
<if,5,9>
<tk_par_izq, 5, 12>
<self,5,13>
<tk_punto, 5, 17>
<id,makes_noise,5,18>
<tk_par_der, 5, 29>
<tk_dos_puntos, 5, 30>
<print,6,13>
<tk_par_izq, 6, 18>
<self,6,19>
<tk_punto, 6, 23>
<id,sound,6,24>
<tk_par_izq, 6, 29>
<tk_par_der, 6, 30>
<tk_par_der, 6, 31>
<def,8,5>
<id,sound,8,9>
<tk_par_izq, 8, 14>
<self,8,15>
<tk_dos_puntos, 8, 19>
<tkn_cadena,"Animal",8,21>
<tk_par_der, 8, 29>
<tk_ejecuta, 8, 31>
<str,8,34>
<tk_dos_puntos, 8, 37>
<return,9,9>
<tkn_cadena,"???",9,16>
<class,11,1>
<id,Cow,11,7>
<tk_par_izq, 11, 10>
<id,Animal,11,11>
<tk_par_der, 11, 17>
<tk_dos_puntos, 11, 18>
<def,12,5>
<__init__,12,9>
<tk_par_izq, 12, 17>
<self,12,18>
<tk_dos_puntos, 12, 22>
<tkn_cadena,"Cow",12,24>
<tk_par_der, 12, 29>
<tk_dos_puntos, 12, 30>
<self,13,9>
<tk_punto, 13, 13>
<id,makes_noise,13,14>
<tk_asig, 13, 26>
<True,13,28>
<def,15,5>
<id,sound,15,9>
<tk_par_izq, 15, 14>
<self,15,15>
<tk_dos_puntos, 15, 19>
<tkn_cadena,"Cow",15,21>
<tk_par_der, 15, 26>
<tk_ejecuta, 15, 28>
<str,15,31>
<tk_dos_puntos, 15, 34>
<return,16,9>
<tkn_cadena,"moo",16,16>
<id,c,18,1>
<tk_dos_puntos, 18, 2>
<id,Animal,18,3>
<tk_asig, 18, 10>
<None,18,12>
<id,c,19,1>
<tk_asig, 19, 3>
<id,Cow,19,5>
<tk_par_izq, 19, 8>
<tk_par_der, 19, 9>
<id,c,20,1>
<tk_punto, 20, 2>
<id,make_noise,20,3>
<tk_par_izq, 20, 13>
<tk_par_der, 20, 14>
```


### 👥 Team Members:

- [Josh Lopez](https://github.com/joshmessi10)
- [Miguel Suarez](https://github.com/PlusMore75)
- [Maria Alejandra Vargas](https://github.com/Malejav18)
