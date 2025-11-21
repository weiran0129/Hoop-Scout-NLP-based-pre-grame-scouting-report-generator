# HoopScout

# 🏀 HoopScout: LLM-Powered NBA Pre-Game Scouting Report Generator

HoopScout is an automated pre-game scouting report generator built with a Large Language Model (LLM) multi-agent architecture.
It processes real NBA player statistics, identifies patterns, assigns badges, and outputs structured, coach-friendly scouting reports to support strategic decision-making.

This system was developed for ECE1786 — Creative Applications of Natural Language Processing, University of Toronto.

# Features
🔹 Multi-Agent LLM Architecture

HoopScout uses specialized LLM agents:

Data-Analyzing Agent — Extracts patterns, strengths, weaknesses, and tendencies from raw data.

Badge-Matching Agent — Assigns up to six skill badges (e.g., Catch & Shoot, Rim Protection) using numerical thresholds.

Report Generation Agent — Combines insights + badges into a structured scouting report.

Team-Level Agent — Summaries team performance trends and produces high-level reports.

🔹 Real NBA Data Integration

Per-player dataset includes:

Shooting stats

Advanced box scores

Passing stats

Dribble breakdown

Defensive tracking

Player profile JSON

Player portrait

The system also supports team-level data, including roster CSVs and team logos.

🔹 Gradio Web UI

A clean, user-friendly interface for:

Uploading player stats

Running analysis

Viewing auto-generated reports

# 🧠 System Architecture

The system follows a multi-agent workflow:

User uploads player profile + advanced stats

Data-Analyzing Agent extracts patterns

Badge-Matching Agent matches badge rules

Report Agent produces final structured scouting report

Output displayed in Gradio UI


# 📊 Quantitative Performance

Using a rubric including readability, badge accuracy, strategic depth, and structure:

Zero-shot prompting: ~72.4 average score

One-shot prompting: ~88.2 average score (significant improvement)

Readability: Successfully achieved Flesch-Kincaid Grade 9–11

Badge matching: Lower accuracy due to numerical reasoning limits of LLMs

