# Can AI help deliver social benefits, or only make things worse?

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rafeekpro/ai-social-benefits-demo/blob/main/ai_social_benefits_demo.ipynb)

Companion notebook to my article on poverty in Spain and AI.

**Important: the simulation uses synthetic data.** It illustrates mechanisms. It does not measure Spain or any real administration.

## What is inside

`ai_social_benefits_demo.ipynb` (already executed, charts included):

1. **Real public figures** that show the delivery gap: AROPE 2025 (Eurostat), unexpected expenses (INE), non-take-up of the Ingreso Minimo Vital and the child supplement (AIReF, July 2025).
2. **Experiment A:** using a model to find eligible households that never applied. Compares random outreach, a simple income rule and a model.
3. **Experiment B:** a risk model trained on a biased audit history (the Dutch childcare benefit mechanism). Shows that removing the sensitive column is not enough and that training on a random audit sample restores parity.

## Assumptions to keep in mind

- 60,000 synthetic households, calibrated so that about 55% of eligible households do not apply (as in the AIReF headline).
- The share of contacted households that go on to apply (60%) is an assumption, not an empirical finding.
- In a real deployment a person decides, and the affected household can ask for an explanation and appeal.

## Run it

```bash
pip install -r requirements.txt
jupyter notebook ai_social_benefits_demo.ipynb
```

Random seeds are fixed, so the numbers are reproducible.

## Sources

- Eurostat: https://ec.europa.eu/eurostat/en/web/products-eurostat-news/w/ddn-20260430-1
- INE: https://www.ine.es/dyngs/Prensa/ECV2025.htm
- AIReF (via El Salto): https://www.elsaltodiario.com/renta-basica/55percent-hogares-podrian-recibir-imv-no-lo-han-solicitado-segun-airef
- Amnesty International on the Dutch scandal: https://www.amnesty.org/en/latest/news/2021/10/xenophobic-machines-dutch-child-benefit-scandal/
- EU AI Act, Annex III: https://artificialintelligenceact.eu/annex/3/

## Licence

MIT.
