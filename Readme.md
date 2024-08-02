![logo]( https://github.com/nomankarim8/nomankarim8/blob/main/image.png?raw=true )


# Digital Clock

This is a simple digital clock application created using Python's `tkinter` library. The clock displays the current time and updates every second.

## Features

- Displays the current time in `HH:MM:SS AM/PM` format.
- Shows the current day of the week.
- Uses a digital font for a stylish look.
- Updates every second to ensure the time is always accurate.

## Prerequisites

- Python 3.x

## Installation

1. Clone the repository or download the `clock.py` file.

    ```sh
    git clone https://github.com/nomankarim8/digital-clock.git
    cd digital-clock
    ```

2. Make sure you have the `tkinter` library installed. This library usually comes pre-installed with Python, but if you need to install it, you can use the following command:

    ```sh
    pip install tk
    ```

## Usage

1. Navigate to the directory containing the `clock.py` file.

2. Run the `clock.py` script.

    ```sh
    python clock.py
    ```

3. A window will appear displaying the current time and day of the week.

## Code Explanation

- **Imports**:
    ```python
    from tkinter import *
    from tkinter.ttk import *
    from time import strftime
    ```

- **Root Window**:
    ```python
    root = Tk()
    root.title("Clock")
    ```

- **Time Function**:
    The `time` function fetches the current time and updates the label every second.
    ```python
    def time():
        string = strftime('%H:%M:%S %p %a')
        label.config(text=string)
        label.after(1000, time)
    ```

- **Label**:
    The label is used to display the time with a specified font, background, and foreground color.
    ```python
    label = Label(root, font=('ds-digital', 80), background='black', foreground='cyan')
    label.pack(anchor='center')
    ```

- **Initialize Time and Mainloop**:
    The `time` function is called once to initialize the clock, and `mainloop` is used to run the application.
    ```python
    time()
    mainloop()
    ```

## Author

Created by [nomankarim8](https://github.com/nomankarim8)

## License

This project is licensed under the MIT License - see the [LICENSE](licence) file for details.
```

This `README.md` file provides an overview of the project, installation instructions, usage guide, and an explanation of the code.
