# notes for the notifier

## notification types
(postMessage type is always "gm_notification" or "gm_notification_popup")

Theres gonna be different types of notifications, multiple importance ranks.

1. Important
  ID: 0
  Use Cases:
    - Shutdown warnings
  Displayed to: global
  Additional: Will **ALWAYS** be displayed. Not usable on Popup notifications

2. Announcement
  ID: 1
  Use Cases:
    - Event announcements
  Displayed to: global

3. Info
  ID: 2
  Use Cases:
    - Something finished, for successes use success type though
  Displayed to: single players

4. Success
  ID: 3
  Use Cases:
    - If the player succeeds in something, such as the driving school
  Displayed to: single players

5. Failure
  ID: 4
  Use Cases:
    - Player fucked something up
  Displayed to: single players

6. Warning
  ID: 5
  Use Cases:
    - Something is happening that isnt supposed to be like it is
    - For code problems or wrong use of things by players that could cause problems
    - reserved for script internals, not for excessive use by server staff
  Displayed to: Whoever it happens to

7. Error
  ID: 6
  Use Cases:
    - Something went wrong in a script
    - reserved for script internals, not for excessive use by server staff