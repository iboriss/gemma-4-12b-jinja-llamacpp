# gemma-4-12b-jinja-llamacpp

Jinja2 template for Gemma 4 12B model. Fixes larger context errors in LMStudio/llama.cpp & enables thinking.

**License**: [Apache 2.0](https://ai.google.dev/gemma/docs/gemma_4_license) | **Authors**: [Google DeepMind](https://deepmind.google/models/gemma/) | **Jinja modification**: [Unsloth](https://huggingface.co/unsloth/gemma-4-12b-it)

## Changes made to Unsloth Jinja

1. Changed `is sequence` checks to `is iterable`. Prevents crashes when handling large context and multimodal inputs.
2. Hardcoded `enable_thinking = true` at the top to enable reasoning, because `<|think|>` token doesn't work in lmstudio. Change to `false` to turn off reasoning.

