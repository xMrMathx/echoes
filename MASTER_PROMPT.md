# MASTER PROMPT: Echoes (verbatim, user-issued 2026-10-06)

## 1. Core Concept & Vision
- Game Title: Echoes
- Genre: Premium Over-the-Shoulder 3D Tactical 5v5 Multiplayer Shooter
- Platform: Web-based (WebGPU / High-end WebGL 2.0 / WASM engine)
- Visual Target: "Ultra-Premium / Web-AAA" — High-fidelity lighting, PBR materials, post-processing (bloom, ambient occlusion, motion blur), and smooth 60+ FPS performance directly in modern desktop browsers.

## 2. Game Loop & Objective (Round-Based PvP)
- Match Structure: 5v5 team match split into dynamic rounds.
- Phase 1: Mid-Core Control
  - Both teams fight for control of a neutral Mid-Core located at the map's center.
  - To capture, a team must hold the Mid-Core uncontested until a 1-minute capture timer completes.
- Phase 2: Base Core Assault
  - Once the Mid-Core is captured and secured by Team A, Team B's Main Base Core becomes vulnerable.
  - Team A pushes into the enemy base to destroy the Main Core to win the round.

## 3. Mechanics: The Echo System
- Each player brings an AI companion into battle called an Echo.
- Spawning: Every player starts the round with an Echo active.
- Summoning/Repositioning: Pressing a dedicated Echo button triggers a rapid visual animation — a bright pulse/flash radiating out of the player's body — deploying or repositioning the Echo.
- Loadouts: Players customize separate loadouts for themselves and their Echo prior to match start (weapons, defensive capabilities, passive enhancements).
- Echo AI Modes (Tactical Command Wheel / Hotkeys):
  - Seek: Pursues and engages the nearest detected enemy players.
  - Cover: Follows the player closely, engaging enemies that attack or threaten the player.
  - Guard Point: Holds a player-selected waypoint on the map, providing vision and defensive fire.
  - Free Roam (Autonomous): Uses adaptive utility AI to evaluate game state, automatically helping team objectives, capturing points, or supporting low-health teammates.

## 4. Camera, Controls & Feel
- Camera: Dynamic tight over-the-shoulder perspective with smooth camera transitions during sprint, aim-down-sights (ADS), and stance shifts.
- Movement: Responsive tactical movement (sprinting, sliding, vaulting, ducking behind cover).
- Gunplay: Punchy recoil patterns, hit-scan or fast-projectile ballistics with clear hit markers and spatial audio feedback.

## 5. Technical Architecture & Performance Requirements
- Engine/Framework: High-performance web engine target (e.g., Unreal Engine Pixel Streaming / PlayCanvas / Babylon.js / Three.js + WebGPU).
- Networking: Low-latency authoritative server architecture (WebSockets / WebRTC) with client-side prediction, entity interpolation, and lag compensation for smooth 5v5 + 10-entity combat.
- Optimization: Dynamic LODs, GPU-driven particle effects for the Echo flash animation, spatial audio management, and occlusion culling to preserve high frame rates on web browsers.
