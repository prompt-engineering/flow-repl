# FlowRepl

[![CI](https://github.com/prompt-engineering/flow-repl/actions/workflows/ci.yaml/badge.svg)](https://github.com/prompt-engineering/flow-repl/actions/workflows/ci.yaml)

> FlowRepl is an interactive REPL tool that enables users to easily run code generated by LLMs and interact with it in real-time.

we are currently working on poc of FlowRepl, which will be released soon. will update this README.md when it is ready.

Plan support languages:

- [x] Kotlin
- [ ] Java
- [ ] Python
- [ ] JavaScript

## Development

1. git clone `https://github.com/prompt-engineering/flow-repl`
2. `./gradlew bootRun`

API:

### Websocket

server: `ws://localhost:8080/repl`

input: 

```kotlin
@Serializable
data class InterpreterRequest(
    var id: Int = -1,
    val code: String
)
```

output: 

```kotlin
@Serializable
data class Message(
    var id: Int = -1,
    var resultValue: String,
    var className: String = "",
    var msgType: MessageType = MessageType.NONE,
    var content: MessageContent? = null,
)
```


## LICENSE

This code is distributed under the MIT license. See [LICENSE](./LICENSE) in this directory.
