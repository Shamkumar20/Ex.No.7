# Exno.7-Develop a prompt-based application tailored to their personal needs, fostering creativity and practical problem-solving skills while leveraging the capabilities of large language models.

# Date:
# Register no: 212222073001
# Aim:
To develop a prompt-based application using ChatGPT - To demonstrate how to create a prompt-based application to organize daily tasks, showing the progression from simple to more advanced prompt designs and their corresponding outputs.

# AI Tools Required: 
ChatGPT

# Explanation: 
Prompt:
"Design a personal productivity assistant that can help manage daily tasks, schedule reminders, suggest wellness tips, and answer general queries. The assistant should interact using natural language and be adaptable to the user’s changing preferences over time."
## Procedure:
1. Define the core requirements of a personal productivity assistant.
2. Identify and construct appropriate prompts for each task using an LLM (e.g., ChatGPT).
3. Simulate natural user interaction through a simple interface or command-line system.
4. Collect feedback or inputs from users and adapt responses accordingly.
5. (Optional) Integrate basic memory to simulate preference adaptation.
## EXPECTED OUTPUT: - (attached the drive link)
Output (Example Response by LLM):
## Personal Productivity Assistant Features:
1. Daily Task Manager:
o Accept tasks via natural language (e.g., "Remind me to call mom at 6 PM").
o Organize tasks by priority and deadline.
o Provide daily summaries and pending items.
2. Smart Scheduler:
o Schedule events and set reminders using contextual understanding.
o Notify user of overlapping appointments or free time slots.
3. Wellness Tips Generator:
o Suggest daily wellness advice (hydration, exercise, screen-time breaks).
o Adapt suggestions based on past user preferences and responses.

# Counclusion:
## 1. Core Requirements & Simple Prompts
Features: Basic task management, scheduling, wellness tips, and queries. Interaction: Command-line style with natural language inputs.

## A. Daily Task Manager
Prompt Example: "Extract task, time, and priority from: '[User Input]'. Respond in JSON with keys: task, time, priority (high/medium/low)."

User Input: "Remind me to call Mom at 6 PM."

## Output:
{
  "task": "Call Mom",
  "time": "6:00 PM",
  "priority": "medium"
}

## B. Smart Scheduler
Prompt Example: "Check if '[new event time]' conflicts with existing events: [existing events]. Respond with 'Conflict: Yes/No' and a summary."

User Input: "Schedule a meeting at 3 PM tomorrow."

## Output:
{
  "Conflict": "No",
  "Summary": "The meeting at 3 PM tomorrow fits between the 2 PM team briefing and the 4 PM client call."
}

## C. Wellness Tips Generator
Prompt Example: "Suggest a wellness tip from: hydration, stretching, screen breaks. Avoid: [user disliked tips]."

## Output:
Tip: “Take a few minutes every hour to stretch your shoulders and neck to relieve tension from sitting too long.”

## 2. Intermediate: Contextual Understanding
Enhancements: Conflict detection, priority sorting, basic user preferences.

## A. Conflict Detection
Prompt Example: "User input: '[event request]'. Existing events: [list]. Identify overlaps and respond with a warning if conflicts exist."

User Input: "Add yoga class at 5 PM today."

## Output:
{
  "Conflict": "Yes",
  "Warning": "The yoga class at 5 PM overlaps with the project meeting scheduled at 4:30 PM today.",
  "Suggested_Action": "Consider rescheduling the yoga class to after 5:30 PM."
}

## B. Priority-Based Task Sorting
Prompt Example: "Sort tasks by priority (high > medium > low): [task list]. Format as a numbered list."

## Output:
1.Submit project report – high
2.Prepare for meeting – high
3.Reply to emails – medium
4.Water the plants – low

## 3. Advanced: Adaptive Memory & Natural Interaction
Enhancements:
Simulated memory for preferences, personalized responses

## A. Wellness Tips with Memory
Prompt Example: "User previously disliked 'hydration' tips. Suggest a new tip. Options: meditation, walking, ergonomics."

## Output:
Tip: “Take a short 10-minute walk outdoors to refresh your mind and boost energy levels during work breaks.”

## B. User Preference Adaptation
Simulated Memory (JSON):
{
  "preferred_tip_types": ["walking", "meditation"],
  "disliked_tip_types": ["hydration"],
  "daily_focus": "stress reduction",
  "reminder_time": "8:00 AM",
  "recent_tips": ["Take deep breaths for 5 minutes", "Stretch your arms and shoulders"]
}

## Output:
“Start your day with a 5-minute meditation to reduce stress and improve focus.”

## C.Natural Language Interaction
Prompt Example: "Respond conversationally to the user's task list request: [tasks]."

User Input: "What’s on my schedule today?"

## Output:
“You’ve got a busy day ahead! There’s a team meeting at 10 AM, lunch with Sarah at 1 PM, and don’t forget to submit your report by 5 PM.”

## 4. Optional: Feedback Loop & Interface Simulation
Feedback Collection: After each action, ask: "Was this helpful? (Yes/No)"

If "No": "Noted! I’ll adjust future suggestions."

Command-Line Simulation (Python Pseudocode):

## Python
def ai_response(user_input):
    if "schedule" in user_input:
        return "Meeting at 10 AM, report at 5 PM."
    return "Try asking about your schedule or wellness tips."

while True:
    user = input("User: ")
    if user.lower() in ["exit", "quit"]:
        break
    print("Assistant:", ai_response(user))
    fb = input("Was this helpful? (Yes/No): ")
    print("Assistant:", "Noted!" if fb.lower() == "no" else "Glad to hear that!")

## Expected Output Example
User: "Plan a blog draft and a dentist appointment at 2 PM tomorrow."

## Assistant:
{
  "tasks": [
    {
      "task": "Plan a blog draft",
      "time": "Not specified",
      "priority": "medium"
    },
    {
      "task": "Dentist appointment",
      "time": "2:00 PM tomorrow",
      "priority": "high"
    }
  ]
}

User: "What wellness tip do you recommend?"

## Assistant (Adaptive):
You might enjoy a short mindfulness session — take 5 minutes to breathe deeply and relax your shoulders. It helps reduce stress and improve focus.”


# Result: 
The lab exercise resulted in the creation of a prototype concept for a personal assistant powered by large language models. Students were able to:
- Understand how to tailor LLM prompts to real-life applications.
- Foster creativity by designing features suited to their personal or academic lives.
- Learn prompt engineering techniques for optimal interaction with AI tools.
- Experience the versatility and utility of generative AI in solving everyday problems.
