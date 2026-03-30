# Agenda

A minimal, mobile-first daily schedule app designed to live on your iPhone home screen as a web clip. No accounts, no subscriptions, no app store — just a single HTML file served from anywhere.

---

## What It Does

Agenda gives you a structured daily schedule across three day types — **Weekday**, **Saturday**, and **Sunday** — each with its own curated set of time blocks. The philosophy is simple: protect your personal hours, do deep work in long uninterrupted sessions, and ship something real every day.

---

## Features

### 📋 Schedule View
- Three day modes: **Weekday**, **Saturday**, and **Sunday**, each with a distinct block structure
- Time blocks are color-coded by category: Work, Creative, Building, Learning, Fitness, Adventure, Research, and more
- Each block shows its start/end time, duration, category label, and an italic description
- Blocks are automatically marked as **upcoming**, **current** (with a glowing dot), or **done** (dimmed) based on the current time
- A **day progress bar** at the top shows how far through the day you are

### ✅ Tasks
- Each focusable block supports inline task checklists
- Default tasks are pre-populated on relevant blocks (e.g. "Drink water" on the morning block)
- Add your own tasks with the **+ add task** button — they persist across sessions
- Tasks can be checked off and are saved locally

### 📝 Block Notes
- Any focusable block supports a **progress note** — a freeform italic annotation saved per block
- Notes persist across sessions and can be edited or deleted inline

### ⏱ Focus Mode
- Tap any focusable block to enter **Focus Mode** — a fullscreen overlay showing the block title, description, and a live timer
- Start, pause, and resume the timer as you work
- A mantra at the bottom: *"Phone face-down. You know what to do."*

### ✏️ Edit Mode
- Tap **Edit** in the schedule header to enter edit mode
- In edit mode, each block's **start and end times become editable inputs** — type any time format (`7am`, `7:30am`, `19:30`) and tap away to commit
- Editing a block's time **auto-adjusts subsequent overlapping blocks** to preserve the schedule's integrity
- Drag the **≡ handle** on any block to **swap it** with another block's time slot — the timeline always stays sorted chronologically

### ✦ Wins
- Log accomplishments with a type (Finished, Shipped, Learned, Showed Up, PR/Record, Other), an optional category, an optional linked block, and an optional note
- Wins are shown as a filterable list: **All**, **Today**, or **This week**
- Each win can be edited or deleted inline
- A badge on the nav shows how many wins you've logged today

### ◎ Stats
- Breakdown of personal (non-work) hours in the current day mode
- Count of focusable blocks and total wins
- **Category balance chart** showing how your time is distributed across Creative, Building, Learning, Fitness, Adventure, Research, and Rest

### 📅 Week View
- A compact 7-column grid showing the week at a glance
- Each day's blocks are represented as color-coded pips
- Today's column is highlighted

---

## Day Structures

| Mode | Character | Blocks |
|------|-----------|--------|
| **Weekday** | Work hard, then make something | Morning routine → Deep work → Workout → Lunch → Afternoon work → Clock-out → Creative → Building → Dinner → Learning → Wind down |
| **Saturday** | Adventure first, create after | Morning ease → Adventure block → Lunch → Creative session → Research → Building → Free evening |
| **Sunday** | No obligations, long sessions | Morning routine → Long workout → Deep work project → Lunch → Deep learning → Research → Creative work → Week prep → Wind down |

---

## Tech

- **Single HTML file** — no build step, no dependencies, no framework
- **localStorage** for all persistence (tasks, notes, wins, custom times)
- Works as a **PWA web clip** on iOS (Add to Home Screen)
- Fully offline once loaded
- Dark theme only

---

## Setup

1. Clone or download the repo
2. Serve the HTML file with any static web server, e.g.:
   ```bash
   python3 -m http.server 8080
   ```
3. Open the URL in Safari on your iPhone
4. Tap **Share → Add to Home Screen** to install as a web clip

No configuration needed. The app auto-detects the current day of the week on load.

---

## Data & Privacy

All data lives exclusively in your browser's `localStorage` under the key prefix `ag7_`. Nothing is sent anywhere. Clearing your browser data will erase your tasks, notes, and wins.

---

## Version

Current version: **ag7**
