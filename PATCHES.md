# Patches
## Fixes
- List of fixes that has been applied and descrption of the issue without fix.
<table>
    <tr>
        <th>Description</th>
        <th>Description of issue</th>
    </tr>
    <tr>
        <td>3D Audio Pitch</td>
        <td>Cone Vector is not normalized and causes wrong calculation.<br>(Noticable while driving vehicle near pedestrian which is talking)</td>
    </tr>
    <tr>
        <td>Auto Player/Vehicle Tape</td>
        <td>The option doesn't save between game sessions.</td>
    <tr>
    <tr>
        <td>Character Animations</td>
        <td>Animations are clamped under 60 FPS while playing above that limit it will cause animation to speedup.</td>
    <tr>
    </tr>
        <td>Character Walk/Run Speedup</td>
        <td>This issue comes from delta time calculation which is not really the main issue, but the issue comes from multiple functions which creates fake FlowTime for valid reasons, but that also updates the character physics delta time.</td>
    <tr>
    </tr>
        <td>Culling Mode</td>
        <td>The game renders everything from front face which wouldn't be big issue if the models were properly updated for PC Version.</td>
    <tr>
    <tr>
        <td>Display Resolutions</td>
        <td>The game has list of predefined resolutions in options.</td>
    <tr>
    </tr>
        <td>Mouse Input</td>
        <td>Developers for some reason clamped input from mouse as analog stick which makes people think they're emulating joystick.</td>
    <tr>
    </tr>
    <tr>
        <td>Ocean Animation</td>
        <td>The ocean is animated with tiles that relies on frame counter and issue occurs while playing above 30 FPS.</td>
    </tr>
    <tr>
        <td>Rendering Issues</td>
        <td>The game is not playable at all without using any patches due how vertices are locked which causes them to be discarded while rendering.</td>
    </tr>
    <tr>
        <td>Shadow Color</td>
        <td>In certain areas the shadow color becomes glitched and changes color.</td>
    </tr>
    <tr>
        <td>Vehicle Glass Shader</td>
        <td>Windshield & windows didn't have any visual damage while still showing particle that the glass has been destroyed.</td>
    </tr>
    <tr>
        <td>Vehicle Object Collision</td>
        <td>While vehicle collides with other vehicle/prop or character it has applied impulse which is additionally added each frame and can cause issues where vehicle get launched to the air.</td>
    </tr>
    <tr>
        <td>Weapon Barrel Rattle (Camera Spin)</td>
        <td>After shooting from weapon the camera should with 50% return to previous angle, but there is chance that it never happens and the camera will slowly drag itself down/side.</td>
    </tr>
    <tr>
        <td>Weapon Barrel Rattle (Side Randomizer)</td>
        <td>The weapon should have randomized rattle which works fine for vertical aspect, but horizontal part is missing max value and it always gives minimum result.</td>
    </tr>
</table>

## Improvements
- List of improvements and the reason of addition/change.
<table>
    <tr>
        <th>Description</th>
        <th>Reason of addition/change</th>
    </tr>
    <tr>
        <td>Camera Blending</td>
        <td>This seems to be part where the game is supposed to be played with controller and make smooth movement while rotating around, but while using mouse it makes it feel like there is something preventing you from moving fast enough so this was fully removed.</td>
    </tr>
    <tr>
        <td>Controller Button Prompts</td>
        <td>Someone might want to play the game on controller, but the game lacks of support for controller button prompts. The patch adds them back with option to download which type of button prompts to use or create own.</td>
    </tr>
    <tr>
        <td>Controller Mapping</td>
        <td>The game has small list of controllers that it automatically maps. The patch checks for more controllers and rename them to match one of the game list and map all buttons properly.</td>
    </tr>
    <tr>
        <td>Post-Process FX</td>
        <td>This option is unused in the game. It add blur that might not be good for someone's eyes, but has additional bloom effect.</td>
    </tr>
    <tr>
        <td>Process Affinity</td>
        <td>The game by default forces process affinity to run on single core due to some threading issues. This shouldn't be big issue, but due to modern hardware/additional modules that can create multiple threads can cause performance degradation. The patch assure that only main thread of game is set to first core while others remain unaffected.</td>
    </tr>
    <tr>
        <td>Settings moved to INI file</td>
        <td>Game by default using registry for saving/loading settings which might be not appropriate in modern days.</td>
    </tr>
    <tr>
        <td>Skip License Screen/Movies</td>
        <td>Nobody wants to watch those at launch of game, right?</td>
    </tr>
    <tr>
        <td>Vehicle Shininess</td>
        <td>Bumpers don't reflect same way as on consoles.</td>
    </tr>
    <tr>
        <td>Vibrance</td>
        <td>This option is already in-game, but hardcoded. So why not have it as option.</td>
    </tr>
    <tr>
        <td>Walking with keyboard</td>
        <td>Controllers can do this by default due to analog stick and it might be useful to be able to do this even on keyboard.</td>
    </tr>
    <tr>
        <td>Windowed mode</td>
        <td>Option to set the game to launch in windowed/windowed borderless.</td>
    </tr>
    <tr>
        <td>Widescreen HUD</td>
        <td>The game HUD is kind of cramped in 4:3 resolution and having the HUD take space in view-area while playing on widescreen might look bad for some people so there is option to toggle this.</td>
    </tr>
    <tr>
        <td>Multiple performance improvements</td>
        <td>Due to decision of using v1.00.2 (ActiveMARK protected) version of game, there are bunch of left-over checks that has been removed. There are also some left-over debug code that has been removed that could cause micro-stutters and much more.</td>
    </tr>
</table>