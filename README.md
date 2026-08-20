# Object-Oriented Programming: Library Management Lab

This project applies core object-oriented programming concepts to a small library management system. The notebook models several kinds of library items using a shared base class and specialized subclasses.

## Project Goal

Design a reusable class hierarchy that captures behavior shared by all library items while allowing books, magazines, and DVDs to define their own attributes and functionality.

## Concepts Practiced

- Python classes and objects
- `__init__` constructors
- Instance attributes
- Inheritance
- `super()`
- Method overriding
- State changes through methods
- Sets and class-specific behavior

## Class Design

### `LibraryItem`
Common attributes:
- `title`
- `author`
- `publication_year`
- `is_available`

Common methods:
- `display_info()`
- `checkout()`
- `return_item()`

### `Book`
Extends `LibraryItem` with:
- `isbn`
- `publisher`

Overrides `display_info()` to include book-specific information.

### `Magazine`
Extends `LibraryItem` with:
- `issue_number`
- `publication_month`

Overrides `display_info()` to include magazine-specific information.

### `DVD`
Extends `LibraryItem` with:
- `duration`
- `director`
- `genres`
- default `author='N/A'`

Adds:
- `add_genre()`

## Testing

The notebook creates sample `Book`, `Magazine`, and `DVD` objects and verifies:

- inherited attributes
- overridden display methods
- checkout and return behavior
- DVD genre updates

## Potential Improvements

A fuller library system could add:

- validation for IDs and publication dates
- checkout guards for unavailable items
- multiple-copy inventory tracking
- persistent database storage
- search and sorting utilities
- additional subclasses such as `Audiobook` and `Journal`

## Files

- `oop_lab.ipynb` — completed lab notebook
- `README.md` — project overview

## Run the Project

Open `oop_lab.ipynb` in Jupyter Notebook, JupyterLab, VS Code, or Google Colab and run the cells from top to bottom.
