phonenums-v2

# Extract Phone Numbers from text v2
I had a lot of fun making this because this is my first ever GUI project in python. The first one is always close to your heart. This script plucks Indian phone numbers out of messy text files, like OCR outputs or e-paper dumps and neatly tucks them into a CSV.

## What it Does
- No more dealing with long file paths. Use a standard file dialog to find your OCR files.
- India-Centric: Specifically tuned to find Indian phone formats (National and +91).
- It automatically de-duplicates the list. If a number appears ten times in your text, it only appears once in your CSV.
- CSV Export: Saves everything into a tidy epaper_phones.csv right where the script lives.

## Getting Started
1. Prerequisites
You’ll need Python 3 installed. You also need the phonenumbers library:

- `pip install phonenumbers`
- Tkinter comes pre-installed with most Python distributions, so you're likely good to go.)

2. Usage
- Run the script: python "phonenums v2.py"
- Click the "Try Clicking Me!" button.
- Select your .txt file from the file explorer.
- Once the "Extracted phones" message pops up, check your folder for epaper_phones.csv.

![phonenums v2 gif](https://github.com/user-attachments/assets/ed6bc564-0427-464e-800b-1504ad8f694e)

## Built With
- Standard Python Tkinter Library: For the window, file dialog & messagebox features for the GUI.
- Standard Python csv module.
- [python-phonenumbers](https://github.com/daviddrysdale/python-phonenumbers) - A Python port of Google's libphonenumber. This library handles the heavy lifting of extracting and validating the phone numbers.

## What’s New (Comparison with v1)
If you used the previous version of this tool, here is what has changed in this update:

- GUI vs. CLI: I have upgraded from the command line. Praise me. Instead of pasting paths into a terminal, now there's a window with buttons and labels. I made it pink.
- Visual File Picker: The "Pro Tip" about avoiding quotes and double backslashes in paths is long gone now. The new filedialog handles the pathing for you automatically.

## Implementation Notes
- If you want to change the default folder that opens when you click the button, look for this line in the code and swap the path:
**Change this path to your preferred folder**
`filepath = filedialog.askopenfilename(initialdir="C:\\Your\\Path\\Here")`
- Where's my file? The output (epaper_phones.csv) saves directly to the directory where you ran the script.
- Indian Numbers Only: This project is currently tuned for the Indian National Format. If it's skipping numbers, double-check if they follow the +91 or 10-digit standard.
