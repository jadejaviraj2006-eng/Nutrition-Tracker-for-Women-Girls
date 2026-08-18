# Nutrition-Tracker-for-Women-Girls
---
A complete web platform built to evaluate female body metrics, automate personalized 30-day nutrition and workout schedules, track daily hydration and active calories, and deliver month-end progress visualizations.

---

## 📌 Core Modules

* **Health Assessment Engine:** Evaluates BMI, BMR, and TDEE adjusted for female biological factors.
* **Caloric & Macro Calculation:** Computes target daily caloric intake for fat loss, maintenance, or muscle gain.
* **Hydration Tracker:** Calculates minimum and active daily water requirements.
* **4-Week Meal Architecture:** Structured monthly meal plan template focused on essential micronutrients (Iron, Calcium, Folate, Vitamin D).
* **Weekly Workout Split:** Structured exercise programming combining resistance training, cardio, and active recovery.
* **Month-End Analytics:** Calorie deficit tracking, adherence percentage, and interactive progress graphs.

---

## 🧮 Scientific Calculations & Formulas

| Activity Level | Multiplier | Description |
| :--- | :--- | :--- |
| **Sedentary** | `1.2` | Desk job, little to no structured exercise |
| **Lightly Active** | `1.375` | 1–3 days of light workouts / walking |
| **Moderately Active** | `1.55` | 3–5 days of moderate exercise/sports |
| **Very Active** | `1.725` | 6–7 days of intense training |
| **Extremely Active** | `1.9` | Daily athletic training or physical job |

### 3. Caloric Target Strategy
* **Healthy Weight/Fat Loss:** $\text{Target} = \text{TDEE} - 350\text{ to }500\text{ kcal/day}$ *(Safe target: ~0.35–0.5 kg loss/week)*
* **Maintenance:** $\text{Target} = \text{TDEE}$
* **Muscle Gain/Lean Surplus:** $\text{Target} = \text{TDEE} + 200\text{ to }300\text{ kcal/day}$

### 4. Macronutrient Distribution (Standard Female Fat-Loss / Tone Model)
* **Protein:** $1.6\text{--}2.0\text{ g per kg of bodyweight}$ (4 kcal/g)
* **Fats:** $25\%\text{--}30\%\text{ of total daily calories}$ (9 kcal/g) — essential for female hormone regulation
* **Carbohydrates:** Remaining balance of calories (4 kcal/g)

### 5. Daily Water Intake Formula
$$\text{Baseline Water (Liters)} = \text{weight (kg)} \times 0.033$$
$$\text{Active Adjustment} = +0.35\text{ to }0.5\text{ Liters per 30 minutes of moderate-to-intense exercise}$$

---

## 🥗 4-Week Progressive Meal Architecture

| Week | Focus Phase | Meal Structure Template | Key Micronutrients |
| :--- | :--- | :--- | :--- |
| **Week 1** | Habit Baseline & High Fiber | Oats/chia bowls, lentil/chickpea salads, grilled proteins, quinoa | Magnesium, Soluble Fiber |
| **Week 2** | Micronutrient & Iron Density | Spinach/kale wraps, eggs, lean meats/tofu, citrus, pumpkin seeds | Heme & Non-Heme Iron, Vitamin C |
| **Week 3** | Anti-Inflammatory & Bone Health | Greek yogurt, cottage cheese, salmon/chia/flax, mixed berries, nuts | Calcium, Omega-3s, Vitamin D |
| **Week 4** | Sustained Energy & Recovery | Sweet potato bowls, edamame, whole grains, steamed greens, avocado | B-Complex Vitamins, Potassium |

### Daily Meal Distribution Example (1,600 kcal Target)
* **Breakfast (~400 kcal):** Rolled oats with unsweetened almond milk, 1 scoop protein/chia seeds, and fresh berries.
* **Lunch (~450 kcal):** Grilled chicken or tofu bowl with brown rice, steamed broccoli, and avocado slices.
* **Snack (~200 kcal):** Greek yogurt with a handful of walnuts or roasted chickpeas.
* **Dinner (~450 kcal):** Lentil soup/curry or baked fish with mixed greens and sweet potato.
* **Hydration Goal:** 2.5–3.0 Liters throughout the day.

---

## 🏋️‍♀️ Weekly Workout Schedule

