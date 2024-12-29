from datetime import datetime
from fractions import Fraction

# Завдання 1
print((lambda year: year % 4 == 0 and (year % 100 != 0 or year % 400 == 0))(2024))  # True
print((lambda d1, d2: abs((d2 - d1).days))(datetime(2023, 1, 1), datetime(2023, 12, 31)))  # 364
print((lambda d1, d2: abs((d2 - d1).days) // 7)(datetime(2023, 1, 1), datetime(2023, 12, 31)))  # 52
print((lambda date: date.strftime('%A'))(datetime(1969, 7, 20)))  # Sunday

# Завдання 2
print((lambda a, b: a + b)(Fraction(1, 3), Fraction(2, 3)))  # 1
print((lambda a, b: a - b)(Fraction(3, 4), Fraction(1, 2)))  # 1/4
print((lambda a, b: a * b)(Fraction(2, 3), Fraction(3, 4)))  # 1/2
print((lambda a, b: a / b)(Fraction(3, 4), Fraction(2, 3)))  # 9/8

# Завдання 3
print((lambda a, b, c, d: max(a, b, c, d))(1, 2, 3, 4))  # 4
print((lambda a, b, c, d: min(a, b, c, d))(1, 2, 3, 4))  # 1

# Завдання 4
print((lambda x, y: x == y)(5, 5))  # True
print((lambda x, a, b: not (a <= x <= b))(5, 1, 4))  # True
print((lambda x: x > 0)(10))  # True
print((lambda x: x < 0)(-10))  # True
