
# 🐉 Part 3: Dragon Mastery

**Mission:**  
> _"Dragons have advanced in their training! Expand their profiles, track detailed skill records, and master the Academy's new data systems!"_

---

<details>
<summary><strong>1. Expand the Dragons Table (ALTER TABLE)</strong></summary>

Tasks:
- Add a `color` column (TEXT) to the Dragons table.
- Add a `behavior` column (TEXT) to the Dragons table.

---

📋 **Expected Dragons Table Structure After ALTER TABLE:**

| Column          | Type    |
|:----------------|:--------|
| id              | INTEGER |
| name            | TEXT    |
| element         | TEXT    |
| age             | INTEGER |
| training_level  | INTEGER |
| color           | TEXT    |
| behavior        | TEXT    |

</details>

---

<details>
<summary><strong>2. Update Dragons with Color and Behavior (UPDATE)</strong></summary>

Tasks:
- Assign a color and behavior for each dragon:

| Name    | Color    | Behavior  |
|:--------|:---------|:----------|
| Pyra    | Crimson  | Aggressive |
| Glimmer | White    | Wise       |
| Rocky   | Brown    | Stoic      |
| Zephyra | Silver   | Energetic  |

(Note: Aqua was deleted in Part 2.)

---

📋 **Expected Full Dragons Table After Updates:**

| id | name    | element  | age | training_level | color   | behavior  |
|:--:|:-------:|:--------:|:---:|:--------------:|:-------:|:---------:|
| 1  | Pyra    | Fire     | 5   | 4              | Crimson | Aggressive |
| 3  | Glimmer | Starlight| 7   | 4              | White   | Wise       |
| 4  | Rocky   | Earth    | 6   | 3              | Brown   | Stoic      |
| 5  | Zephyra | Air      | 4   | 3              | Silver  | Energetic  |

</details>

---

<details>
<summary><strong>3. Create the Training_Records Table (CREATE TABLE)</strong></summary>

Tasks:
- Create a new table `Training_Records` with the following fields:
  - record_id (INTEGER, PRIMARY KEY)
  - dragon_id (INTEGER, FOREIGN KEY to Dragons.id)
  - flying_points (INTEGER)
  - elemental_points (INTEGER)
  - endurance_points (INTEGER)

---

📋 **Expected Empty Training_Records Table Structure:**

| Column           | Type    |
|:-----------------|:--------|
| record_id        | INTEGER |
| dragon_id        | INTEGER |
| flying_points    | INTEGER |
| elemental_points | INTEGER |
| endurance_points | INTEGER |

</details>

---

<details>
<summary><strong>4. Insert Initial Training Records (INSERT INTO)</strong></summary>

Tasks:
- Insert the following training points for each dragon:

| Dragon Name | Flying Points | Elemental Points | Endurance Points |
|:------------|:--------------|:-----------------|:-----------------|
| Pyra        | 70             | 85               | 60               |
| Glimmer     | 90             | 80               | 70               |
| Rocky       | 60             | 65               | 85               |
| Zephyra     | 85             | 70               | 55               |

---

📋 **Expected Full Training_Records Table After Inserts:**

| record_id | dragon_id | flying_points | elemental_points | endurance_points |
|:---------:|:---------:|:-------------:|:----------------:|:----------------:|
| 1         | 1         | 70            | 85               | 60               |
| 2         | 3         | 90            | 80               | 70               |
| 3         | 4         | 60            | 65               | 85               |
| 4         | 5         | 85            | 70               | 55               |

</details>

---

<details>
<summary><strong>5. Improve Dragon Endurance (UPDATE)</strong></summary>

Tasks:
- Boost **endurance_points** by **+10** for all dragons after a tough tournament.

---

📋 **Expected Full Training_Records Table After Endurance Update:**

| record_id | dragon_id | flying_points | elemental_points | endurance_points |
|:---------:|:---------:|:-------------:|:----------------:|:----------------:|
| 1         | 1         | 70            | 85               | 70               |
| 2         | 3         | 90            | 80               | 80               |
| 3         | 4         | 60            | 65               | 95               |
| 4         | 5         | 85            | 70               | 65               |

</details>

---

<details>
<summary><strong>6. Training Review (SELECT with JOIN)</strong></summary>

Tasks:
- List dragons' **name**, **color**, **behavior**, and **flying_points**.
- List dragons with **flying_points > 80**, ordered by **flying_points descending**.
- (Bonus) Calculate average flying points **grouped by behavior**.

---

📋 **Expected Output for JOIN (Dragon Info + Flying Points):**

| name    | color   | behavior  | flying_points |
|:-------:|:-------:|:---------:|:-------------:|
| Pyra    | Crimson | Aggressive | 70            |
| Glimmer | White   | Wise       | 90            |
| Rocky   | Brown   | Stoic      | 60            |
| Zephyra | Silver  | Energetic  | 85            |

---

📋 **Expected Output for Dragons with flying_points > 80:**

| name    | flying_points |
|:-------:|:-------------:|
| Glimmer | 90            |
| Zephyra | 85            |

---

📋 **Expected Output for Average Flying Points Grouped by Behavior:**

| behavior  | avg_flying_points |
|:---------:|:-----------------:|
| Aggressive| 70                |
| Wise      | 90                |
| Stoic     | 60                |
| Energetic | 85                |

</details>