| Day | Workout Type | Focus & Routine | Duration |
| :--- | :--- | :--- | :--- |
| **Monday** | Lower Body (Strength) | Squats, Romanian deadlifts, lunges, glute bridges | 45 min |
| **Tuesday** | Upper Body & Core | Dumbbell rows, push-ups, shoulder press, planks | 40 min |
| **Wednesday** | Low-Intensity Cardio (LISS) | Incline walking, cycling, or brisk outdoor walk | 45 min |
| **Thursday** | Full Body Circuit | Kettlebell swings, bodyweight squats, step-ups, lat pull-downs | 40 min |
| **Friday** | Core & Glutes / Mobility | Hip thrusts, Bulgarian split squats, side planks, leg raises | 35 min |
| **Saturday** | Moderate Cardio / HIIT | 20 min interval running/cycling + 15 min full-body stretching | 35 min |
| **Sunday** | Rest & Active Recovery | Light yoga, mobility drills, or casual walking | 30 min |

---

## 📈 Month-End Analytics & Improvement Metrics

### 1. Calorie Deficit vs. Weight Delta
$$\text{Expected Weight Change (kg)} = \frac{\sum (\text{Daily Target Deficit})}{\text{7700 kcal per kg of fat}}$$

### 2. Adherence Score
$$\text{Adherence \%} = \left( \frac{\text{Days Calorie \& Water Goals Met}}{30} \right) \times 100$$

### 3. Improvement KPIs Tracked
* **Body Composition:** Start vs. End Weight, Waist/Hip ratio.
* **Hydration Consistency:** Average daily liters logged vs. target.
* **Active Calorie Output:** Total workout calories burned per week.
* **Consistency Rating:** Monthly compliance badge (e.g., Bronze: 60–74%, Silver: 75–89%, Gold: 90%+).

---

## 🏗️ How I Built the Website

This section provides a complete breakdown of the development lifecycle, technical decisions, and architecture implemented to build this application.

### 1. Project Planning & Requirements
* Defined the target user journey: Onboarding Profile $\rightarrow$ Calorie/Diet Engine $\rightarrow$ Daily Loggers $\rightarrow$ Monthly Visualizations.
* Designed responsive wireframes focusing on mobile-first accessibility for quick daily tracking.

### 2. Tech Stack Selection
* **Frontend:** React.js / Next.js with Tailwind CSS for component-based modular UI and mobile responsiveness.
* **State Management:** React Context API / Redux Toolkit to manage active user stats, daily logs, and dynamic calorie calculations across components.
* **Data Visualization:** Chart.js and Recharts to render monthly dual-line trends (calories in vs. calories burned) and bar charts for macronutrient ratios.
* **Backend:** Node.js with Express.js (REST API architecture) to process user inputs, run calculations, and handle data storage.
* **Database:** MongoDB / PostgreSQL storing schemas for `Users`, `DailyLogs`, `MealTemplates`, and `WorkoutRoutines`.
* **Authentication:** JWT (JSON Web Tokens) / Firebase Auth for secure user signup, profile sessions, and data persistence.

### 3. Step-by-Step Implementation Flow
[User Input Form]
│ (Height, Weight, Age, Activity, Goal)
▼
[Calculation Logic Engine] ───► Calculates BMR, TDEE, Macros & Water Targets
│
├───► [30-Day Meal Plan Generator]
└───► [Weekly Workout Scheduler]
│
▼
[Daily Logging System] ───────► Logs Food, Workouts & Hydration
│
▼
[Analytics & Chart Engine] ───► Computes Net Deficits, Adherence % & Visual Trend



* **Step A: Core Calculation Engine:** Built modular utility functions in JavaScript/TypeScript implementing the Mifflin-St Jeor equation and hydration formulas.
* **Step B: Dynamic Diet & Workout Generator:** Created template mapping logic that matches calculated calorie goals to pre-balanced 4-week meal plans and workout splits.
* **Step C: Daily Logging Components:** Developed interactive forms allowing users to log meals (with instant macro breakdowns), log workout burn, and increment water intake via a single-tap interface.
* **Step D: Analytics Dashboard:** Integrated Recharts to aggregate 30 days of logged data, calculate net caloric balances, and render the end-of-month progress report with compliance metrics.

---

## 🚀 Getting Started

### Prerequisites
* [Node.js](https://nodejs.org/) (v16.x or higher)
* `npm` or `yarn`

### Installation & Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/your-username/Nutrition-Tracker-for-Women-Girls.git](https://github.com/your-username/Nutrition-Tracker-for-Women-Girls.git)
   cd Nutrition-Tracker-for-Women-Girls
