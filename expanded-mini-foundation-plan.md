# Expanded Mini-Foundation Builder: 1 Hour Daily Plan
*Prepared for Aerosane on 2025-03-03 18:29:24 UTC*
*Login: Aerosane*
*March 3 - March 20, 2025*

## Overview

This detailed plan expands on the daily 1-hour sessions, providing specific guidance, exercises, and additional free resources for each day. Each session is carefully designed to build a solid foundation across computer science, security, and quantum/AI domains.

## Day 1 (March 3): Learning Systems Setup

### Knowledge Building (25 min)
* **Topic**: Effective learning techniques
* **Specific Focus**:
  * Understanding spaced repetition principles
  * Active recall vs. passive review
  * The forgetting curve and how to combat it
  * Interleaving practice
* **Approach**: Read one article from each resource listed below

### Hands-On Practice (25 min)
* **Setup Anki**:
  * Download from https://apps.ankiweb.net/ (free, open-source)
  * Create your first deck named "CS-Quantum-Security Foundations"
  * Learn how to create basic cards (front/back)
  * Create 5 sample cards on any topic you know
* **Setup GitHub**:
  * Create account at github.com
  * Complete the "Hello World" guide: https://guides.github.com/activities/hello-world/
  * Initialize a repository named "learning-journey"

### Reflection & Connection (10 min)
* Create a markdown file in your GitHub repo titled "learning-journal.md"
* Write a short entry (150-200 words) addressing:
  * Your goals for the next 18 days
  * How you plan to apply spaced repetition
  * How these learning techniques might apply to quantum computing concepts

### Free Resources
* **Primary**:
  * [Learning How to Learn Coursera Course](https://www.coursera.org/learn/learning-how-to-learn) (just the videos from Week 1)
  * [Anki Manual: Getting Started](https://docs.ankiweb.net/getting-started.html)
  * [How to Remember More of What You Learn with Spaced Repetition](https://collegeinfogeek.com/spaced-repetition-memory-technique/)

* **Additional**:
  * [Nicky Case's interactive guide to spaced repetition](https://ncase.me/remember/)
  * [GitHub Markdown Guide](https://guides.github.com/features/mastering-markdown/)
  * [How to Study for a Test with Spaced Repetition](https://youtu.be/Z-zNHHpXoMM) (YouTube)

## Day 2 (March 4): Binary Fundamentals

### Knowledge Building (25 min)
* **Topic**: Number systems and binary representation
* **Specific Focus**:
  * Binary, decimal, hexadecimal, and octal systems
  * Converting between number systems
  * Representing negative numbers (two's complement)
  * Bitwise operations
* **Approach**: Work through the interactive tutorials at Computerphile and Khan Academy

### Hands-On Practice (25 min)
* **Exercise 1**: Convert the following numbers by hand:
  * Decimal to binary: 13, 27, 42, 255, 128
  * Binary to decimal: 1011, 10101, 11111111, 10000000
  * Decimal to hexadecimal: 15, 16, 42, 255
  * Hexadecimal to binary: 0xA, 0x1F, 0xFF, 0x80
* **Exercise 2**: Implement a function in Python that takes a decimal number and outputs its binary representation without using built-in conversion functions

### Reflection & Connection (10 min)
* Add to your learning journal:
  * How binary representation underlies all computing
  * How quantum bits (qubits) differ from classical bits
  * Create 3-5 Anki cards covering key binary concepts

### Free Resources
* **Primary**:
  * [Khan Academy: Binary number system](https://www.khanacademy.org/computing/computer-science/how-computers-work2/v/khan-academy-binary-numbers)
  * [Computerphile: Number Systems](https://www.youtube.com/watch?v=_SkpnG571z8)
  * [Binary Hex Decimal Converter Tool](https://www.rapidtables.com/convert/number/binary-to-decimal.html)

* **Additional**:
  * [Interactive Binary Game](https://games.penjee.com/binary-numbers-game/)
  * [Two's Complement Calculator](https://www.exploringbinary.com/twos-complement-converter/)
  * [Binary to Text Converter](https://www.convertbinary.com/)

## Day 3 (March 5): Boolean Logic

### Knowledge Building (25 min)
* **Topic**: Boolean logic operations and gates
* **Specific Focus**:
  * Basic operations: AND, OR, NOT, XOR, NAND, NOR
  * Truth tables for each operation
  * Boolean algebra laws and simplification
  * Logic gates and circuit representations
* **Approach**: Work through the Khan Academy digital logic unit, focusing on basic gates

### Hands-On Practice (25 min)
* **Exercise 1**: Draw truth tables for:
  * AND, OR, NOT, XOR, NAND, NOR gates
  * Compound operations: (A AND B) OR (NOT C)
* **Exercise 2**: Implement basic logic gates in Python:
```python
def AND(a, b):
    return a and b

def OR(a, b):
    return a or b

def NOT(a):
    return not a

def XOR(a, b):
    # Implement XOR
    pass

def NAND(a, b):
    # Implement NAND
    pass

def NOR(a, b):
    # Implement NOR
    pass

# Test your implementations