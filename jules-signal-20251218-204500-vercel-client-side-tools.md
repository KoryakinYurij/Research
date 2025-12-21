# Context
Vercel AI SDK 3.2 Release (June 2024)

# Observation
The Vercel AI SDK introduced client-side tool execution, allowing agentic workflows to run tools directly in the browser. The `useChat` hook, combined with `streamText`, now supports an `onToolCall` handler. This enables the definition of tools that are executed on the client, including tools that require user interaction (e.g., rendering a confirmation dialog).

# Reason
This feature was introduced to support the development of more interactive and responsive AI applications. By executing tools on the client, developers can reduce server roundtrips for tasks that don't require server-side resources. It also enables agents to directly interact with the user and the DOM, which is essential for building generative UI.

# Implication
This marks a significant architectural shift towards hybrid server-client agents. While the LLM orchestration might still be managed by the server, the execution of certain tools is delegated to the client. This pattern is particularly powerful for applications that require dynamic user interaction within an agentic workflow, as it allows for a tighter integration between the agent and the user interface.

# Sources
- [Introducing Vercel AI SDK 3.2](https://vercel.com/blog/introducing-vercel-ai-sdk-3-2)
- [Vercel AI SDK `useChat` hook documentation](https://ai-sdk.dev/docs/reference/ai-sdk-ui/use-chat)
