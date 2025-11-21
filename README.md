# 🏀 HoopScout: LLM-Powered NBA Pre-Game Scouting Report Generator

HoopScout is an automated pre-game scouting report generator built with a Large Language Model (LLM) multi-agent architecture.
It processes real NBA player statistics, identifies patterns, assigns badges, and outputs structured, coach-friendly scouting reports to support strategic decision-making.

This system was developed for ECE1786 — Creative Applications of Natural Language Processing, University of Toronto.

# Example Generated Pre-Game Scouting Report
<div style="text-align:">
  <span style="font-size: 32px; font-weight: bold;">Pre-Game Scouting Report</span>
</div>

<img src="https://drive.google.com/uc?export=view&id=1yRtJeQX8iZCs8dv7m9KvJDYQWgp_v32I" 
     alt="Portrait" width="520" height="380" 
     style="border: 1px solid #ddd; border-radius: 5px; padding: 5px;">

<div margin: 20px 0;>
  <img src="https://upload.wikimedia.org/wikipedia/commons/0/09/Jumpshot.png" alt="Jump Shot Badge" width="92" height="104" style="margin: 0 5px;">
</div>

<div>
  <span style="font-size: 32px; font-weight: bold;">Austin Reaves</span><br>
  <span style="font-size: 24px;">Los Angeles Lakers | #15 | Guard</span>
</div>

<div style="margin: 30px 0;">
  <table style="width: 100%; border-collapse: collapse; text-align: center;">
    <thead style="background-color">
      <tr>
        <th style="padding: 10px; border: 1px solid #ddd;">PPG</th>
        <th style="padding: 10px; border: 1px solid #ddd;">RPG</th>
        <th style="padding: 10px; border: 1px solid #ddd;">APG</th>
        <th style="padding: 10px; border: 1px solid #ddd;">SPG</th>
        <th style="padding: 10px; border: 1px solid #ddd;">BPG</th>
        <th style="padding: 10px; border: 1px solid #ddd;">FG%</th>
        <th style="padding: 10px; border: 1px solid #ddd;">3P%</th>
        <th style="padding: 10px; border: 1px solid #ddd;">FT%</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td style="padding: 10px; border: 1px solid #ddd;">17.44</td>
        <td style="padding: 10px; border: 1px solid #ddd;">3.56</td>
        <td style="padding: 10px; border: 1px solid #ddd;">5.31</td>
        <td style="padding: 10px; border: 1px solid #ddd;">1.12</td>
        <td style="padding: 10px; border: 1px solid #ddd;">0.25</td>
        <td style="padding: 10px; border: 1px solid #ddd;">44.23%</td>
        <td style="padding: 10px; border: 1px solid #ddd;">35.21%</td>
        <td style="padding: 10px; border: 1px solid #ddd;">62.63%</td>
      </tr>
    </tbody>
  </table>
</div>

<h2>Overview:</h2>
Austin Reaves provides scoring and playmaking for the Lakers as a guard. Recently, his performance has been inconsistent, particularly in shooting and free throws. He plays a significant role due to his synergy with key teammates.
<hr>

<h2>Key Strengths:</h2>
<ul>
  <li>Proficient in mid-range and pull-up shooting.</li>
  <li>Solid playmaker with over 5 assists per game.</li>
  <li>Effective in defense against long-range shots.</li>
</ul>
<hr>

<h2>Key Weaknesses:</h2>
<ul>
  <li>Inconsistent free-throw percentage (62.63%).</li>
  <li>Moderate three-point shooting (35.21%) with fluctuations.</li>
  <li>Struggles with interior defense and shot-blocking.</li>
</ul>
<hr>

<h2>Offensive Strategy:</h2>
<ul>
  <li>Encourage perimeter shots due to vulnerability beyond 15 feet.</li>
  <li>Utilize pick-and-roll to exploit mismatches.</li>
</ul>
<hr>

<h2>Defensive Strategy:</h2>
<ul>
  <li>Pressure on perimeter shooting to limit effectiveness.</li>
  <li>Force him to the free-throw line to exploit his weakness.</li>
</ul>

# Features
## 🔹 Multi-Agent LLM Architecture
HoopScout uses specialized LLM agents:

Data-Analyzing Agent — Extracts patterns, strengths, weaknesses, and tendencies from raw data.

Badge-Matching Agent — Assigns up to six skill badges (e.g., Catch & Shoot, Rim Protection) using numerical thresholds.

Report Generation Agent — Combines insights + badges into a structured scouting report.

Team-Level Agent — Summaries team performance trends and produces high-level reports.

## 🔹 Real NBA Data Integration

Per-player dataset includes:

* Shooting stats

* Advanced box scores

* Passing stats

* Dribble breakdown

* Defensive tracking

* Player profile JSON

* Player portrait

The system also supports team-level data, including roster CSVs and team logos.

## 🔹 Gradio Web UI

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

