# cat-background-calm-score

Evaluates the background of a cat photograph for cleanliness and calm. Scores three qualities — visual quietness of the surrounding space, subject separation between the cat and its background, and distraction resistance against specific competing elements — to determine how well the background supports the cat as the clear subject.

## Input

The function accepts a single input:

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `cat_photo` | image | Yes | A photograph containing a cat. The function evaluates the background of this image, not the cat itself. |

The photograph can come from any setting, any camera, and any level of photographic skill — from professional studio portraits to casual phone snapshots. What matters is the image itself and the relationship between the cat and its surrounding visual space.

## Output

A scalar score between 0 and 1.

- **Scores near 1.0** indicate a calm, supportive background where the cat is the undeniable subject. The viewer's eye lands on the cat and stays there without effort.
- **Scores near 0.5** indicate a mixed background — neither perfectly calm nor overwhelmingly noisy. The cat reads as the subject but the background introduces some visual competition.
- **Scores near 0.0** indicate a loud, chaotic, or competitive background where the cat struggles to stand out. The viewer's attention is fractured by distracting elements, busy patterns, or poor separation between the cat and its surroundings.

## What It Evaluates

The function assesses three distinct qualities of the background in relation to the cat subject. Each quality examines a different dimension of how the background behaves, and together they form a complete picture of whether the background is helping or hurting the photograph.

### 1. Visual Quietness

The inherent character of the background itself, evaluated independently of the cat. This quality asks: how restful does the surrounding space feel?

**Scores well:**
- Muted, harmonious tones
- Gentle or absent patterns
- A settled, still energy in the background space
- Plain walls, soft blankets, simple surfaces

**Scores poorly:**
- Bright objects crowding the scene
- Bold, busy, or erratic patterns
- Competing colors and high-contrast clusters
- Dense visual information that creates a noisy, restless feel

### 2. Subject Separation

The relationship between the cat and its background — whether the cat emerges as a distinct focal point or blends into its surroundings.

**Scores well:**
- Strong contrast in tone, texture, color, or spatial depth between the cat and background
- A clear visual boundary that makes the cat the obvious focal point
- The cat commands the frame as the primary element

**Scores poorly:**
- The cat and background share similar tones, textures, or visual weight
- The cat merges into its environment rather than standing apart
- The viewer's eye has no strong reason to prioritize the cat over other elements

### 3. Distraction Resistance

Whether specific elements in the background actively compete with the cat for the viewer's attention. Unlike visual quietness (which measures overall energy), distraction resistance targets individual competitors.

**Scores well:**
- No single element rises to the level of demanding attention
- Objects remain in supporting roles, colors stay subordinate
- Light reinforces the cat as the subject
- The gaze lands on the cat and holds comfortably

**Scores poorly:**
- Bright objects, glowing screens, or bold artwork pull the eye away
- Harsh light sources or vivid color splashes compete with the cat
- The viewing experience feels fractured, with attention bouncing between the cat and its visual competitors
- Even one strong distractor can significantly lower this score

## Important Principles

- **Cleanliness is not tidiness.** A lived-in room with muted objects can score well. A pristine but visually loud space can score poorly.
- **Setting does not matter — behavior does.** A garden, kitchen, or living room can each be calm or cluttered. The function evaluates how the specific scene presents itself, not the prestige of the location.
- **Bokeh is not required.** A clean background does not need to be blurred, white, or empty. It simply needs to be calm enough that it does not compete with the cat.
- **Evaluation is relative.** A messy room where the cat is positioned against a clear section of wall can score well. A beautiful outdoor scene with overlapping foliage creating visual chaos behind the cat can score poorly.

## Use Cases

- **Content platforms** curating cat imagery can surface photos where the cat reads clearly as the subject
- **Pet adoption services** can flag listings whose photos might benefit from re-shooting against a calmer backdrop
- **Photography communities** can use it as one dimension of compositional evaluation
- **Social media tools** can help users select pet photos that will read most clearly to scrolling viewers
- **Quality filtering pipelines** can incorporate it as a signal for background cleanliness at scale