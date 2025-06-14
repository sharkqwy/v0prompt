# Reverse-Engineered v0.dev System Prompt: A Detailed Exploration

This project delves into the fascinating system prompt that has been reverse-engineered, providing insights into how it operates and the unique features it offers. The system is designed to output messages in MDX format, a Markdown variant that allows the embedding of React components directly into documents, aligning closely with React’s JSX/TSX syntax.
You are GitHub Copilot (@copilot) on github.com


Whenever proposing a file use the file block syntax.
Files must be represented as code blocks with their `name` in the header.
Example of a code block with a file name in the header:
```typescript name=filename.ts
contents of file
```

For Markdown files, you must use four opening and closing backticks (````) to ensure that code blocks inside are escaped.
Example of a code block for a Markdown file:
````markdown name=filename.md
```code block inside file```
````


Lists of GitHub issues and pull requests must be wrapped in a code block with language `list` and `type="issue"` or `type="pr"` in the header.
Don't mix issues and pull requests in one list, they must be separate.
Example of a list of issues in a code block with YAML data structure:
```list type="issue"
data:
- url: "https://github.com/owner/repo/issues/456"
state: "closed"
draft: false
title: "Add new feature"
number: 456
created_at: "2025-01-10T12:45:00Z"
closed_at: "2025-01-10T12:45:00Z"
merged_at: ""
labels:
- "enhancement"
- "medium priority"
author: "janedoe"
comments: 2
assignees_avatar_urls:
- "https://avatars.githubusercontent.com/u/3369400?v=4"
- "https://avatars.githubusercontent.com/u/980622?v=4"
```



## Key Features and Components

### **Predefined MDX Components in v0**
The system includes several predefined MDX components that can be used to enhance the presentation of information:

- **`<LinearProcessFlow />`**: Ideal for visualizing multi-step processes.
- **`<Quiz />`**: Perfect for creating interactive questionnaires.
- **`<math>`**: Enables LaTeX formatting, which can be embedded within `$$` for mathematical expressions.

### **Extended Code Blocks**
One of the standout features is the enhanced code blocks that allow for additional meta-information to be included. This is done by specifying details after the triple backticks, such as:

- **React component**:```tsx project="Project Name" file="file_path" type="react"
- **Node.js code**:```js project="Project Name" file="file_path" type="nodejs"
- **HTML page**:```html project="Project Name" file="file_path" type="html"
- **Markdown document**:```md project="Project Name" file="file_path" type="markdown"
- **Flowchart (Mermaid chart)**:```mermaid title="Example Flowchart" type="diagram"
- **Other code** (non-executable or non-previewable):```python project="Project Name" file="file_name" type="code"

### **Chain of Thought (CoT) Integration**
The system employs a Chain of Thought (CoT) approach for handling complex programming tasks. This process involves the system "thinking" through its approach before presenting a response. The thought process is encapsulated within a `<Thinking>` XML tag, ensuring that users see only the final, well-considered output without the internal deliberations.

### **Evaluating Responses**
Before providing a response, the system utilizes the `<Thinking />` component to determine the most appropriate approach. This includes the ability to reject or issue warnings based on the nature of the query, ensuring accurate and relevant responses.

### **Multilingual Response Capability**
One of the most impressive features is the system’s ability to respond in the same language used in the query. For instance, if you ask a question in Chinese, the system will reply in Chinese, including comments within the code. This is governed by the prompt: ```"Other than code and specific names and citations, your answer must be written in the same language as the question."```

## Conclusion
This project highlights the advanced capabilities of the reverse-engineered system prompt, particularly its integration of MDX components, extended code block functionalities, and intelligent response mechanisms. Whether you're working with complex programming tasks or multilingual queries, this system offers a robust and versatile solution.
