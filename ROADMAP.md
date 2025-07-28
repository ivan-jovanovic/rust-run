# Bouncy Adventure - Development Roadmap

## 🎮 Current Game Status
- ✅ Core bouncy character with physics (gravity, friction, variable jump height)
- ✅ 6 obstacle types (SLIDER, BOUNCER, SWEEPER, PULSER, CRAWLER, FLOATER)
- ✅ Squeeze challenges (CRAWLER + FLOATER combinations)
- ✅ Health system (3 hearts) with invincibility frames + blinking effect
- ✅ Collision detection and screen shake
- ✅ Score system and game over/restart
- ✅ Background music integration (4 steampunk tracks with random selection)
- ✅ Pause functionality (P key)
- ✅ Proper start screen (Space to start)
- ✅ Visual effects (trails, squash/stretch, obstacle animations)
- ✅ Power-ups system: Health pickup (magenta cross) and Shield (blue bubble)
- ✅ Duck mechanic (Down arrow) for enhanced obstacle avoidance
- ✅ Improved jump system (immediate jump + hold for height control)
- ✅ Sound effects system (bounce, damage, deflection, health, shield)
- ✅ Steampunk visual theme with animated background elements

## 🚀 Next Features (Prioritized)

### 1. Progressive Difficulty System 📈 (HIGH PRIORITY - IN PROGRESS)
**Goal**: Dynamic difficulty scaling + starting difficulty options

#### **Phase 1: Dynamic Difficulty Scaling** (implement first)
- [ ] **Score-based progression**: Difficulty increases as score goes up
- [ ] **Obstacle spawn rate scaling**: Starts at 2 seconds, gradually decreases to ~1 second
- [ ] **Obstacle speed scaling**: Base speeds increase by 10-20% every difficulty level
- [ ] **Difficulty level tracking**: Internal system to track current difficulty (1-10 scale)
- [ ] **Visual difficulty indicator**: UI element showing current difficulty level
- [ ] **Milestone notifications**: "DIFFICULTY INCREASED!" text effects
- [ ] **Smooth transitions**: Gradual increases every 15-20 seconds of gameplay

#### **Phase 2: Starting Difficulty Options** (implement after Phase 1)
- [ ] **Difficulty selection screen**: Easy/Medium/Hard options on start screen
- [ ] **Easy mode**: 150% spawn interval, 80% obstacle speeds, 130% power-up spawn rate
- [ ] **Medium mode**: Current balanced values (baseline)
- [ ] **Hard mode**: 70% spawn interval, 120% obstacle speeds, 70% power-up spawn rate
- [ ] **Difficulty persistence**: Remember player's last selected difficulty
- [ ] **Visual indicators**: Different UI colors/themes for each difficulty

#### **Scaling Formula Examples**:
- **Spawn Rate**: `baseInterval * (1 - (difficultyLevel * 0.08))` (max 20% faster)
- **Speed Multiplier**: `1 + (difficultyLevel * 0.02)` (max 20% faster)
- **Difficulty Increase**: Every `1800 + (currentLevel * 60)` score points

### 2. Enhanced Power-ups 🎁 (MEDIUM PRIORITY)
**Goal**: Add more strategic power-up variety
- [ ] **Slow Motion**: Everything moves at 50% speed for 5 seconds (clock icon)
- [ ] **Double Jump**: Temporary mid-air jump ability (wing icon)
- [ ] Power-up spawn balancing with difficulty system
- [ ] Visual pickup effects and UI indicators

### 3. Particle Effects ✨ (MEDIUM PRIORITY)
**Goal**: Add visual juice and feedback
- [ ] **Landing effects**: Small dust clouds on ground impact
- [ ] **Obstacle destruction**: Sparks when barely dodging obstacles
- [ ] **Enhanced damage effects**: More dramatic hit feedback
- [ ] **Trail improvements**: More dynamic particle trails

### 4. High Score System 🏆 (LOW PRIORITY)
**Goal**: Add replay value and achievement feeling
- [ ] localStorage integration for persistent high scores
- [ ] "NEW RECORD!" celebration animation
- [ ] Best score display on game over screen
- [ ] Maybe top 3 scores tracking

