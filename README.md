# ha-occupancy-echo-groups
Set an Echo Group based on a Room's Occupancy - Home Assistant Blueprint

<h3>Platform:</h3>
Home Assistant

<h3>Who is this blueprint for?</h3>

This blueprint is for anyone that has Amazon echo devices and only wants to programmatically play Announcements, TTS messages, and sounds on those devices in which the room is occupied.

<h3>What does this blueprint do?</h3>

The blueprint will create a new entity group with a name that is based on your ‘Room Name’ input. This group will be named ‘group.room_name_occupancy_echos’.

This new group will then be updated each time your selected Occupancy Sensor’s state changes. The contents of the new group will either contain all of your selected ‘Echo Devices’ when the occupancy sensor is ‘On’ or it will be empty when the occupancy sensor is ‘Off’. You can then use this group in other automations to play echo announcements, tts messages, or sounds only when that room is occupied.

For example, you may simply replace your echo device entity with this new group entity in any automation you are running those services. But wait, there’s more…

<h3>Unleash the Power:</h3>

The true power of this blueprint comes after you have created all of your room occupancy echo groups; where you can then create your own group (NOT using this blueprint) that contains the entities of all the echo groups you have created. You might assign this very powerful group a name ‘All Rooms Occupancy Echos’. This new ‘All Rooms Occupancy Echo Group’ will allow you to play Announcments, TTS messages, and sounds on any echo device in your entire house, but only in those rooms that are currently occupied. No longer will you hear six different devices ‘echoing’ (no pun intended) throughout your house from rooms that aren’t occupied.

The ‘All Rooms Occupancy Echos’ group is the only group I personally use in my Amazon echo announcements.

<h3>Prerequisites:</h3>

Must have Amazon echo device entities exposed, via the alexa media player integration for example.

Must have a single sensor, switch, or input_boolean setup per room that contains an echo device which will signal when that room is occupied. There are numerous ways to accomplish this. You could technically use a single motion sensor, but keep in mind most motion sensors time-out (or return to an ‘off’ status) in less than 30 seconds, which is typically too short of time to accurately reflect the correct occupancy status of a room in most scenarios.
