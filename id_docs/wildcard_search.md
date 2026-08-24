# Search - General and Wildcard

The Search function is available throughout the ID application.

Searches in Intelligent Design use Fuzzy Search and its accompanying algorithms, Similarity Scoring, Phonetic Matching, and Contextual Relevance helping to ensure that imperfect input can render accurate and comprehensive results. In addition, search now includes a wildcard option to further refine searches. The wildcard character **%** can be used within a search string to match any character that occupies the same position within a search string. Searches can contain multiple wildcard **%**characters in the search string.

**Note:** See [Tables](id_ug_tables_container.md) to learn more about general searching.

How the wildcard search works. A user wants to search for three parameters named **Param\_1\_A**, **Param\_2\_A**, and **Param\_2\_B**. User enters a search string **Param\_%\_A** Search results include **Param\_1\_A** and **Param\_2\_A** but not **Param\_1\_B**.

How wildcard search works for multiple wildcard characters. A user wants to search for **part1\_subpart2\_subsubpart3**. User enters the following search criteria **part%\_subpart%\_subsubpart3**. Search results return the search string that matches any numbers after part and subpart, but only ones where the subsubpart is 3.

**Parent topic:**[Application elements](../id_docs/id_navigation.md)

