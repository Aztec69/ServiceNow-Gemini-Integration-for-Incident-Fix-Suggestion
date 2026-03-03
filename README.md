# ServiceNow-Gemini-Integration-for-Incident-Fix-Suggestion
This integration creates an AI-powered assistant directly inside your ServiceNow instance to help IT agents resolve incidents faster.

The Use Case:
In a standard IT support workflow, an agent has to read a user's problem and manually research a solution. With this integration:
The agent simply clicks a "Generate AI Fix" button.
The Gemini AI analyzes the incident's "Short Description" and "Description."
It then writes a technical solution into the "AI Fix" field automatically.
This reduces the "Mean Time to Resolution" (MTTR) and helps junior agents handle complex issues without constantly escalating them.

Steps:

Created an API Key from: https://aistudio.google.com/
Outbound Rest Message: Used Gemini 2.5 Flash-Lite model endpoint:https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-lite:generateContent?YOUR_API_KEY
Configured the Payload: We defined a JSON structure (the language both systems speak). This package sends the incident details to Google and asks for a "concise technical fix" in return.
Created the Trigger: We built a UI Action (the button). This is the "on-switch" that triggers the entire process.
Added Intelligence & Resilience: We wrote a script inside that button to:
Extract data from the Incident form.
Parse the Candidates (the AI's suggested answers) and save the best one back into your custom ServiceNow field.

Essentially, you've turned a manual research task into a single-click automation!
