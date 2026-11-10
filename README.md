# Genesys Experience Unit Calculator

A single-page web tool that estimates how many **Genesys Experience Units** (also called tokens; 1 Experience Unit = 1 token) a customer will need each month, and what they will cost.

## Using it

Open `index.html` in a browser (or host it with any static web server such as GitHub Pages). No build step is required.

1. **Voice Mix**: add each voice interaction type with its call length (m:ss), calls per month, % automated and the AI you plan to use (Voice Bot, Virtual Agent or Agentic AI).
2. **Digital Mix**: add each digital interaction type with its average number of turns, interactions per month, % automated and AI (Digital Bot, Virtual Agent or Agentic AI).
3. **Configuration**: set the price per Experience Unit for Bot, VA (Virtual Agent), AVA (Agentic AI) and other capabilities, and turn on any additional capabilities (Copilot, Predictive Engagement, Predictive Routing, Supervisor Copilot, Virtual Supervisor Copilot).
4. Read the totals at the top. Switch **Distribution** between *Selected* (the AI you chose for each interaction) and *Lowest Cost* (the cheapest option per interaction). **Unused Capacity** shows what has been paid for but not consumed.

The per-interaction comparison charts show the cost of each AI option side by side.

See `Genesys Experience Unit Calculator User Guide.pdf` for the full guide.

## Notes

- Light and dark themes follow your system setting; use the toggle in the header to override it.
- Tailwind CSS, Chart.js and the Inter font are loaded from public CDNs.

## Versioning

The app uses semantic versioning. The version is shown in the header and footer and is set by `APP_VERSION` in `index.html`. See [CHANGELOG.md](CHANGELOG.md) for release history and the rules for bumping it.
