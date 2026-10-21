# FitCoach – a simple fitness AI agent

FitCoach is a small rule-based AI agent that builds a personalised weekly workout plan and calorie/protein targets, then adjusts the plan based on user feedback. It runs entirely in the browser (one `index.html` file), so it needs no server and no API key.

**Live demo:** https://YOUR_USERNAME.github.io/fitcoach/

## What it does

1. Asks about your goal, fitness level, equipment, training days, age, sex, weight, height and activity level.
2. Calculates daily calories and protein.
3. Builds a weekly workout plan.
4. Lets you log how training went (too easy, too hard, skipped, pain) and adjusts the plan.
5. Remembers your profile and check-ins between visits.

## Why it is an agent

| Agent part | How FitCoach does it |
|---|---|
| Goal | Help the user reach their fitness goal |
| Tools | `calculateTDEE`, `generateWorkoutPlan`, `adjustPlan`, `save`/`load` |
| Memory | Profile and feedback log saved in the browser's `localStorage` |
| Feedback loop | Plan, act, get feedback, adapt the plan |
| Guardrails | General fitness info only. Pain feedback tells the user to see a professional |

The calorie estimate uses the Mifflin-St Jeor equation. Protein targets are 1.4-1.8 g per kg of body weight depending on the goal.

## Run it locally

Download the files and open `index.html` in any browser.

## Publish with GitHub Pages

1. Create a new public repository on GitHub.
2. Upload `index.html`, `README.md` and `LICENSE`.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then click **Save**.
5. After about a minute your site is live at `https://YOUR_USERNAME.github.io/REPO_NAME/`.

## Limitations

- Rule-based, not a large language model. Plans come from templates.
- Calorie and protein numbers are estimates.
- Not medical advice. See a doctor or qualified trainer if you have an injury or health condition.

## License

MIT License. See the [LICENSE](LICENSE) file.
