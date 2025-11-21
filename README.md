Offline Vocabulary Master
The Offline Vocabulary Master is a single-file, client-side application designed to help users learn and review vocabulary using spaced repetition (SRS) flashcards and quizzes. All data, including your word list and progress, is saved directly in your browser's local storage, making it fully functional offline.

Features
Offline First: All data is stored locally in your browser and is accessible without an internet connection.

Flashcard Mode (SRS):

Review words based on an Spaced Repetition System, scheduling words marked as Easy for 7 days, Hard for 3 days, and Super Hard for 1 day.

Automatic Advancement: Clicking an "Easy," "Hard," or "Super Hard" button automatically saves progress and moves to the next word.

Mobile Gestures: Supports swiping for navigation and marking difficulty (configurable in Settings).

Quiz Mode:

Recognition (MCQ): Choose the correct meaning for a given word.

Recall (Type In): Type the correct word for a given definition.

Visual Feedback: In Quiz mode, the selected option turns green if correct and red if wrong.

Quiz Completion: A pop-up modal appears when all eligible words have been completed, allowing the user to restart the quiz immediately.

Targets words due for review (based on the SRS schedule) and words recently missed.

Word Manager: Import new vocabulary in bulk using a simple JSON array format.

Data Sync: Export and Import all vocabulary and progress data via a compressed QR code, allowing easy synchronization between multiple devices.

Settings: Toggle Dark Mode, adjust quiz settings, and customize mobile swipe actions.

Getting Started
Since this is a single HTML file application, setup is very straightforward.

Prerequisites
A modern web browser (Chrome, Firefox, Edge, Safari).

Installation (Local)
Save the index2.html file to your computer.

Open the file directly in your web browser.

No web server or compilation is required. The application uses only external CDN scripts (Tailwind CSS, QRCodejs, Pako) for styling and data compression/QR generation.

Usage Guide
1. Word Manager (First Steps)
If you are starting fresh, your first step should be to add vocabulary.

Navigate to the ➕ Word Manager tab.

In the Import New Vocabulary section, paste a JSON array of words in the following format:

JSON

[
  {"word": "newword", "meaning": "the meaning of the word", "tag": "category_name"},
  {"word": "ephemeral", "meaning": "lasting for a very short time", "tag": "time_short"}
]
Click Import & Save New Words.

2. Flashcard Mode (Learning)
Navigate to the 📚 Flashcards tab.

Click the card to reveal the meaning (front/back flip).

Once reviewed, mark your knowledge level using the buttons:

Easy (7 Days): Good recall, seen in a week.

Hard (3 Days): Needs practice, seen in a few days.

Super Hard (1 Day): Difficult, seen tomorrow.

The application will automatically proceed to the next card after you select a difficulty.

Use the Previous and Next Word buttons for manual navigation, or swipe horizontally on the card in mobile view.

3. Quiz Mode (Testing)
Navigate to the ❓ Take Quiz tab.

The quiz will automatically select words that are due for review based on the SRS schedule and any words you previously missed.

Choose between Recognition (MCQ) or Recall (Type In).

After submitting an answer:

Options will display green for the correct answer and red for the wrong answer.

The word's progress is automatically updated (missed words are rescheduled for the next day).

Click Next Question → to continue. If the quiz runs out of words, you will be prompted to restart.

4. Data Sync
Go to ➕ Word Manager.

Click Export & Generate QR Code (Source). A QR code containing all your vocabulary and progress will appear.

On the target device, open the app and go to ➕ Word Manager.

Scan the QR code to capture the compressed text.

Paste the text into the sync-import-area.

Click Import & Update All Data (Target). This will overwrite the target device's data with the data from the source device.

Technologies Used
HTML5 / JavaScript (Vanilla): Core application structure and logic.

Tailwind CSS: Utility-first framework for modern styling and responsive design.

Pako: JavaScript library for zlib compression/decompression, used to compress the large data payload for QR code transfer.

QRCode.js: Library for generating QR codes directly in the browser.
