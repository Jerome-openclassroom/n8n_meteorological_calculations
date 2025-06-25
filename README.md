# n8n Workflow #10 – Weather Data & AI Interpretation

## ☁️ Objective
This automated scenario in n8n:
- Retrieves weather data from Avignon via WeatherAPI
- Calculates advanced atmospheric parameters (mixing ratio `r`, equivalent potential temperature `θe`, and LCL)
- Calls GPT-4 for expert meteorological interpretation
- Sends a narrative-style email report

## 🔧 Workflow Steps

1. `Manual Trigger` — Manually launches the workflow
2. `HTTP Request` — Queries WeatherAPI for temperature, humidity, dew point, and pressure
3. `Code` — Computes:
   - Mixing ratio (`r`)
   - Equivalent potential temperature (`θe`)
   - LCL (lifting condensation level)
4. `Code1` — Formats weather data output
5. `OpenAI` — GPT-4 interprets the results with a structured prompt (Lyra-style)
6. `Edit Fields` — Extracts the generated response
7. `Gmail` — Automatically sends the weather report by email

## 🧪 Internal Prompt Sample
> Analyze the following data by evaluating:
> - Convective potential
> - Atmospheric stability
> - Presence of inversion
> - Coherence with observed sky state
> - Likely short-term trend

## 📁 File Structure (with comments)
```
data_and_screenshot/
├── My_workflow_10.json            # Native export of the n8n scenario
├── Workflow_10.txt                # Text explanation of workflow logic and JS formulas (r, θe, LCL)
└── workflow 10.jpg                # Visual screenshot of the complete n8n workflow
```

## 🛠️ Tools Used
- n8n (self-hosted or cloud)
- WeatherAPI
- OpenAI GPT-4
- Gmail (OAuth2)

## 📄 License
Educational demonstration. Freely reproducible for personal or test use.
