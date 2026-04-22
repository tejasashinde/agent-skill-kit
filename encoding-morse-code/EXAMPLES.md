## EXAMPLES

---

### **Example 1: Encoding (single word)**

Input:
```
SOS
```

Output:
```
... --- ...
```

---

### **Example 2: Encoding (multi-word phrase)**

Input:
```
HELLO WORLD
```

Output:
```
.... . .-.. .-.. --- / .-- --- .-. .-.. -..
```

---

### **Example 3: Encoding (alphanumeric input)**

Input:
```
AI 2026
```

Output:
```
.- .. / ..--- ----- ..--- -....
```

---

### **Example 4: Encoding (paragraph input)**

Input:
```
HELLO WORLD THIS IS MORSE CODE
```

Output:
```
.... . .-.. .-.. --- / .-- --- .-. .-.. -.. / - .... .. ... / .. ... / -- --- .-. ... . / -.-. --- -.. .
```

---

### **Example 5: Decoding (single word)**

Input:
```
... --- ...
```

Output:
```
SOS
```

---

### **Example 6: Decoding (multi-word message)**

Input:
```
.... . .-.. .-.. --- / .-- --- .-. .-.. -..
```

Output:
```
HELLO WORLD
```

---

### **Example 7: Decoding (number sequence)**

Input:
```
.- .. / ..--- ----- ..--- -....
```
Output:
```
AI 2026
```

---

### **Example 8: Decoding (full sentence)**

Input:
```
.... . .-.. .-.. --- / -- --- .-. ... . / -.-. --- -.. .

```

Output:
```
HELLO MORSE CODE

```
```

---