
# 🥚 Part 1: Dragon Hatchery 

**Mission:**  
> _The Dragon Hatchery needs you to register dragons and retrieve important information. Complete the tasks and check your results!_

---

<details>
<summary><strong>1. Create the Table</strong></summary>

- Create a table named **Dragons** with the following fields:
  - Dragon ID (integer, primary key)
  - Name (text, cannot be null)
  - Element (text)
  - Age (integer)
  - Training Level (integer)

</details>

---

<details>
<summary><strong>2. Hatch New Dragons</strong></summary>

- Insert **five** dragons of your choice into the table.
- **Important:** use the following dragons for consistency:

| Name     | Element | Age | Training Level |
|:---------|:--------|:----|:---------------|
| Pyra     | Fire    | 5   | 2              |
| Aqua     | Water   | 3   | 1              |
| Glimmer  | Light   | 7   | 4              |
| Rocky    | Earth   | 6   | 3              |
| Zephyra  | Air     | 4   | 2              |

</details>

---

<details>
<summary><strong>3. Retrieve Dragon Data</strong></summary>

Perform the following retrievals and **compare your output** with the expected results:

<details>
<summary> a) List all dragons</summary>

**Expected Output:**

| id | name    | element | age | training_level |
|:--:|:-------:|:-------:|:---:|:--------------:|
| 1  | Pyra    | Fire    | 5   | 2              |
| 2  | Aqua    | Water   | 3   | 1              |
| 3  | Glimmer | Light   | 7   | 4              |
| 4  | Rocky   | Earth   | 6   | 3              |
| 5  | Zephyra | Air     | 4   | 2              |

</details>

<details>
<summary> b) List dragons younger than 5 years old</summary>

**Expected Output:**

| id | name    | element | age | training_level |
|:--:|:-------:|:-------:|:---:|:--------------:|
| 2  | Aqua    | Water   | 3   | 1              |
| 5  | Zephyra | Air     | 4   | 2              |

</details>

<details>
<summary> c) List dragons whose element is "Fire"</summary>

**Expected Output:**

| id | name  | element | age | training_level |
|:--:|:-----:|:-------:|:---:|:--------------:|
| 1  | Pyra  | Fire    | 5   | 2              |

</details>

<details>
<summary> d) List all dragons ordered by training level DESCENDING</summary>

**Expected Output:**

| id | name    | element | age | training_level |
|:--:|:-------:|:-------:|:---:|:--------------:|
| 3  | Glimmer | Light   | 7   | 4              |
| 4  | Rocky   | Earth   | 6   | 3              |
| 1  | Pyra    | Fire    | 5   | 2              |
| 5  | Zephyra | Air     | 4   | 2              |
| 2  | Aqua    | Water   | 3   | 1              |

</details>

<details>
<summary> e) List dragons whose name starts with "Z"</summary>

**Expected Output:**

| id | name    | element | age | training_level |
|:--:|:-------:|:-------:|:---:|:--------------:|
| 5  | Zephyra | Air     | 4   | 2              |

</details>

<details>
<summary> f) Find dragons whose element is "Water" or "Earth" AND are younger than 6 years old</summary>

**Expected Output:**

| id | name    | element | age | training_level |
|:--:|:-------:|:-------:|:---:|:--------------:|
| 2  | Aqua    | Water   | 3   | 1              |

</details>

</details>

---


