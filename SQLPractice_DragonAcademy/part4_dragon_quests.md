
# 🐉 Part 4: Dragon Quests & Glory 

**Mission:**  
> _"Dragons are now sent on legendary quests! Track their journeys, record successes, and identify the true heroes of the Academy!"_

---

<details>
<summary><strong>1. Create the Quests Table (CREATE TABLE)</strong></summary>

Tasks:
- Create a table called `Quests` with the following fields:
  - quest_id (INTEGER PRIMARY KEY)
  - dragon_id (INTEGER, FOREIGN KEY to Dragons.id)
  - quest_name (TEXT)
  - success (BOOLEAN)

---

📋 **Expected Empty Quests Table Structure:**

| Column     | Type    |
|:-----------|:--------|
| quest_id   | INTEGER |
| dragon_id  | INTEGER |
| quest_name | TEXT    |
| success    | BOOLEAN |

</details>

---

<details>
<summary><strong>2. Insert Quests (INSERT INTO)</strong></summary>

Tasks:
- Insert the following quests:

| Dragon Name | Quest Name                   | Success |
|:------------|:------------------------------|:--------|
| Pyra        | Defend Fire Mountain           | 1 |
| Glimmer     | Illuminate the Dark Caves      | 1 |
| Rocky       | Endure the Earthquake Trials   | 0 |
| Zephyra     | Ride the Storm Winds           | 1 |
| Pyra        | Challenge the Volcano King     | 0 |

---

📋 **Expected Full Quests Table After Inserts:**

| quest_id | dragon_id | quest_name                   | success |
|:--------:|:---------:|:-----------------------------:|:-------:|
| 1        | 1         | Defend Fire Mountain          | 1       |
| 2        | 3         | Illuminate the Dark Caves     | 1       |
| 3        | 4         | Endure the Earthquake Trials  | 0       |
| 4        | 5         | Ride the Storm Winds          | 1       |
| 5        | 1         | Challenge the Volcano King    | 0       |

</details>

---

<details>
<summary><strong>3. Update Quest Results (UPDATE)</strong></summary>

Tasks:
- After a surprise comeback, update Pyra's "Challenge the Volcano King" quest to success (set success = 1).

---

📋 **Expected Full Quests Table After Update:**

| quest_id | dragon_id | quest_name                   | success |
|:--------:|:---------:|:-----------------------------:|:-------:|
| 1        | 1         | Defend Fire Mountain          | 1       |
| 2        | 3         | Illuminate the Dark Caves     | 1       |
| 3        | 4         | Endure the Earthquake Trials  | 0       |
| 4        | 5         | Ride the Storm Winds          | 1       |
| 5        | 1         | Challenge the Volcano King    | 1       |

</details>

---

<details>
<summary><strong>4. Join Dragon and Quest Data (SELECT with JOIN)</strong></summary>

Tasks:
- Show dragons' **name**, **color**, **behavior**, **quest name**, and **success status**.

---

📋 **Expected Output:**

| name    | color   | behavior  | quest_name                   | success |
|:-------:|:-------:|:---------:|:-----------------------------:|:-------:|
| Pyra    | Crimson | Aggressive| Defend Fire Mountain          | 1       |
| Glimmer | White   | Wise      | Illuminate the Dark Caves     | 1       |
| Rocky   | Brown   | Stoic     | Endure the Earthquake Trials  | 0       |
| Zephyra | Silver  | Energetic | Ride the Storm Winds          | 1       |
| Pyra    | Crimson | Aggressive| Challenge the Volcano King    | 1       |

</details>

---

<details>
<summary><strong>5. Analyze Quest Results (SELECT, GROUP BY)</strong></summary>

Tasks:
- List dragons who completed at least one successful quest.
- Find the dragon(s) with the most successful quests.
- (Bonus) Calculate % success rate per dragon.

---

📋 **Expected Key Outputs:**

➤ Dragons who completed at least one successful quest:

| name    |
|:-------:|
| Pyra    |
| Glimmer |
| Zephyra |

---

➤ Dragon(s) with most successful quests:

| name    | successful_quests |
|:-------:|:-----------------:|
| Pyra    | 2                 |

---

➤ Bonus: Success rate per dragon (example %):

| name    | success_rate |
|:-------:|:------------:|
| Pyra    | 100%         |
| Glimmer | 100%         |
| Rocky   | 0%           |
| Zephyra | 100%         |

</details>

---

<details>
<summary><strong>6. Create a Top Dragons View (CREATE VIEW)</strong></summary>

Tasks:
- Create a view called `Top_Dragons` that includes dragons who completed more than one successful quest.

---

📋 **Expected Output When Viewing Top_Dragons:**

| name    | successful_quests |
|:-------:|:-----------------:|
| Pyra    | 2                 |

</details>


