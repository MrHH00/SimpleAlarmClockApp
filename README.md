# Simple Alarm Clock App

- Student Id: 22110028

- Student name: Nguyễn Mai Huy Hoàng

# Functional Requirements

## User Interface (UI):
- A simple layout with:
  - A button to set an alarm.
  - A time picker (or input field) for the user to select the alarm time.
  - **Optional:** A text display showing the selected alarm time.
- Minimal design suitable for student practice (e.g., no complex styling).

## Alarm Setting Functionality:
- The app should allow the user to select a time for the alarm.
- Use an implicit intent to delegate the alarm-setting task to the device's default clock or alarm app (e.g., `ACTION_SET_ALARM`).
- Pass the selected time (hour and minute) to the intent.

## Intent Handling:
- The app must create an implicit intent with the action `android.intent.action.SET_ALARM`.
- Include extras in the intent:
  - `EXTRA_HOUR`: The hour of the alarm (0-23).
  - `EXTRA_MINUTES`: The minutes of the alarm (0-59).
  - **Optional:** `EXTRA_MESSAGE` (e.g., "Wake up for class!") for the alarm label.
- Handle cases where no app can respond to the intent (e.g., display a toast message like "No alarm app available").

## Feedback:
- After the intent is fired, show a confirmation message (e.g., a `Toast`) indicating that the alarm has been requested.

---

# Non-Functional Requirements

## Platform:
- Target Android API level 21 (Lollipop) or higher for broad compatibility.
- Use **Java** or **Kotlin** (student’s choice, though **Kotlin** is recommended for modern Android development).

## Permissions:
- No special permissions are required since the implicit intent relies on the system's clock app.

## Simplicity:
- Keep the code minimal and well-commented for educational purposes.
- Avoid complex features like recurring alarms or custom notifications to focus on implicit intent practice.

## Error Handling:
- Gracefully handle cases where the device lacks an app to handle the `ACTION_SET_ALARM` intent.

---

# Technical Requirements

## Dependencies:
- Android SDK with basic libraries (e.g., `androidx.appcompat` for UI compatibility).
- No external libraries needed beyond the Android framework.

## Key Components:
- **Activity**: A single `MainActivity` to host the UI and logic.
- **TimePicker** or **EditText**: To let the user input the alarm time.
- **Button**: To trigger the implicit intent.
- **Intent**: Use `Intent.ACTION_SET_ALARM` with appropriate extras.

