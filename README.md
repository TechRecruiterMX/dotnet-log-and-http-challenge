💻 .NET/C# Coding Challenge

A two-part backend algorithm challenge focused on string processing, log analysis, and HTTP client handling in .NET.

🧩 Overview

This challenge consists of two independent tasks, both meant to evaluate your skills with:

C#/.NET fundamentals

Algorithms & data manipulation

Clean code practices

HTTP communication

Error handling and defensive programming

Each task can be solved individually, and both should be completed using .NET 6+ or .NET 7+.

🧠 Challenge 1 — Transaction Log Analyzer

You are given:

A list of log entries (List<string>)

Each entry contains a user’s license plate (matrícula) and additional transaction info

An integer parameter minTransactions

🎯 Goal

Write a function that:

Processes all log strings

Extracts the license plates

Counts how many transactions each plate appears in

Returns a List<string> containing all license plates whose transaction count is:

≥ minTransactions

📝 Example Input
var logs = new List<string>
{
    "2024-01-10 12:00:01 | ABC1234 | Payment Registered",
    "2024-01-10 12:05:11 | BBB9000 | Payment Registered",
    "2024-01-10 12:12:31 | ABC1234 | Toll Processed",
    "2024-01-10 13:10:54 | XYZ7777 | Toll Processed",
    "2024-01-10 14:01:02 | ABC1234 | Notification Sent"
};

int minTransactions = 2;

✅ Expected Output
{ "ABC1234" }

📌 Notes

You may assume logs are consistently formatted.

Focus on LINQ, dictionaries, and clean code.

Complexity matters: aim for O(n).

🌐 Challenge 2 — HTTP Client Parameter Extractor

Create a .NET console app or library that:

Uses HttpClient to call a given public API endpoint

Reads and parses the JSON response

Extracts and returns specific parameters requested (will be provided)

Handles failure scenarios properly:

network errors

invalid JSON

missing fields

retry logic (optional but a plus)

📝 Example Pseudocode
using var client = new HttpClient();
var response = await client.GetAsync("https://example.com/api/data");
var json = await response.Content.ReadAsStringAsync();

// Parse JSON and extract fields

🎯 Expected Output

A simple object or DTO containing the extracted fields.

⭐ Extra Points

Use System.Text.Json with strong typing

Add cancellation tokens

Implement retry with exponential backoff

📦 Requirements

✔ .NET 6 or .NET 7

✔ Clean folder structure

✔ Clear separation of concerns

✔ Meaningful variable/method names

✔ Unit tests (optional but recommended)

📁 Suggested Repository Structure
/src
   /Challenge1
   /Challenge2
/tests
   /Challenge1.Tests
   /Challenge2.Tests
README.md
.gitignore

🚀 Submission Instructions

Create your own GitHub repository

Add your code inside /src

Push your final solution

Optional: include instructions on how to run it

Send the link to your completed repository

🙌 Additional Notes

You can solve each challenge independently.

Completing both is ideal but partial submissions are acceptable.

This challenge is designed to evaluate real-world backend problem-solving.
