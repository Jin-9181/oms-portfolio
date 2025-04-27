# 📅 Understanding `datetime.date` and `datetime.time` Dot Notation in Python

This guide explains how to use dot notation to access individual parts of `datetime.date` and `datetime.time` objects in Python, followed by a practical example.

---

## ✅ Concept Overview

In Python, the `datetime` module allows you to work with dates and times.

### 🟦 `datetime.date` Components:
You can access:
- `start_date.year` → Year (e.g., 2024)
- `start_date.month` → Month (1–12)
- `start_date.day` → Day of the month (1–31)

### 🟨 `datetime.time` Components:
You can access:
- `start_time.hour` → Hour (0–23, 24-hour format)
- `start_time.minute` → Minute (0–59)
- `start_time.second` → Second (0–59)

These attributes allow you to compare or manipulate individual parts of a date/time.

---

## 🧪 Example Problem

> "Given `start_date`, `end_date`, `start_time`, and `end_time`, check if the **start moment happens before the end moment** on the same day using dot notation."

### ✅ Example Code:

```python
import datetime

start_date = datetime.date(2017, 2, 16)
end_date = datetime.date(2017, 2, 16)
start_time = datetime.time(4, 30, 0)
end_time = datetime.time(4, 30, 17)

# Compare year/month/day to confirm same day
same_day = (
    start_date.year == end_date.year and
    start_date.month == end_date.month and
    start_date.day == end_date.day
)

# Compare time components in order
time_earlier = (
    start_time.hour < end_time.hour or
    (start_time.hour == end_time.hour and start_time.minute < end_time.minute) or
    (start_time.hour == end_time.hour and start_time.minute == end_time.minute and start_time.second < end_time.second)
)

# Final result
if same_day and time_earlier:
    print("Start is earlier than end on the same day")
else:
    print("Not earlier")
```

---

## 🧠 Summary

| Object Type | Attribute | Example | Description |
|-------------|-----------|---------|-------------|
| `datetime.date` | `.year` | `start_date.year` | Year (e.g. 2024) |
| 〃 | `.month` | `start_date.month` | Month (1–12) |
| 〃 | `.day` | `start_date.day` | Day of the month |
| `datetime.time` | `.hour` | `start_time.hour` | Hour (0–23) |
| 〃 | `.minute` | `start_time.minute` | Minute (0–59) |
| 〃 | `.second` | `start_time.second` | Second (0–59) |

---

> Use dot notation to precisely access and compare parts of a date or time in Python.
