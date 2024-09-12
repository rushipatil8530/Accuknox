class Rectangle:
    def __init__(self, length: int, width: int):
        self.length = length
        self.width = width

    def __iter__(self):
        yield {'length': self.length}
        yield {'width': self.width}

# Example usage:
rect = Rectangle(10, 5)

# Iterating over the rectangle instance
for dimension in rect:
    print(dimension)
# Explanation:
The __init__ method initializes the Rectangle object with length and width.
The __iter__ method is defined to make the class iterable. It yields the length first as a dictionary and then the width.
# Example Output 
{'length': 10}
{'width': 5}
