## M302: Advanced String Toolkit – Comprehensive Text Analysis

**Assignment Overview:**
In this project, you will implement a single Python function that performs detailed text analysis on an input string—using only primitive types, loops, and string operations (no lists or dictionaries). Your function will compute and return:

1. The **reversed** string
2. The **length** (total characters)
3. The **vowel count** (A, E, I, O, U, case-insensitive)
4. The **consonant count** (letters only)
5. A **palindrome check** result (ignoring case and non-letters)

This assignment reinforces your skills in string indexing, loops, conditionals, and function design.

---

**Objectives:**
By completing this assignment, you will:

* Traverse a string character-by-character to build new strings and counts.
* Use conditional checks to classify and count characters.
* Build a cleaned, lowercase version of the text for palindrome testing.
* Compare characters from both ends to detect palindromes.
* Encapsulate all logic in a single reusable function.

> **Note:** Do **not** use lists, dictionaries, `.split()`, or any advanced data structures—only strings, integers, loops, and conditionals.

---

**Instructions:**

1. **Write the Function**

   * Signature:

     ```python
     def analyze_text(s):
         """
         Takes string s and returns:
           rev         = reversed string
           length      = total number of characters
           vowels      = count of vowels (A, E, I, O, U)
           consonants  = count of consonant letters
           is_pal      = True if s is a palindrome (letters only, case-insensitive)
         Returns: rev, length, vowels, consonants, is_pal
         """
         # your implementation
     ```
   * Inside `analyze_text`:

     * Build the **reversed** string by looping indices from end to start.
     * Count **length** by iterating once over `s`.
     * For each character:

       * If it’s a letter (`'A' ≤ ch ≤ 'Z'` or `'a' ≤ ch ≤ 'z'`), convert to lowercase:

         * Increment `vowels` if it’s one of `aeiou`; otherwise increment `consonants`.
         * Append to a `cleaned` string for palindrome testing.
     * Check **palindrome** by comparing `cleaned[i]` to `cleaned[-1-i]` for the first half.

2. **Edge Cases:**

   * Empty string → function should return `("", 0, 0, 0, True)` (an empty string is a palindrome).
   * Punctuation, spaces, and digits are ignored in vowel/consonant counts and palindrome logic.

---

**Technical Requirements:**

* **Data Types:** Only strings and integers.
* **Loops:** Use `for` or `while` loops for traversal.
* **Conditionals:** Use `if`/`else` to classify characters.
* **Functions:** Single function `analyze_text(s)` only.
* **String Operations:** Indexing, concatenation, and case conversion—no helper methods like `.split()`.

---

**Deliverables:**

* **Python Script:**

  * File name: `M302_string_toolkit.py`
  * Contains **only** the `analyze_text(s)` function as specified.

---

**Example of Usage:**

```python
# Suppose you call:
rev, length, vowels, consonants, is_pal = analyze_text("A man, a plan, a canal: Panama!")

# Expected return values:
# rev        == "!amanaP :lanac a ,nalp a ,nam A"
# length     == 30
# vowels     == 10
# consonants == 11
# is_pal     == True
```

---

**Evaluation Criteria:**

* **Correctness (50%)**

  * Accurate reversal, counts, and palindrome result.
* **Code Quality (30%)**

  * Clear, well-commented logic with meaningful variable names.
* **Edge-Case Handling (20%)**

  * Proper treatment of empty input and non-letter characters.

---

**Tip for Success:**
Plan your character-by-character passes carefully so you can compute multiple metrics in as few loops as possible—then encapsulate that logic cleanly in `analyze_text`.

---
