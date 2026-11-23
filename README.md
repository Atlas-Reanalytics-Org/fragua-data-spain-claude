# Fragua Data Spain

![Fragua Data Spain](assets/logo.png)

Ask Claude about Spanish real estate: market KPIs, price, rent, supply and yield trends, comparable
listings and closings, valuations, cadastre and address lookups, demographics, housing demand, student
housing, flex living and senior living for postal codes, municipalities and provinces. Data comes from
Fragua by Atlas Real Estate Analytics and is read-only.

This plugin bundles the Fragua Data Spain connector (`https://apiv2.atlas-reanalytics.com/public-mcp/mcp`) with skills that teach Claude
how to pick the right data and present the results.

## Requirements

A Fragua API account (username and password). No account yet? Write to welcome@atlas-reanalytics.com.

## Use it

1. Add the plugin, then connect **Fragua Data Spain** from the plugin's **Connectors** tab and sign in with
   your Fragua username and password.
2. Ask, for example:
   - "¿Cuáles son los principales KPIs del mercado residencial del código postal 28012?"
   - "Find residential comparables for sale in postal code 28001."
   - "How has the asking price per m² changed in 28004 over the last three years?"
   - "What are the demographic indicators for postal code 28001?"

### Claude Code

```bash
claude plugin marketplace add Atlas-Reanalytics-Org/fragua-data-spain-claude
claude plugin install fragua-data-spain@atlas-reanalytics-spain
```

Then run `/mcp`, select **fragua-data-spain** and sign in. Port `4322` must be free on your computer while
you sign in.

## Data and privacy

When Claude calls a tool, the plugin sends the places and filters of your question (for example a postal
code, an address, bedroom counts or a price range) to the Fragua Data Spain server at `https://apiv2.atlas-reanalytics.com/public-mcp/mcp`,
together with your sign-in token. Fragua records each call (your user, the tool, the request, the status
and the time) to count it against your account's monthly allowance. A valuation requested by street
address, without coordinates, sends that address to a geocoding service to locate it. Sign-in is handled
by Auth0 for Atlas Real Estate Analytics. The plugin itself stores nothing, runs no local code and sends no data
anywhere else.

Documentation and troubleshooting: https://fragua-ai-plugins.atlas-reanalytics.com/claude

Privacy policy: https://atlas-reanalytics.com/fragua/politica-de-privacidad/
Terms of service: https://atlas-reanalytics.com/fragua/terminos-y-condiciones/

## Support

welcome@atlas-reanalytics.com - https://fragua-ai-plugins.atlas-reanalytics.com/es/support
