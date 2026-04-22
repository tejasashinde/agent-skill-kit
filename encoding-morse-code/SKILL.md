---
name: morse-code-processing
description: >
  Bidirectional Morse Code processing that encodes text into International Morse Code or decodes Morse Code into plain text using strict ITU-standard mapping. Use when converting text to Morse, Morse to text, or handling general signal translation in either direction.
---

# MORSE CODE PROCESSING

## Contents

- [Purpose](#purpose)
- [When to USE THIS SKILL](#when-to-use-this-skill)
- [Mode Selection](#mode-selection)
- [Agent Behavior (Workflow Mode)](#agent-behavior-workflow-mode)
- [Rules (Authoritative)](#rules-authoritative)
- [Morse Code Mapping (ITU Standard)](#morse-code-mapping-itu-standard)
  - [Letters (A–Z)](#letters-a-z)
  - [Numbers (0–9)](#numbers-0-9)
  - [Punctuation](#punctuation)
- [Algorithm](#algorithm)
- [Failure Handling](#failure-handling)
- [Examples](#examples)
- [Output Style Constraint](#output-style-constraint)
- [Safety / Integrity](#safety--integrity)

---

## Purpose

Provide deterministic bidirectional conversion between plain text and International Morse Code.

Focus:
- Strict ITU-standard mapping
- Fully reversible transformation
- No interpretation or summarization

---

## When to USE THIS SKILL

Activate when user requests:

### Encoding (text → Morse)
- convert to morse
- encode in morse
- text to morse
- signal conversion

### Decoding (Morse → text)
- decode morse
- morse to text
- translate morse
- dot-dash sequences (e.g., `... --- ...`)

---

## Mode Selection

Determine mode from input:

- If input contains `.` or `-` → **DECODING MODE**
- If input contains alphabetic characters (A–Z) → **ENCODING MODE**
- If input is ambiguous (valid for both modes) → **ASK USER FOR CLARIFICATION**

---

## Agent Behavior (Workflow Mode)

Execute sequentially. Do not skip steps.
```
Task Progress:

- [ ] Step 1: Detect processing mode (encoding or decoding)
- [ ] Step 2: Normalize input format
- [ ] Step 3: Tokenize input based on mode
- [ ] Step 4: Apply ITU mapping (encode or decode)
- [ ] Step 5: Validate spacing and word boundaries
- [ ] Step 6: Emit final output
```

---

### Step 1: Detect processing mode

* If input contains `.` or `-` → DECODING MODE
* Else → ENCODING MODE

---

### Step 2: Normalize input

* Encoding mode: convert text → uppercase
* Decoding mode: trim whitespace only (do not alter Morse tokens)

---

### Step 3: Tokenize input

* Encoding: split by words → characters
* Decoding: split by `" / "` → words → Morse tokens

---

### Step 4: Apply mapping

* Encoding: char → Morse
* Decoding: Morse → char
* Unknown symbols → ignore silently

---

### Step 5: Validate structure

* Encoding:

  * letters separated by single space
  * words separated by `" / "`

* Decoding:

  * preserve word boundaries exactly

---

### Step 6: Emit output

Return only final result:

* no explanation
* no labels
* no formatting
* no commentary

---

## Rules (Authoritative)

* Case-insensitive text input
* Strict ITU Morse mapping only
* Words separated by `" / "`
* Multiple spaces → treated as single word break
* Unknown characters or invalid Morse → ignored silently
* Preserve word boundaries strictly
* Entire input (including paragraphs) must be fully processed
* Output must be raw result only

---

## Morse Code Mapping (ITU Standard)

### Letters (A–Z)

| Char | Morse | Char | Morse | Char | Morse | Char | Morse |
| ---- | ----- | ---- | ----- | ---- | ----- | ---- | ----- |
| A    | .-    | B    | -...  | C    | -.-.  | D    | -..   |
| E    | .     | F    | ..-.  | G    | --.   | H    | ....  |
| I    | ..    | J    | .---  | K    | -.-   | L    | .-..  |
| M    | --    | N    | -.    | O    | ---   | P    | .--.  |
| Q    | --.-  | R    | .-.   | S    | ...   | T    | -     |
| U    | ..-   | V    | ...-  | W    | .--   | X    | -..-  |
| Y    | -.--  | Z    | --..  |      |       |      |       |

---

### Numbers (0–9)

| Char | Morse |
| ---- | ----- |
| 0    | ----- |
| 1    | .---- |
| 2    | ..--- |
| 3    | ...-- |
| 4    | ....- |
| 5    | ..... |
| 6    | -.... |
| 7    | --... |
| 8    | ---.. |
| 9    | ----. |

---

### Punctuation (ITU Standard)

| Char | Morse  | Char | Morse   | Char | Morse  |
| ---- | ------ | ---- | ------- | ---- | ------ |
| .    | .-.-.- | ,    | --..--  | ?    | ..--.. |
| '    | .----. | !    | -.-.--  | /    | -..-.  |
| (    | -.--.  | )    | -.--.-  | &    | .-...  |
| :    | ---... | ;    | -.-.-.  | =    | -...-  |
| +    | .-.-.  | -    | -....-  | _    | ..--.- |
| "    | .-..-. | $    | ...-..- | @    | .--.-. |

---

## Algorithm

### Encoding
1. Normalize input → uppercase  
2. Tokenize characters  
3. Map to Morse  
4. Join letters with space  
5. Join words with " / "  
6. Output result  

### Decoding
1. Split input by " / " into words  
2. Split words by space into symbols  
3. Map Morse → character  
4. Join characters into words  
5. Join words with space  
6. Output result

---

## Failure Handling

* Encoding failure → `""`
* Decoding failure → `""`

No exceptions. Silent fallback only.

---

## Examples

Refer [markdown](EXAMPLES.md) for detailed examples

---

## Output Style Constraint

* No explanations, no formatting, no commentary
* Only raw output allowed

---

## Safety / Integrity

* No hallucinated mappings
* Strict ITU compliance only
* No inference beyond direct mapping
* Fully deterministic behavior

---