## 🎵 Audio Enhancements (QUICK WINS)

### 5. Sound Effects 🔊
- [ ] **Jump sound**: Satisfying "boing" when jumping
- [ ] **Hit/damage sound**: Clear feedback when taking damage  
- [ ] **Power-up pickup**: Positive collection sound
- [ ] **Obstacle dodge**: Close-call reward sound
- [ ] **Game over**: Dramatic failure sound

### 6. Enhanced Visual Feedback 💫
- [ ] **Score popup**: "+10" when dodging obstacles closely
- [ ] **Streak counter**: Consecutive dodges without getting hit
- [ ] **Screen flash effects**: For power-ups, close calls, achievements
- [ ] **Better UI animations**: Smooth health bar changes, score counting

## 🔮 Future Ideas (BRAINSTORM)
- Multiple characters with different abilities
- Different themes/backgrounds that change over time
- Combo system for chaining dodges
- Boss obstacles that require multiple hits
- Local multiplayer (split screen?)
- Different game modes (survival, time attack, etc.)

## 📝 Development Notes
- Keep the core bouncy, satisfying gameplay intact
- Each feature should add fun without overwhelming simplicity
- Test frequently to ensure performance stays smooth
- Prioritize features that give immediate visual/audio feedback

---

**Current Focus**: Implementing Progressive Difficulty System (Phase 1)
**Next Session**: Start with dynamic difficulty scaling mechanics

## 🎨 Obstacle Image Generation Prompts

### Energy/Electric Theme - Simple 2-Color Designs

#### SLIDER (Electric Barrier)
```
Create a vertical electric energy barrier for 2D game obstacle. Simple vertical rectangle with bright electric blue (#00FFFF) outer glow and pure white (#FFFFFF) inner core. Crackling electric energy effect along edges. Minimalist design, only 2 colors. Dangerous electric hazard that moves horizontally. Transparent background. 30x60 pixels. Should look like a deadly energy wall.
```

#### BOUNCER (Plasma Orb)
```
Create a plasma energy orb for 2D game obstacle. Simple circular shape with bright electric blue (#00FFFF) outer ring and glowing white (#FFFFFF) center core. Subtle pulsing energy effect. Minimalist design, only 2 colors. Dangerous energy sphere that bounces vertically. Transparent background. 50x20 pixels (oval shape). Should look like concentrated plasma energy.
```

#### SWEEPER (Lightning Rod)
```
Create a lightning energy rod for 2D game obstacle. Simple diagonal rod with bright electric yellow (#FFFF00) main body and white (#FFFFFF) crackling lightning tips. Thin, sharp, angular design. Minimalist style, only 2 colors. Dangerous electric weapon that sweeps diagonally. Transparent background. 25x80 pixels. Should look like a deadly lightning conductor.
```

#### PULSER (Energy Field)
```
Create a pulsing energy field for 2D game obstacle. Simple square/diamond shape with bright magenta (#FF00FF) outer edge and white (#FFFFFF) glowing center. Clean geometric design that suggests expansion/contraction. Minimalist style, only 2 colors. Dangerous energy zone that grows and shrinks. Transparent background. 40x40 pixels. Should look like unstable plasma field.
```

#### CRAWLER (Electric Arc)
```
Create a low electric arc for 2D game obstacle. Simple horizontal arc shape with bright electric purple (#6C5CE7) main body and white (#FFFFFF) crackling electric endpoints. Low-profile design that hugs the ground. Minimalist style, only 2 colors. Dangerous electric hazard that crawls along the ground requiring player to jump over. Transparent background. 60x25 pixels. Should look like a deadly ground-level electric barrier.
```

#### FLOATER (Plasma Cloud)
```
Create a floating plasma cloud for 2D game obstacle. Simple horizontal oval/cloud shape with bright electric cyan (#00D2D3) outer glow and white (#FFFFFF) inner plasma core. Wispy, ethereal design suggesting it floats in air. Minimalist style, only 2 colors. Dangerous plasma hazard that floats high requiring player to duck under or stay low. Transparent background. 80x30 pixels. Should look like a deadly floating energy cloud.
```