Learning Note of SMACSS (Scalable and Modular Architecture for CSS)
====================================================================

## SMACSS is
  - Categorization
  - Naming Convention
  - Decoupling CSS from HTML
  - State-based Design (How to build a webpage)

#### Categorization
  - Base (Recommend no css resets or normalize)
    - Element Selectors
    - CSS Resets
    - Normalize
  - Layout
    - Major containing elements
    - Grid Systems
    - How do you group your content
  - Module
    - Contain content
    - Are the majority of your site
    - Each module is an interface that your users have to learn
    - Each module is code that has to be written, delivered and maintained
    - Isolate modules from each other
    - Prevent styles from coming in or out
  - State
    - Changing (Maybe a module or layout)
    - Like a module variation(sub-module) but indicate a JavaScript dependency
  - Themes
    - Only for on-the-fly style changes
    - Usually aren't needed
      - Preprocessors can help
  - Every style we wrote should serve on of these above purposes whether we're aware of it or not
  - Isolating code allows for easier reuse, testing and debugging
  - Categorizing reveals patterns; easier to identify when things break the pattern

#### Naming Convention
  - There are only two hard things in Computer Science: cache invalidation and naming things
  - Base: Just selectors
  - Layout: layout-content. layout-header, layout-something
  - Use Class over ID
    - Specificity is dangerous



















