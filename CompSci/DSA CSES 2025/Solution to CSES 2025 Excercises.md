Kunci jawaban Two Same Turing Machine code
def create_rules():
    rules = []
 
    rules.append(("L", 1, "L", 1, "RIGHT"))
    rules.append(("0", 1, "A", 2, "RIGHT"))
    rules.append(("1", 1, "B", 2, "RIGHT"))
    rules.append(("A", 1, "A", 1, "RIGHT"))
    rules.append(("B", 1, "B", 1, "RIGHT"))
    rules.append(("0", 2, "0", 2, "RIGHT"))
    rules.append(("1", 2, "1", 2, "RIGHT"))
    rules.append(("C", 2, "C", 2, "RIGHT"))
    rules.append(("D", 2, "D", 2, "RIGHT"))
 
    rules.append(("R", 2, "R", 3, "LEFT"))
    rules.append(("0", 3, "C", 4, "LEFT"))
    rules.append(("1", 3, "D", 4, "LEFT"))
    rules.append(("C", 3, "C", 3, "LEFT"))
    rules.append(("D", 3, "D", 3, "LEFT"))
    rules.append(("0", 4, "0", 4, "LEFT"))
    rules.append(("1", 4, "1", 4, "LEFT"))
    rules.append(("A", 4, "A", 4, "LEFT"))
    rules.append(("B", 4, "B", 4, "LEFT"))
    rules.append(("L", 4, "L", 1, "RIGHT"))
 
    rules.append(("C", 1, "C", 5, "LEFT"))
    rules.append(("D", 1, "D", 5, "LEFT"))
    rules.append(("A", 5, "A", 5, "LEFT"))
    rules.append(("B", 5, "B", 5, "LEFT"))
    rules.append(("L", 5, "L", 6, "RIGHT"))
    rules.append(("X", 6, "X", 6, "RIGHT"))
    rules.append(("A", 6, "X", 7, "RIGHT"))
    rules.append(("B", 6, "X", 8, "RIGHT"))
    rules.append(("A", 7, "A", 7, "RIGHT"))
    rules.append(("A", 8, "A", 8, "RIGHT"))
    rules.append(("B", 7, "B", 7, "RIGHT"))
    rules.append(("B", 8, "B", 8, "RIGHT"))
    rules.append(("X", 7, "X", 7, "RIGHT"))
    rules.append(("X", 8, "X", 8, "RIGHT"))
    rules.append(("C", 7, "X", 5, "LEFT"))
    rules.append(("D", 8, "X", 5, "LEFT"))
    rules.append(("X", 5, "X", 5, "LEFT"))
    rules.append(("R", 6, "R", 6, "ACCEPT"))
 
    return rules

[CSES](https://cses.fi/)  (see if it still works lol)