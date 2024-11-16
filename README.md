#Q1
book_strings = [
    "Harry Potter, 101, 39.99",
    "Percy Jackson, 102, 29.99",
    "The Hobbit, 103, 49.95",
    "Alice in Wonderland, 104, 24.75",
    "Charlotte's Web, 105, 19.95",
]
class Book:
    def __init__(self, title, book_id, price):
        self.title = title
        self.book_id = book_id
        self.price = price
   
    def __str__(self):
        return f"Book(title='{self.title}', id={self.book_id}, price={self.price})"


# 1. Convert book_strings into books with title, id, and price
books = []
for book_string in book_strings:
    book_info = list(map(lambda x: x.strip(), book_string.split(",")))
    title, book_id, price = book_info
    book = Book(title, book_id, price)
    books.append(book)
# 2. Find the book with the highest price and print the details
most_expensive_book = max(books, key= lambda book: book.price)
print(f"The most expensive book is: Title: {most_expensive_book.title}, ID: {most_expensive_book.book_id}, Price: ${most_expensive_book.price}")
# 3. Find the book with the longest title.
most_expensive_book = max(books, key= lambda book: len(book.title))
print(f"The book with the longest title is: Title: {most_expensive_book.title}, ID: {most_expensive_book.book_id}, Price: ${most_expensive_book.price}")
# 4. Calculate the average price of all the books.
avg_book_price = 0
for book in books:
    avg_book_price += float(book.price)
avg_book_price /= len(books)
print(f"The average price of a book is: {avg_book_price}")
# 5. Create a list of only the titles of all the books.
book_titles = []
for book in books:
    book_titles.append(book.title)
print(*book_titles, sep= ", ") 
# 6. Count the number of books with a price above $30. # 7. Print the book titles in alphabetical order.
book_price_above_30 = []
for book in books:
    if float(book.price) >= 30.0:
        book_price_above_30.append(book.title)
print(f"There are {len(book_price_above_30)} books above 30$, the titles of the books are:",*book_price_above_30, sep=", ")
#Q2
'''fahrenheit_temps = [32, 45, 64, 72, 90, 100, 212]
#1.Convert Fahrenheit to Celsius using map function.
def fahrenheit_to_celsius(temp):
    return (temp-32)*(5/9)
celsius_temps = list(map(fahrenheit_to_celsius, fahrenheit_temps))
print(celsius_temps)
#2. Round each Celsius temperature to two decimal places.
def round_func(temp):
    return round(temp,2)
rounded_celsius_temps = list(map(round_func, celsius_temps))
print(rounded_celsius_temps)
#3. Label each temperature as "Cold Day", "Mild Day", or "Hot Day" if temp < 10 as "Cold Day", else if temp < 25 as Mild Day else hot day.
classified_temps = []
for temp in rounded_celsius_temps:
    if temp <= 10:
        classified_temps.append(f"Cold day, Temp:{temp}")
    if temp <= 25 and temp >10:
        classified_temps.append(f"Mild day, Temp:{temp}")
    if temp > 25:
        classified_temps.append(f"Hot day, Temp:{temp}")
print(classified_temps)'''
