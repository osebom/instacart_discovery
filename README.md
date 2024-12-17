# Recipe Recommendations with Semantic Search and LLMs

This project demonstrates how to **generate meal prep recipes** and **enhance ingredient discovery** using **Cohere's LLMs** and a semantic search approach inspired by [Instacart's "Supercharging Discovery in Search with LLMs"](https://tech.instacart.com/supercharging-discovery-in-search-with-llms-556c585d4720).

---

## Overview

The script fetches and processes recipes in a JSON-like format, performs **semantic search** to enrich recipe ingredients, and outputs a **structured DataFrame**. This enables accurate and context-aware ingredient suggestions for recipes.

### Key Components:
1. **Cohere's Chat API**: Generates recipes and contextual outputs based on user queries.
2. **Semantic Search**: Matches each ingredient using embeddings for enhanced discovery.
3. **Pandas DataFrame Output**: Recipes are displayed in a clean, tabular format with:
   - `Recipe Name`: The name of the recipe.
   - `Reason`: The rationale behind the recipe suggestion.
   - `Ingredients`: A formatted list of relevant ingredients (single-quoted and comma-separated).

---

## Inspiration

The project takes inspiration from **Instacart's approach** to supercharging discovery in search. Their method leverages **LLMs** for enriching search results and providing a more intuitive user experience. By combining **semantic search** and **contextual relevance**, this project mimics that concept for meal planning and ingredient discovery.

Read the article: [Supercharging Discovery in Search with LLMs](https://tech.instacart.com/supercharging-discovery-in-search-with-llms-556c585d4720).

---

## How It Works

1. **User Query**: Input a keyword or query (e.g., "Hoisin Sauce").
2. **Recipe Generation**: The Cohere Chat API generates a JSON output with:
   - Substitutes, complementary ingredients, and recipe suggestions.
3. **Semantic Search**:
   - Ingredients in each recipe are matched using a semantic search function.
   - This ensures high-quality and context-aware ingredient suggestions.
4. **Formatted Output**:
   - Results are displayed in a `pandas` DataFrame with formatted columns.

---

## Example Output

Sample DataFrame:

| **Recipe Name**                  | **Reason**                                                                                       | **Ingredients**                                                                |
|----------------------------------|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| Hoisin Glazed Pork and Rice Bowls | A simple yet flavorful bowl that showcases the versatility of Hoisin sauce as a glaze.          | `['Pork Tenderloin', 'Hoisin Sauce', 'Brown Rice', 'Bok Choy', 'Spring Onions']` |
| Beef and Broccoli Stir-Fry       | A classic Asian stir-fry that's easy to make and freezes well. The oyster sauce adds depth.      | `['Beef Sirloin', 'Broccoli Florets', 'Garlic', 'Ginger', 'Oyster Sauce']`      |

<img width="680" alt="image" src="https://github.com/user-attachments/assets/1c83b9f3-9afd-4c38-9a92-653d7fa3f6d3" />

---

## Dependencies

- Python 3.8+
- Cohere API Key
- Libraries:
  - `cohere`
  - `pandas`
  - `numpy`
  - `sklearn` (for `cosine_similarity`)
  - `sentence-transformers` (or equivalent for embeddings)


