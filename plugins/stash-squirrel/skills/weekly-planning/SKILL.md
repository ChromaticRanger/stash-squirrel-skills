---
name: weekly-planning
description: Help a person plan their week in Stash Squirrel — lay out what's due day by day, flag overloaded days, and spread or schedule todos. Use when they ask to plan the week, see the week ahead, balance their workload, or schedule undated todos.
---

# Weekly planning

Turn a week of due dates into a plan the person believes in. Follow the conventions in the `stash-squirrel` skill (dates, time zones, confirming changes).

## 1. Gather

1. `get_account` if you haven't this session.
2. `list_items` with `view: "week"` — open items due in the next 7 days, across all lists, with events.
3. `list_items` with `view: "overdue"` — these belong in the plan too.
4. On Pro, `calendar` for the 7 days gives events (with repeats expanded) alongside dated todos — use it to see how much of each day meetings already take.
5. Ask what they want to fit in if they mention undated work: `list_items` for the relevant list with `view: "list"` and look for open todos without `due`.

Work in their time zone; ask once if you don't know it. Bucket items by **their** local day, not the UTC day.

## 2. Lay out the week

A compact day-by-day view, for example:

```
Mon 9   ●●●  Book MOT (high), Call Sam, Gym — 2 events
Tue 10  ●    Renew passport
Wed 11  ●●●●●●  ← heavy
…
```

- Count todos per day; show events separately — they're fixed.
- Flag a day as **heavy** if it has more than their capacity. Ask what that is ("How many todos is a full day for you?"); default to 5 if they don't say.
- Put overdue items at the top as "needs a day".

## 3. Propose changes

- Move lower-priority todos off heavy days to lighter ones, keeping `high` priority items where they are unless asked.
- Give overdue items a realistic day.
- Spread new or undated todos across light days.
- Keep a todo's time of day when moving it, unless the person says otherwise.

Show the proposal as a short list of moves ("Wed → Thu: Call Sam"). Get a yes (or edits), then apply with `update_item` (`due`). Don't move events with this skill unless asked.

## 4. Wrap up

The revised day-by-day view and one line on what changed.

## Don'ts

- Don't change priorities, titles or lists while planning.
- Don't move items on shared lists without saying whose list they're on — someone else may depend on that date.
- Repeating todos: moving `due` moves only this occurrence. Say so if it matters.
