# Scoring Setup Guide

## Fix for Scoring Issues

The scoring wasn't working because the method names changed. Here's how to fix it:

### Step 1: Configure Scoring Zones
1. **Select each scoring zone** in your scene
2. **In the Inspector**, find the ScoringZone component
3. **Set the "Is Left Zone" checkbox**:
   - **Left scoring zone** (on the left side of the screen): Check "Is Left Zone"
   - **Right scoring zone** (on the right side of the screen): Uncheck "Is Left Zone"

### Step 2: Verify GameManager References
1. **Select your GameManager object**
2. **In the Inspector**, make sure these are assigned:
   - **Left Player Paddle**: Your left paddle (with PlayerPaddle script)
   - **Right Player Paddle**: Your right paddle (with RightPlayerPaddle script)
   - **Left Player Score Text**: Your left player score UI text
   - **Right Player Score Text**: Your right player score UI text

### Step 3: Test the Scoring
1. **Play the game**
2. **Let the ball hit a scoring zone**
3. **The score should update** and the ball should reset

## How Scoring Works Now:

- **Ball hits left zone** → Right player scores
- **Ball hits right zone** → Left player scores
- **Score updates** and ball resets to center

## Troubleshooting:

### If scoring still doesn't work:
1. **Check the Console** for any error messages
2. **Make sure the scoring zones have colliders** and are set as triggers
3. **Verify the ball has a Rigidbody2D** and collider
4. **Check that the GameManager references** are properly assigned

### If you see errors about missing methods:
- The script has been updated to call the correct methods automatically
- Make sure you're using the latest version of the ScoringZone script

## Quick Test:
1. Play the game
2. Let the ball hit either side
3. You should see the score change and the ball reset to the center
4. The game should pause when you press P

The scoring should now work correctly with the updated method names!
