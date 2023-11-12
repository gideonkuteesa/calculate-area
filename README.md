# calculate-area
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

    def __str__(self):
        return f"({self.x}, {self.y})"


class Rectangle:
    def __init__(self, top_left, bottom_right):
        self.top_left = top_left
        self.bottom_right = bottom_right

    def area(self):
        width = self.bottom_right.x - self.top_left.x
        height = self.bottom_right.y - self.top_left.y
        return width * height

    def __str__(self):
        return f"Rectangle with top left corner at {self.top_left} and bottom right corner at {self.bottom_right}"


class Circle:
    def __init__(self, center, radius):
        self.center = center
        self.radius = radius

    def area(self):
        return 3.14 * self.radius ** 2

    def __str__(self):
        return f"Circle with center at {self.center} and radius {self.radius}"


def main():
    # Create a rectangle
    rectangle = Rectangle(Point(0, 0), Point(10, 10))

    # Create a circle
    circle = Circle(Point(5, 5), 5)

    # Print the area of the rectangle
    print(f"Area of the rectangle: {rectangle.area()}")

    # Print the area of the circle
    print(f"Area of the circle: {circle.area()}")


if __name__ == "__main__":
    main()
