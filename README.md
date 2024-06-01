- 👋 Hi, I’m @anshulCHAURASI
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
anshulCHAURASI/anshulCHAURASI is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Public Notes</title>
    <style>
        /* Basic CSS for styling */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
        }
        header {
            background-color: #333;
            color: #fff;
            padding: 10px;
            text-align: center;
        }
        section {
            padding: 20px;
            margin: 20px auto;
            max-width: 600px;
        }
        .note {
            border: 1px solid #ddd;
            padding: 10px;
            margin-bottom: 10px;
        }
    </style>
</head>
<body>
    <header>
        <h1>Public Notes</h1>
    </header>
    <section>
        <h2>Upload Your Note</h2>
        <form id="noteForm">
            <textarea id="noteContent" rows="4" cols="50" placeholder="Enter your note here"></textarea>
            <br>
            <button type="submit">Upload</button>
        </form>
    </section>
    <section id="notesContainer">
        <h2>Public Notes</h2>
        <!-- Notes will be displayed here -->
    </section>

    <script>
        // JavaScript for handling form submission and displaying notes
        const noteForm = document.getElementById('noteForm');
        const noteContent = document.getElementById('noteContent');
        const notesContainer = document.getElementById('notesContainer');

        noteForm.addEventListener('submit', function(event) {
            event.preventDefault();
            const noteText = noteContent.value.trim();
            if (noteText !== '') {
                // Create a new note element
                const noteElement = document.createElement('div');
                noteElement.classList.add('note');
                noteElement.textContent = noteText;

                // Append the note to the container
                notesContainer.appendChild(noteElement);

                // Clear the textarea
                noteContent.value = '';
            } else {
                alert('Please enter a note before uploading.');
            }
        });
    </script>
</body>
</html>
