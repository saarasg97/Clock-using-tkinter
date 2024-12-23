# Clock-using-tkinter
A simple Python digital clock using tkinter, displaying real-time updates in a 12-hour format. Lightweight, customizable, and perfect for learning Python GUI development.

# Digital Clock Using Python and Tkinter

This repository contains a simple digital clock application built using Python and the tkinter library. The clock displays the current time in a 12-hour format with AM/PM indicators, updating in real-time every second.

## Features
- **Real-Time Updates**: Displays the current time dynamically, refreshed every second.
- **Customizable Design**: Easily modify the font, background, and text colors to suit your preferences.
- **Lightweight and Efficient**: Runs smoothly with minimal resource usage.
- **Beginner-Friendly**: Ideal for learning Python and GUI programming with tkinter.

## Technologies Used
- **Python**: Core programming language.
- **Tkinter**: Built-in library for creating graphical user interfaces.

## How to Use
1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/yourusername/digital-clock.git
   ```
2. Navigate to the project directory:
   ```bash
   cd digital-clock
   ```
3. Run the application:
   ```bash
   python clock.py
   ```

## Code Overview
The application uses tkinter to create a window and label for displaying the clock. The `strftime` function from the `time` module is used to fetch the current time, which is updated every second using the `after` method.

### Key Code Snippet
```python
from tkinter import *
from time import strftime

root = Tk()
root.title('Clock')

lbl = Label(root, font=('calibri', 40, 'bold'), background='purple', foreground='white')
lbl.pack()

def time():
    string = strftime('%H:%M:%S %p')
    lbl.config(text=string)
    lbl.after(1000, time)

time()
root.mainloop()
```

## Customization
- **Font and Size**: Modify the `font` attribute in the `Label` widget.
- **Background and Text Colors**: Adjust the `background` and `foreground` attributes.
- **Time Format**: Change the `strftime` format string to customize time display (e.g., 24-hour format).

## License
This project is licensed under the MIT License. You are free to use, modify, and distribute the code.

---

Feel free to contribute by submitting issues or pull requests. Happy coding!

