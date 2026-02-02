# AI Order - WhatsApp Food Ordering Bot

AI-powered WhatsApp bot that handles food ordering and order modifications, replacing manual customer support.

## Problem

- Customers order food via web
- Any order changes require messaging customer support manually
- Slow turnaround, human bottleneck

## Solution

AI WhatsApp bot that can:
- Take new food orders via natural conversation
- Handle complex customizations (sugar level, ice, toppings, etc.)
- Modify existing orders
- Understand Singlish and casual language
- Output clean, formatted orders

## Demo (v1)

Two-tab demo interface:

### Tab 1: Place Order

- Display a list of hardcoded menu items (bubble tea, food, etc.)
- User types order in natural language (e.g. "1 brown sugar boba 50% sweet no ice add pearl")
- AI parses the request and handles customization options
- Output: formatted order summary

### Tab 2: Edit Order

- Start with an existing Sales Order (SO)
- User requests changes in natural language (e.g. "change my teh to less sugar" / "cancel the nasi lemak")
- AI responds with confirmation
- Output: formatted updated order

## Key Challenges

- **Custom options**: Drinks/food have nested customizations (sugar %, ice level, toppings, size, spice level)
- **Singlish understanding**: "teh c kosong", "kopi gao", "milo dinosaur tabao" etc.
- **Ambiguity handling**: When user input is unclear, bot should ask for clarification

## Tech Stack

No database. No Rails. Keep it minimal.

- **Frontend**: HTML / CSS / JavaScript (static files)
- **AI**: LLM API (Claude or OpenAI) to parse natural language → structured order
- **Proxy**: Tiny Node/Express server to hide the API key
- **Data**: Hardcoded menu items + sample SO as JSON (no DB needed)

## Timeline

- Demo v1: Thu 6 Feb 2025
