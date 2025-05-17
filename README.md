# n8n Workflow #10 – Météo et Interprétation IA

## ☁️ Objectif
Ce scénario automatisé dans n8n :
- Récupère les données météo d’Avignon via WeatherAPI
- Calcule des paramètres atmosphériques avancés (r, θe, LCL)
- Interroge GPT-4 pour une analyse météo experte
- Envoie le bilan par mail avec un style clair et narratif

## 🔧 Étapes du workflow

1. `Manual Trigger` — Exécution à la demande
2. `HTTP Request` — Requête vers WeatherAPI pour température, humidité, rosée, pression
3. `Code` — Calculs JS :
   - Rapport de mélange (r)
   - Température potentielle équivalente (θe)
   - LCL (niveau de condensation)
4. `Code1` — Mise en forme des données météo
5. `OpenAI` — Interprétation GPT-4 avec prompt structuré (style Lyra)
6. `Edit Fields` — Extraction du message généré
7. `Gmail` — Envoi automatique du mail météo

## 🧪 Exemple de prompt (interne)
> Analyse ces données en évaluant :
> - Le potentiel convectif
> - La stabilité atmosphérique
> - La présence possible d'une inversion
> - La cohérence avec l'observation
> - Une tendance possible à court terme

## 📁 Fichiers inclus
- `My_workflow_10.json` — export natif du workflow n8n
- `Workflow_10.txt` — explication fonctionnelle et code commenté
- `README.md` — ce fichier

## 🛠️ Outils
- n8n (self-hosted ou cloud)
- WeatherAPI
- OpenAI GPT-4
- Gmail OAuth2

## 📄 Licence
Démonstration pédagogique. Reproductible librement à usage personnel ou de test.
