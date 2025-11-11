---
title: Home Automation | Automations
---
I run a range of automations at home, built around openHAB, HomeKit, and a mix of sensors, cameras, and smart devices. These aren’t just “nice to have” tricks; they solve real problems, increase safety, and reduce hassle.

## Security Modes

My security automation is built around presence detection.

- Everyone in the house uses an iPhone, and with an Apple TV acting as a hub, I track when each family member arrives or leaves.
- When the last person leaves, Security Away mode is activated automatically.
  - If any doors or windows are left open, a push notification is sent.
  - If a door or motion sensor is triggered while in Away mode, alerts are sent to our devices.
- When someone arrives home, the system deactivates Away mode automatically.
- There is also a manual Stay mode:
  - Only perimeter and door sensors are active.
  - Indoor motion sensors do not trigger notifications, so the house can be occupied without constant alerts.

## Smoke Alarms

Smart smoke alarms are fully integrated into the system:

- If smoke is detected, notifications are sent immediately.
- At night, all lights turn on automatically when an alarm is triggered.
- The alarms can be silenced via HomeKit or the openHAB app.
  - I also have a HomeKit scene to silence alarms added to Control Center on my Apple Watch for quick access.
- Every Sunday at 2 PM, all smoke alarms perform a self-test.
  - If one or more do not respond, a housewide notification and push alert lets us know there’s an issue.

## Water Leak Detection

Water leak sensors are installed anywhere there is a water source.

- If a leak is detected, a housewide alert and push notification are triggered immediately.
- This has been especially useful around appliances like the washing machine, where early detection can prevent damage.

## AI-Assisted Vision

Some of my automations handle less obvious but very practical scenarios:

- If:
  - The grass needs mowing, or
  - Clothes are still on the line, or
  - Garden tools (like the lawnmower or weed wacker) are left outside,
- Then:
  - A housewide and push notification is sent as a reminder.

To achieve this, TAPO cameras regularly send images to an OpenAI-compatible endpoint. AI vision is used with custom prompts to determine what’s in the scene and whether action is needed. This allows automation based on visual cues that traditional sensors can’t easily provide.

## Camera-Based Detection

TAPO cameras also include built-in AI event detection:

- They can distinguish between motion, people, pets, and vehicles.
- I subscribe to these events using ONVIF and feed them into openHAB.

Previously, I used outdoor motion sensors that triggered audio alerts at night (for example, an announcement like “ding ding, backyard” when motion was detected). This was genuinely useful: one night, it alerted me to someone walking through our property.

However, traditional motion sensors outdoors tend to generate many false alarms from insects, weather, and temperature shifts. With TAPO’s AI-based detection and event hooks:

- I can trigger alerts based on more specific conditions (such as “person detected”).
- False positives are significantly reduced, while still maintaining awareness and security.

These automations are an ongoing project, always evolving as I find new ways to make the home smarter, safer, and more aware of what’s actually happening in and around it.
