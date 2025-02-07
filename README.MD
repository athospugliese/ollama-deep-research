# Ollama Deep Researcher

Ollama Deep Researcher is inspired by IterDRAG. This approach will decompose a query into sub-queries, retrieve documents for each one, answer the sub-query, and then build on the answer by retrieving docs for the second sub-query. Here, we do similar:

- Given a user-provided topic, use a local LLM (via Ollama) to generate a web search query.
- Uses a search engine (configured for Tavily) to find relevant sources.
- Uses LLM to summarize the findings from web search related to the user-provided research topic.
- Then, it uses the LLM to reflect on the summary, identifying knowledge gaps.
- It generates a new search query to address the knowledge gaps.
- The process repeats, with the summary being iteratively updated with new information from web search.
- It will repeat down the research rabbit hole.
- Runs for a configurable number of iterations (see configuration tab).

## Future Features

- **Multi-engine support**: Expand search capabilities to support multiple search engines beyond Tavily.
- **Enhanced query refinement**: Improve sub-query generation using advanced NLP techniques.
- **Customizable search strategies**: Allow users to define custom search strategies and parameters.
- **Source credibility assessment**: Implement methods to evaluate and rank sources based on credibility.
- **Interactive user refinement**: Allow users to guide the search refinement process interactively.
- **Multi-modal input support**: Enable research on non-text formats, such as images and videos.
- **Integration with external knowledge bases**: Connect with external databases and research repositories for richer insights.
