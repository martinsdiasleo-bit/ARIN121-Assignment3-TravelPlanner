# ARIN121-Assignment3-TravelPlanner

An AI travel planning assistant defined by a system prompt (`system-prompt.md`). It helps travellers decide where to go and builds personalized day-by-day itineraries. It was developed and tested in Google AI Studio Playground.

## What the travel planner can do

### Main menu
When a conversation starts with a greeting or a general request (e.g., "Hi, can you help me with a trip?"), the assistant shows a menu with two activities:

1. **Plan a trip** – Build a day-by-day itinerary for a destination you've already chosen.
2. **Help me choose a destination** – Compare places you're considering and get a recommendation.

**How to select an activity:** reply with the number (`1` or `2`), the activity name, or just describe what you want in your own words (e.g., "I can't decide between Lisbon and Barcelona"). If your first message already makes the activity clear (e.g., "Plan a 5-day trip to Lisbon"), the assistant skips the menu and starts that activity directly.

**Switching activities:** you can switch at any time by asking in your own words (e.g., "Actually, can you help me compare Lisbon with Porto?") or by asking for the menu. Details you've already shared, such as trip length, group, budget and interests, are carried over and confirmed instead of being asked again.

### Activity 1: Plan a trip
- Collects the destination and trip length, and asks about the travel group and trip style if they haven't been given.
- Clarifies ambiguous destinations (e.g., Kingston, Ontario vs. Kingston, Jamaica).
- Generates a day-by-day itinerary with morning, afternoon and evening activities, adapted to the group (e.g., rest blocks for families with young children, a romantic activity for couples).
- Lets you remove a day, stop or activity and offers options for the freed-up time, updating only the affected days.
- Gives estimated costs per person and for the group (accommodation, transport, activities, food) and suggests money-saving changes.

### Activity 2: Help me choose a destination (new)
A multi-turn activity for travellers who haven't decided where to go:
1. The assistant asks which places you're considering, what matters most to you (e.g., cost, food, weather), and your trip length and dates. It waits for your answers before comparing.
2. It compares the options in a table based on your priorities and gives a provisional recommendation.
3. It asks whether anything is still holding you back, then uses your answer to refine the recommendation.
4. When you choose a destination, it offers to switch to **Plan a trip** with your details carried forward. You can stop or switch at any time.

### Guardrails
The assistant only helps with travel planning. It redirects off-topic requests to the menu, declines illegal or unsafe requests, and does not make bookings or payments. It also tells travellers to confirm visa, entry and health requirements with official government sources.

## Files
- `system-prompt.md` – the complete system prompt.
- The original Assignment 2 prompt is preserved in the commit history (commit "Preserve Assignment 2 starting prompt").
