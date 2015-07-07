=======
Notizen
=======

Module
------

Um ein Modul zu importieren gibt es folgenden Befehl

``$ import <Modulname>``


Die Funktionen werden nicht automatisch in die gloable Symboltabelle eingefügt. Um diese anzusprechen, benutzt man den Modulnamen

``$ Modulname.function()``

Wenn man plant, eine Funktion öfters zu verwenden, kann man diese an einen lokalen Namen binden

``$ var = Modulname.function``

Es gibt eine Variante der import-Anweisung, welche bestimmte Namen aus einem Modul direkt in die Symboltabelle des importierenden Moduls einfügt

``$ from Modulname import function1, function2``

Zusätzlich gibt es eine Variante um alle Namen eines Moduls zu importieren

``$ from Modulname import *``


dir()-Funktion
""""""""""""""

Die eingebaute Funktion dir() wird benutzt, um herauszufinden, welche Namen in einem Modul definiert sind. Es wird eine sortierte Liste von Strings zurückgegeben

dir() listet allerdings nicht die Namen der eingebauten Funktionen und Variablen auf. Falls man diese auflisten will, muss man das Standardmodul builtins verwenden

``$ import builtins``
``$ dir(builtins)``
``['ArithmeticError', 'AssertionError', 'AttributeError', 'BaseException',
'BufferError', 'BytesWarning', 'DeprecationWarning', 'EOFError', 'Ellipsis',
'EnvironmentError', 'Exception', 'False', 'FloatingPointError',
'FutureWarning', 'GeneratorExit', 'IOError', 'ImportError', 'ImportWarning',
'IndentationError', 'IndexError', 'KeyError', 'KeyboardInterrupt',
'LookupError', 'MemoryError', 'NameError', 'None', 'NotImplemented',
'NotImplementedError', 'OSError', 'OverflowError',
'PendingDeprecationWarning', 'ReferenceError', 'RuntimeError',
'RuntimeWarning', 'StopIteration', 'SyntaxError', 'SyntaxWarning',
'SystemError', 'SystemExit', 'TabError', 'True', 'TypeError',
'UnboundLocalError', 'UnicodeDecodeError', 'UnicodeEncodeError',
'UnicodeError', 'UnicodeTranslateError', 'UnicodeWarning', 'UserWarning',
'ValueError', 'Warning', 'ZeroDivisionError', '__build_class__',
'__debug__', '__doc__', '__import__', '__name__', '__package__', 'abs',
'all', 'any', 'ascii', 'bin', 'bool', 'bytearray', 'bytes', 'chr',
'classmethod', 'compile', 'complex', 'copyright', 'credits', 'delattr',
'dict', 'dir', 'divmod', 'enumerate', 'eval', 'exec', 'exit', 'filter',
'float', 'format', 'frozenset', 'getattr', 'globals', 'hasattr', 'hash',
'help', 'hex', 'id', 'input', 'int', 'isinstance', 'issubclass', 'iter',
'len', 'license', 'list', 'locals', 'map', 'max', 'memoryview', 'min',
'next', 'object', 'oct', 'open', 'ord', 'pow', 'print', 'property', 'quit',
'range', 'repr', 'reversed', 'round', 'set', 'setattr', 'slice', 'sorted',
'staticmethod', 'str', 'sum', 'super', 'tuple', 'type', 'vars', 'zip']``

