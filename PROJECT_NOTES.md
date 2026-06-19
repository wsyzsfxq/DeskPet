# DeskPet Project Notes

Setting and product-vision documents now live under `docs/设定集/`.

## Product Direction

DeskPet is a desktop pet first, with AI companion features later.

The project began from the idea of a mysterious personal pet, but its current direction is clearer: a desktop-resident companion. The pet should be able to exist on the user's real desktop even when all game-like UI is hidden.

Core experience:

- The pet can live directly on the desktop without requiring a large game window.
- The pet's nest, furniture, care UI, settings, and inventory can be hidden.
- A single action can bring the hidden UI back.
- The pet can interact with furniture and decorations inside its nest.
- The user can interact with the pet through mouse clicks and desktop gestures.
- Future desktop-awareness features must be user-controlled with a clear on/off switch.

## Current Product Understanding

DeskPet is best understood as:

> A desktop-resident pet and lightweight AI companion. The user can hide the pet's nest and UI, leaving only the pet active on the desktop. The pet can move, idle, react to clicks, interact with furniture, and eventually understand the user's desktop context with explicit permission.

This is different from a normal pet-raising game. The main scene is not a room inside a game client. The main scene is the user's actual desktop.

The important feeling is: the user is not visiting the pet; the pet is living alongside the user.

## Core Pillars

### 1. Desktop Presence

The pet should be able to stay on top of or around the desktop without feeling like a full application window.

Expected behaviors:

- Walk, idle, sleep, sit, look around, or follow nearby activity.
- Stay visible while the user works in other apps.
- Avoid blocking important work by default.
- Support quick hide, show, and focus behavior.

### 2. Hidden UI, One-Action Return

The pet's UI should be summonable rather than always present.

UI that can be hidden:

- Nest/home area.
- Furniture and decoration editing.
- Feeding and care panels.
- Status, mood, health, and settings.
- Inventory or shop-like systems.

The user should be able to collapse everything back down to "only the pet" quickly.

### 3. Nest And Furniture Interaction

The nest is not only decoration. It should be an interactive living space.

Possible interactions:

- The pet sleeps in its bed or nest.
- The pet climbs, hides, plays, scratches, or rests on furniture.
- Furniture affects idle animations, mood, routines, or available behaviors.
- Decorations can create personality and make each user's pet feel local to their desktop.

### 4. Direct Mouse Interaction

The user should be able to interact with the pet through the mouse without opening a large UI.

Possible interactions:

- Click to get attention.
- Double-click or long-press for affection/play.
- Drag nearby objects or toys.
- Pet reaction to cursor movement.
- Pet reaction to repeated poking, ignoring, hovering, or gentle interaction.

### 5. Optional Desktop Awareness

Later versions may allow the pet to "see" or understand the user's desktop.

This must be opt-in and easy to disable.

Possible awareness:

- Recognize that the user is writing, drawing, coding, watching videos, gaming, or in a meeting.
- React to long working sessions, late-night usage, window switching, or idle time.
- Offer quiet companionship, small reminders, or assistant-like responses.

Design rule: desktop awareness should make the pet feel considerate and alive, not surveillant.

### 6. AI Companion, Not Just Chatbot

AI should primarily be expressed through the pet's behavior, timing, memory, and small reactions.

The pet may eventually talk, but the core interface should remain:

- Movement.
- Expression.
- Animation.
- Short contextual reactions.
- Relationship memory.
- Optional assistant actions.

The product should avoid becoming "a chatbot with a pet skin."

## World And Naming Notes

Chinese name is still undecided.

Previous naming discussion:

- "DeskPet" is the simple English project codename.
- "余生物" was discussed as a possible Chinese creative direction for the creature concept.
- The emotional direction behind "余生物" is that the pet is a small overlooked life that exists in the gaps of ordinary life.

This worldbuilding can remain useful, but the product form is now desktop-first.

Potential concept sentence:

> It does not live in a game window. It lives on your desktop.

## Interaction Priorities

Early prototype should prove:

- Transparent or shaped desktop pet window.
- Always-on-top behavior.
- Click-through or input routing modes.
- Hide/reveal UI shell.
- Basic pet animation states.
- Direct mouse interaction.
- Simple nest UI that can be shown and hidden.

Later prototype should explore:

- Furniture interaction.
- Behavior scheduling and idle life.
- Mood and care loops.
- Desktop context permission model.
- Local-first desktop awareness experiments.
- AI memory and companion behavior.

## Early Questions

- Desktop framework: Tauri, Electron, Unity, Godot, or native Windows.
- Rendering style: Live2D, Spine, frame animation, 2D skeletal animation, or 3D.
- AI scope: local behavior rules first, cloud model later, or hybrid.
- Privacy model for desktop-awareness: opt-in, scoped capture, local-first processing.

## Technical Notes To Decide Later

- Whether the pet should be implemented as a transparent always-on-top window.
- Whether the UI shell should be a separate window, an expandable overlay, or a tray-controlled panel.
- Whether the pet and nest are rendered by the same process or separate surfaces.
- How to handle click-through modes so the pet can both interact and stay out of the way.
- How to store pet memory, behavior state, and user preferences locally.
- How to design desktop-awareness permissions in a way users can understand immediately.
