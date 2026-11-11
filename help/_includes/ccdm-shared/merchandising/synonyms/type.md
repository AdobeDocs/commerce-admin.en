# Types of Synonyms

One- and two-way synonyms expand the definition of keywords. Some are interchangeable with the keyword, while others represent a subset of the keyword.

## Two-way

Two-way synonyms have the same meaning and return the same search results. In the following example, the first word shown in bold is the keyword that is used in the catalog, followed by words that have the same meaning as the original keyword. You can create a simple pair of two-way synonyms, or a chain of multiple two-way synonyms for the same keyword.

**jacket** ![Two-way selector](/help/assets/ccdm-shared/synonyms/two-way.png) coat
**pants** ![Two-way selector](/help/assets/ccdm-shared/synonyms/two-way.png) slacks ![Two-way selector](/help/assets/ccdm-shared/synonyms/two-way.png) trousers

## One-way

A one-way synonym is a subset of a keyword, but with a more specific meaning. For example, capris and shorts are pants, but not all pants are capris or shorts. A search for pants includes capris and shorts. However, a search for shorts does not return capris.

**sweatshirt** ![One-way selector](/help/assets/ccdm-shared/synonyms/one-way.png) hoodie
**pants** ![One-way selector](/help/assets/ccdm-shared/synonyms/one-way.png) capris ![One-way selector](/help/assets/ccdm-shared/synonyms/one-way.png) calf-length-pants ![One-way selector](/help/assets/ccdm-shared/synonyms/one-way.png) peddle pushers

## Multi-word synonym behavior

For multi-word synonyms, the system considers the synonym as a phrase. For example, if you create a two-way synonym **dining room table** ![Two-way selector](/help/assets/ccdm-shared/synonyms/two-way.png) **kitchen table** ![Two-way selector](/help/assets/ccdm-shared/synonyms/two-way.png) **dining table**, then the system searches across all fields set to searchable for the occurrence of **dining room table** or **kitchen table** or **dining table**.

If no synonym is created and a shopper searches for **kitchen table**, the system looks for the terms anywhere in the searchable fields, even across different fields, for example **table** in the name field and **kitchen** in the meta keyword.

After creating a synonym, the search behavior changes to look for the exact phrase **kitchen table**. This might reduce the number of results because only products with the exact phrase will be shown.

If you want the terms to be searched separately as before, you can [create a support ticket](https://experienceleague.adobe.com/en/docs/support-resources/adobe-support-tools-guide/adobe-commerce-support/adobe-commerce-help-center-user-guide).
