# Search Experience & Decision Flow

## Student Programme Discovery

The search experience was designed to allow students to begin with the information they know, rather than forcing them to complete every search field.

```mermaid
flowchart TD
    A[Student starts search] --> B{Search criteria entered?}

    B -->|No| C[Show available options]
    B -->|Yes| D[Validate selected criteria]

    D --> E{Valid criteria?}

    E -->|No| F[Show validation message]
    E -->|Yes| G[Retrieve matching results]

    G --> H{Results found?}

    H -->|No| I[Show no results message]
    H -->|Yes| J[Display matching schools and programmes]

    J --> K[Student selects result]
    K --> L[View school or programme details]
    L --> M{Suitable opportunity?}

    M -->|No| A
    M -->|Yes| N[Start application]
