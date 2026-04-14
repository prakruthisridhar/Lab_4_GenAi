{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "c5fe0cde-d1f7-4dd8-992b-54ca53ddb563",
   "metadata": {},
   "source": [
    "## prompting_Lab4.ipynb\n",
    "\n",
    "### Programmatically input prompts, compare results from different models\n",
    "\n",
    "\"Practice Chain of thought, Tabular format, fill in the blank, RGC, zero shot, one shot and few shots prompting\".  modify the code to use different models available in Hugging face. Compare the results."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "dab5a4ec-c92a-4118-b5d8-2cfacd19566b",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Starting prompting techniques comparison\n",
      "Models: 5\n",
      "Techniques: 7\n",
      "Questions: 3\n",
      "Time limit: 30 minutes\n",
      "--------------------------------------------------\n",
      "\n",
      "Question 1: Explain the concept of neural networks...\n",
      "\n",
      "Model: gpt2\n",
      "  Testing zero_shot on gpt2...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "/home/haris/python/gen_ai/venv312/lib/python3.12/site-packages/transformers/tokenization_utils_base.py:1617: FutureWarning: `clean_up_tokenization_spaces` was not set. It will be set to `True` by default. This behavior will be deprecated in transformers v4.45, and will be then set to `False` by default. For more details check this issue: https://github.com/huggingface/transformers/issues/31884\n",
      "  warnings.warn(\n",
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ zero_shot: 9.53s\n",
      "  Testing one_shot on gpt2...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ one_shot: 6.09s\n",
      "  Testing few_shot on gpt2...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ few_shot: 5.63s\n",
      "  Testing chain_of_thought on gpt2...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ chain_of_thought: 6.81s\n",
      "  Testing tabular_format on gpt2...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ tabular_format: 7.03s\n",
      "  Testing fill_in_blank on gpt2...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ fill_in_blank: 8.04s\n",
      "  Testing rgc_prompting on gpt2...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ rgc_prompting: 6.36s\n",
      "\n",
      "Model: DialoGPT-small\n",
      "  Testing zero_shot on DialoGPT-small...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ zero_shot: 0.17s\n",
      "  Testing one_shot on DialoGPT-small...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ one_shot: 0.25s\n",
      "  Testing few_shot on DialoGPT-small...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ few_shot: 0.38s\n",
      "  Testing chain_of_thought on DialoGPT-small...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ chain_of_thought: 1.05s\n",
      "  Testing tabular_format on DialoGPT-small...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ tabular_format: 0.62s\n",
      "  Testing fill_in_blank on DialoGPT-small...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ fill_in_blank: 0.49s\n",
      "  Testing rgc_prompting on DialoGPT-small...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ rgc_prompting: 1.16s\n",
      "\n",
      "Model: distilgpt2\n",
      "  Testing zero_shot on distilgpt2...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ zero_shot: 5.82s\n",
      "  Testing one_shot on distilgpt2...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ one_shot: 4.05s\n",
      "  Testing few_shot on distilgpt2...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ few_shot: 4.03s\n",
      "  Testing chain_of_thought on distilgpt2...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ chain_of_thought: 4.52s\n",
      "  Testing tabular_format on distilgpt2...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ tabular_format: 4.68s\n",
      "  Testing fill_in_blank on distilgpt2...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ fill_in_blank: 6.42s\n",
      "  Testing rgc_prompting on distilgpt2...\n"
     ]
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "Truncation was not explicitly activated but `max_length` is provided a specific value, please use `truncation=True` to explicitly truncate examples to max length. Defaulting to 'longest_first' truncation strategy. If you encode pairs of sequences (GLUE-style) with the tokenizer you can select this strategy more precisely by providing a specific strategy to `truncation`.\n"
     ]
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ rgc_prompting: 10.59s\n",
      "\n",
      "Model: bart-large-mnli\n",
      "  Testing zero_shot on bart-large-mnli...\n"
     ]
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "ed725818c865421d8cb820ab48e5b339",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "config.json: 0.00B [00:00, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "261f806dd911471aad635b8b76114aa8",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "model.safetensors:   0%|          | 0.00/1.63G [00:00<?, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "name": "stderr",
     "output_type": "stream",
     "text": [
      "'(ProtocolError('Connection aborted.', RemoteDisconnected('Remote end closed connection without response')), '(Request ID: 5ed22c50-5d54-4dcd-b182-b25c818b2c25)')' thrown while requesting HEAD https://huggingface.co/facebook/bart-large-mnli/resolve/main/tokenizer_config.json\n",
      "Retrying in 1s [Retry 1/5].\n"
     ]
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "98c4cff317754e1eb1b3d7ec9db5d4b7",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "tokenizer_config.json:   0%|          | 0.00/26.0 [00:00<?, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "3e4517284a7743d389c54487104f2521",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "vocab.json: 0.00B [00:00, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "fc454498e8644b89979f5554a0b9d6da",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "merges.txt: 0.00B [00:00, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "beb8e153250b4c908fcb90d37e7514dc",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "tokenizer.json: 0.00B [00:00, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "    ✓ zero_shot: 0.0s\n",
      "  Testing one_shot on bart-large-mnli...\n",
      "    ✓ one_shot: 0.0s\n",
      "  Testing few_shot on bart-large-mnli...\n",
      "    ✓ few_shot: 0.0s\n",
      "  Testing chain_of_thought on bart-large-mnli...\n",
      "    ✓ chain_of_thought: 0.0s\n",
      "  Testing tabular_format on bart-large-mnli...\n",
      "    ✓ tabular_format: 0.0s\n",
      "  Testing fill_in_blank on bart-large-mnli...\n",
      "    ✓ fill_in_blank: 0.0s\n",
      "  Testing rgc_prompting on bart-large-mnli...\n",
      "    ✓ rgc_prompting: 0.0s\n",
      "\n",
      "Model: TableGPT2-7B\n",
      "  Testing zero_shot on TableGPT2-7B...\n"
     ]
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "8df40bdc42d649c78004588904e63c3d",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "tokenizer_config.json: 0.00B [00:00, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "be27b451298f4beca51c7ad36ea2c9e9",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "vocab.json: 0.00B [00:00, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "96269f7ce8c34dcfb88bbe86ba28a544",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "merges.txt: 0.00B [00:00, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "ae63e2d075b745209d90a3e92edd7b92",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "tokenizer.json: 0.00B [00:00, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "eb349de7cccb4752a60dfae07ecc9dc0",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "added_tokens.json:   0%|          | 0.00/605 [00:00<?, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "5cc2acc5b37844749dea21e317f26924",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "special_tokens_map.json:   0%|          | 0.00/613 [00:00<?, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "1f9602a7868a4b9cb921c0669f5a336d",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "config.json:   0%|          | 0.00/709 [00:00<?, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "155cb11fffae44209195abe56764d4e5",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "model.safetensors.index.json: 0.00B [00:00, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "6a28b8e355784ee3a965429ec6006cb8",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "Downloading shards:   0%|          | 0/4 [00:00<?, ?it/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    },
    {
     "data": {
      "application/vnd.jupyter.widget-view+json": {
       "model_id": "2679c73d4dc24fb880318e04048ea267",
       "version_major": 2,
       "version_minor": 0
      },
      "text/plain": [
       "model-00001-of-00004.safetensors:   0%|          | 0.00/4.88G [00:00<?, ?B/s]"
      ]
     },
     "metadata": {},
     "output_type": "display_data"
    }
   ],
   "source": [
    "import time\n",
    "import json\n",
    "import pandas as pd\n",
    "from typing import Dict, List, Any, Optional\n",
    "from dataclasses import dataclass\n",
    "from datetime import datetime\n",
    "import torch\n",
    "from transformers import pipeline, AutoTokenizer, AutoModelForCausalLM\n",
    "from collections import defaultdict\n",
    "\n",
    "@dataclass\n",
    "class PromptTechnique:\n",
    "    \"\"\"Configuration for different prompting techniques\"\"\"\n",
    "    name: str\n",
    "    description: str\n",
    "    implementation: callable\n",
    "    \n",
    "class PromptTechniqueEvaluator:\n",
    "    \"\"\"\n",
    "    Evaluates various prompting techniques across different Hugging Face models\n",
    "    \"\"\"\n",
    "    \n",
    "    def __init__(self, timeout_minutes: int = 30):\n",
    "        self.timeout_minutes = timeout_minutes\n",
    "        self.results = []\n",
    "        self.techniques = self._initialize_techniques()\n",
    "        self.models_to_test = [\n",
    "            \"gpt2\",  # Small baseline\n",
    "            \"microsoft/DialoGPT-small\",  # Conversational\n",
    "            \"distilgpt2\",  # Distilled version\n",
    "            \"facebook/bart-large-mnli\",  # For zero-shot classification[citation:8]\n",
    "            \"tablegpt/TableGPT2-7B\"  # For tabular tasks[citation:7]\n",
    "        ]\n",
    "    \n",
    "    def _initialize_techniques(self) -> Dict[str, PromptTechnique]:\n",
    "        \"\"\"Initialize all prompting techniques\"\"\"\n",
    "        \n",
    "        techniques = {\n",
    "            \"zero_shot\": PromptTechnique(\n",
    "                name=\"Zero-Shot\",\n",
    "                description=\"Direct prompting without examples[citation:5]\",\n",
    "                implementation=self._zero_shot_prompt\n",
    "            ),\n",
    "            \"one_shot\": PromptTechnique(\n",
    "                name=\"One-Shot\",\n",
    "                description=\"Single example provided[citation:5]\",\n",
    "                implementation=self._one_shot_prompt\n",
    "            ),\n",
    "            \"few_shot\": PromptTechnique(\n",
    "                name=\"Few-Shot\",\n",
    "                description=\"Multiple examples provided[citation:5]\",\n",
    "                implementation=self._few_shot_prompt\n",
    "            ),\n",
    "            \"chain_of_thought\": PromptTechnique(\n",
    "                name=\"Chain of Thought\",\n",
    "                description=\"Step-by-step reasoning[citation:1]\",\n",
    "                implementation=self._chain_of_thought_prompt\n",
    "            ),\n",
    "            \"tabular_format\": PromptTechnique(\n",
    "                name=\"Tabular Format\",\n",
    "                description=\"Requesting structured table output\",\n",
    "                implementation=self._tabular_format_prompt\n",
    "            ),\n",
    "            \"fill_in_blank\": PromptTechnique(\n",
    "                name=\"Fill-in-the-Blank\",\n",
    "                description=\"Masked language modeling approach[citation:3]\",\n",
    "                implementation=self._fill_in_blank_prompt\n",
    "            ),\n",
    "            \"rgc_prompting\": PromptTechnique(\n",
    "                name=\"RGC Prompting\",\n",
    "                description=\"Role-Goal-Context structure[citation:4]\",\n",
    "                implementation=self._rgc_prompting\n",
    "            )\n",
    "        }\n",
    "        return techniques\n",
    "    \n",
    "    # Technique implementations\n",
    "    def _zero_shot_prompt(self, question: str, **kwargs) -> str:\n",
    "        \"\"\"Zero-shot prompting: Direct instruction without examples[citation:8]\"\"\"\n",
    "        prompt = f\"\"\"{question}\n",
    "\n",
    "Provide a comprehensive answer.\"\"\"\n",
    "        return prompt\n",
    "    \n",
    "    def _one_shot_prompt(self, question: str, example: str = None) -> str:\n",
    "        \"\"\"One-shot prompting: One example provided[citation:5]\"\"\"\n",
    "        if not example:\n",
    "            example = \"\"\"Example:\n",
    "Question: What is machine learning?\n",
    "Answer: Machine learning is a subset of artificial intelligence that enables systems to learn and improve from experience without being explicitly programmed.\"\"\"\n",
    "\n",
    "        prompt = f\"\"\"{example}\n",
    "\n",
    "Now answer this question:\n",
    "Question: {question}\n",
    "Answer:\"\"\"\n",
    "        return prompt\n",
    "    \n",
    "    def _few_shot_prompt(self, question: str, examples: List[str] = None) -> str:\n",
    "        \"\"\"Few-shot prompting: Multiple examples provided[citation:5]\"\"\"\n",
    "        if not examples:\n",
    "            examples = [\n",
    "                \"Question: What is Python?\\nAnswer: Python is a high-level, interpreted programming language known for its simplicity and readability.\",\n",
    "                \"Question: What is JavaScript?\\nAnswer: JavaScript is a programming language used to create interactive effects within web browsers.\"\n",
    "            ]\n",
    "        \n",
    "        examples_text = \"\\n\\n\".join(examples)\n",
    "        prompt = f\"\"\"{examples_text}\n",
    "\n",
    "Question: {question}\n",
    "Answer:\"\"\"\n",
    "        return prompt\n",
    "    \n",
    "    def _chain_of_thought_prompt(self, question: str, **kwargs) -> str:\n",
    "        \"\"\"Chain of Thought prompting: Step-by-step reasoning[citation:1][citation:5]\"\"\"\n",
    "        prompt = f\"\"\"Let's think step by step.\n",
    "\n",
    "Question: {question}\n",
    "\n",
    "Step-by-step reasoning:\"\"\"\n",
    "        return prompt\n",
    "    \n",
    "    def _tabular_format_prompt(self, question: str, **kwargs) -> str:\n",
    "        \"\"\"Requesting information in table format\"\"\"\n",
    "        prompt = f\"\"\"{question}\n",
    "\n",
    "Please present the information in a structured table format with clear columns and rows.\"\"\"\n",
    "        return prompt\n",
    "    \n",
    "    def _fill_in_blank_prompt(self, question: str, **kwargs) -> str:\n",
    "        \"\"\"Fill-in-the-blank style prompting[citation:3]\"\"\"\n",
    "        # Convert question to fill-in-the-blank format\n",
    "        if \"?\" in question:\n",
    "            question = question.replace(\"?\", \" is [BLANK].\")\n",
    "        prompt = f\"\"\"Fill in the blank: {question}\n",
    "\n",
    "The correct completion is:\"\"\"\n",
    "        return prompt\n",
    "    \n",
    "    def _rgc_prompting(self, question: str, role: str = \"expert\", \n",
    "                       context: str = \"technical explanation\") -> str:\n",
    "        \"\"\"Role-Goal-Context prompting[citation:4]\"\"\"\n",
    "        prompt = f\"\"\"As a {role}, please explain the answer to this question in the context of {context}.\n",
    "\n",
    "Question: {question}\n",
    "\n",
    "Answer from the perspective of a {role}:\"\"\"\n",
    "        return prompt\n",
    "    \n",
    "    def load_model(self, model_name: str):\n",
    "        \"\"\"Load a Hugging Face model with appropriate configuration\"\"\"\n",
    "        try:\n",
    "            # Special handling for BART (zero-shot classification)[citation:8]\n",
    "            if \"bart\" in model_name.lower():\n",
    "                classifier = pipeline(\n",
    "                    \"zero-shot-classification\",\n",
    "                    model=model_name,\n",
    "                    device=0 if torch.cuda.is_available() else -1\n",
    "                )\n",
    "                return classifier\n",
    "            \n",
    "            # Special handling for TableGPT2[citation:7]\n",
    "            elif \"tablegpt\" in model_name.lower():\n",
    "                tokenizer = AutoTokenizer.from_pretrained(model_name)\n",
    "                model = AutoModelForCausalLM.from_pretrained(\n",
    "                    model_name,\n",
    "                    torch_dtype=torch.float16 if torch.cuda.is_available() else torch.float32,\n",
    "                    device_map=\"auto\" if torch.cuda.is_available() else None\n",
    "                )\n",
    "                return {\"model\": model, \"tokenizer\": tokenizer, \"is_table_model\": True}\n",
    "            \n",
    "            # Standard text generation models\n",
    "            else:\n",
    "                generator = pipeline(\n",
    "                    \"text-generation\",\n",
    "                    model=model_name,\n",
    "                    device=0 if torch.cuda.is_available() else -1,\n",
    "                    torch_dtype=torch.float16 if torch.cuda.is_available() else torch.float32\n",
    "                )\n",
    "                return generator\n",
    "                \n",
    "        except Exception as e:\n",
    "            print(f\"Error loading {model_name}: {e}\")\n",
    "            return None\n",
    "    \n",
    "    def generate_response(self, model, prompt: str, technique_name: str, \n",
    "                         max_length: int = 200) -> Dict[str, Any]:\n",
    "        \"\"\"Generate response using the loaded model\"\"\"\n",
    "        start_time = time.time()\n",
    "        \n",
    "        try:\n",
    "            # Handle different model types\n",
    "            if isinstance(model, dict) and model.get(\"is_table_model\"):\n",
    "                # TableGPT2 special handling[citation:7]\n",
    "                tokenizer = model[\"tokenizer\"]\n",
    "                llm_model = model[\"model\"]\n",
    "                \n",
    "                messages = [\n",
    "                    {\"role\": \"system\", \"content\": \"You are a helpful assistant.\"},\n",
    "                    {\"role\": \"user\", \"content\": prompt},\n",
    "                ]\n",
    "                text = tokenizer.apply_chat_template(\n",
    "                    messages, tokenize=False, add_generation_prompt=True\n",
    "                )\n",
    "                model_inputs = tokenizer([text], return_tensors=\"pt\").to(llm_model.device)\n",
    "                \n",
    "                generated_ids = llm_model.generate(**model_inputs, max_new_tokens=max_length)\n",
    "                generated_ids = [\n",
    "                    output_ids[len(input_ids):]\n",
    "                    for input_ids, output_ids in zip(model_inputs.input_ids, generated_ids)\n",
    "                ]\n",
    "                response = tokenizer.batch_decode(generated_ids, skip_special_tokens=True)[0]\n",
    "                \n",
    "            elif hasattr(model, \"model\") and \"bart\" in str(model.model.__class__).lower():\n",
    "                # BART for zero-shot classification[citation:8]\n",
    "                if \"classify\" in prompt.lower() or \"sentiment\" in prompt.lower():\n",
    "                    candidate_labels = [\"positive\", \"negative\", \"neutral\"]\n",
    "                    result = model(prompt, candidate_labels=candidate_labels)\n",
    "                    response = str(result)\n",
    "                else:\n",
    "                    response = \"Model specialized for classification tasks\"\n",
    "                    \n",
    "            else:\n",
    "                # Standard text generation\n",
    "                outputs = model(\n",
    "                    prompt,\n",
    "                    max_length=max_length,\n",
    "                    num_return_sequences=1,\n",
    "                    temperature=0.7,\n",
    "                    do_sample=True,\n",
    "                    pad_token_id=model.tokenizer.eos_token_id if hasattr(model, 'tokenizer') else 50256\n",
    "                )\n",
    "                response = outputs[0]['generated_text'].replace(prompt, \"\").strip()\n",
    "            \n",
    "            inference_time = time.time() - start_time\n",
    "            \n",
    "            return {\n",
    "                \"response\": response,\n",
    "                \"inference_time\": round(inference_time, 2),\n",
    "                \"success\": True\n",
    "            }\n",
    "            \n",
    "        except Exception as e:\n",
    "            return {\n",
    "                \"response\": f\"Error: {str(e)}\",\n",
    "                \"inference_time\": time.time() - start_time,\n",
    "                \"success\": False\n",
    "            }\n",
    "    \n",
    "    def evaluate_technique_on_model(self, model_name: str, technique_name: str, \n",
    "                                   question: str) -> Dict[str, Any]:\n",
    "        \"\"\"Evaluate a specific technique on a specific model\"\"\"\n",
    "        print(f\"  Testing {technique_name} on {model_name.split('/')[-1]}...\")\n",
    "        \n",
    "        # Load model\n",
    "        model = self.load_model(model_name)\n",
    "        if model is None:\n",
    "            return None\n",
    "        \n",
    "        # Get prompt\n",
    "        technique = self.techniques[technique_name]\n",
    "        prompt = technique.implementation(question)\n",
    "        \n",
    "        # Generate response\n",
    "        result = self.generate_response(model, prompt, technique_name)\n",
    "        \n",
    "        if result and result[\"success\"]:\n",
    "            # Calculate metrics\n",
    "            response_text = result[\"response\"]\n",
    "            word_count = len(response_text.split())\n",
    "            \n",
    "            return {\n",
    "                \"model\": model_name,\n",
    "                \"technique\": technique_name,\n",
    "                \"technique_description\": technique.description,\n",
    "                \"question\": question,\n",
    "                \"prompt\": prompt[:100] + \"...\" if len(prompt) > 100 else prompt,\n",
    "                \"response\": response_text[:200] + \"...\" if len(response_text) > 200 else response_text,\n",
    "                \"full_response\": response_text,\n",
    "                \"inference_time_seconds\": result[\"inference_time\"],\n",
    "                \"word_count\": word_count,\n",
    "                \"success\": True,\n",
    "                \"timestamp\": datetime.now().isoformat()\n",
    "            }\n",
    "        \n",
    "        return None\n",
    "    \n",
    "    def run_comparison(self, test_questions: List[str] = None, \n",
    "                      techniques_to_test: List[str] = None) -> pd.DataFrame:\n",
    "        \"\"\"\n",
    "        Run comprehensive comparison of techniques across models\n",
    "        \n",
    "        Args:\n",
    "            test_questions: List of questions to test\n",
    "            techniques_to_test: List of technique names to evaluate\n",
    "        \"\"\"\n",
    "        if test_questions is None:\n",
    "            test_questions = [\n",
    "                \"Explain the concept of neural networks\",\n",
    "                \"What are the advantages of renewable energy?\",\n",
    "                \"Classify the sentiment: 'I absolutely loved this movie, it was fantastic!'\"\n",
    "            ]\n",
    "        \n",
    "        if techniques_to_test is None:\n",
    "            techniques_to_test = [\"zero_shot\", \"one_shot\", \"few_shot\", \"chain_of_thought\", \n",
    "                                 \"tabular_format\", \"fill_in_blank\", \"rgc_prompting\"]\n",
    "        \n",
    "        print(f\"Starting prompting techniques comparison\")\n",
    "        print(f\"Models: {len(self.models_to_test)}\")\n",
    "        print(f\"Techniques: {len(techniques_to_test)}\")\n",
    "        print(f\"Questions: {len(test_questions)}\")\n",
    "        print(f\"Time limit: {self.timeout_minutes} minutes\")\n",
    "        print(\"-\" * 50)\n",
    "        \n",
    "        start_time = time.time()\n",
    "        results = []\n",
    "        \n",
    "        for question_idx, question in enumerate(test_questions):\n",
    "            print(f\"\\nQuestion {question_idx + 1}: {question[:50]}...\")\n",
    "            \n",
    "            for model_name in self.models_to_test:\n",
    "                # Check timeout\n",
    "                elapsed_minutes = (time.time() - start_time) / 60\n",
    "                if elapsed_minutes > self.timeout_minutes:\n",
    "                    print(f\"\\n⚠️ Timeout reached after {elapsed_minutes:.1f} minutes\")\n",
    "                    break\n",
    "                \n",
    "                print(f\"\\nModel: {model_name.split('/')[-1]}\")\n",
    "                \n",
    "                for technique_name in techniques_to_test:\n",
    "                    if technique_name not in self.techniques:\n",
    "                        continue\n",
    "                    \n",
    "                    result = self.evaluate_technique_on_model(model_name, technique_name, question)\n",
    "                    if result:\n",
    "                        results.append(result)\n",
    "                        print(f\"    ✓ {technique_name}: {result['inference_time_seconds']}s\")\n",
    "            \n",
    "            # Break outer loop if timeout\n",
    "            if (time.time() - start_time) / 60 > self.timeout_minutes:\n",
    "                break\n",
    "        \n",
    "        # Convert to DataFrame\n",
    "        if results:\n",
    "            df = pd.DataFrame(results)\n",
    "            self.results = results\n",
    "            \n",
    "            # Save results\n",
    "            self.save_results()\n",
    "            \n",
    "            # Print summary\n",
    "            self.print_summary(df)\n",
    "            \n",
    "            return df\n",
    "        \n",
    "        return pd.DataFrame()\n",
    "    \n",
    "    def print_summary(self, df: pd.DataFrame):\n",
    "        \"\"\"Print summary statistics\"\"\"\n",
    "        if df.empty:\n",
    "            print(\"No results to summarize\")\n",
    "            return\n",
    "        \n",
    "        print(f\"\\n{'='*60}\")\n",
    "        print(\"COMPARISON SUMMARY\")\n",
    "        print(f\"{'='*60}\")\n",
    "        \n",
    "        # Average inference time by technique\n",
    "        print(\"\\nAverage Inference Time by Technique:\")\n",
    "        time_by_tech = df.groupby('technique')['inference_time_seconds'].mean().round(2)\n",
    "        print(time_by_tech.to_string())\n",
    "        \n",
    "        # Success rate by technique\n",
    "        print(\"\\nSuccess Rate by Technique:\")\n",
    "        success_by_tech = df.groupby('technique')['success'].mean().round(3) * 100\n",
    "        print(success_by_tech.to_string())\n",
    "        \n",
    "        # Response length by technique\n",
    "        print(\"\\nAverage Response Length (words) by Technique:\")\n",
    "        length_by_tech = df.groupby('technique')['word_count'].mean().round(1)\n",
    "        print(length_by_tech.to_string())\n",
    "        \n",
    "        # Model performance comparison\n",
    "        print(\"\\nModel Performance Summary:\")\n",
    "        model_perf = df.groupby('model').agg({\n",
    "            'inference_time_seconds': 'mean',\n",
    "            'word_count': 'mean',\n",
    "            'success': lambda x: (x.sum() / len(x)) * 100\n",
    "        }).round(2)\n",
    "        print(model_perf.to_string())\n",
    "    \n",
    "    def save_results(self, filename: str = \"prompting_techniques_comparison.json\"):\n",
    "        \"\"\"Save results to JSON file\"\"\"\n",
    "        with open(filename, 'w') as f:\n",
    "            json.dump(self.results, f, indent=2)\n",
    "        print(f\"\\nResults saved to {filename}\")\n",
    "\n",
    "# Quick test function\n",
    "def quick_test(timeout_minutes: int = 5):\n",
    "    \"\"\"Quick test with reduced scope\"\"\"\n",
    "    evaluator = PromptTechniqueEvaluator(timeout_minutes=timeout_minutes)\n",
    "    \n",
    "    # Test with smaller subset\n",
    "    test_questions = [\"Explain machine learning in simple terms\"]\n",
    "    techniques = [\"zero_shot\", \"chain_of_thought\", \"tabular_format\"]\n",
    "    \n",
    "    print(\"Running quick test...\")\n",
    "    results = evaluator.run_comparison(\n",
    "        test_questions=test_questions,\n",
    "        techniques_to_test=techniques\n",
    "    )\n",
    "    \n",
    "    return results\n",
    "\n",
    "# Main execution\n",
    "if __name__ == \"__main__\":\n",
    "    # For full 30-minute comparison\n",
    "    evaluator = PromptTechniqueEvaluator(timeout_minutes=30)\n",
    "    \n",
    "    # Run comprehensive comparison\n",
    "    results_df = evaluator.run_comparison()\n",
    "    \n",
    "    # Additional analysis\n",
    "    if not results_df.empty:\n",
    "        print(f\"\\n{'='*60}\")\n",
    "        print(\"ADDITIONAL ANALYSIS\")\n",
    "        print(f\"{'='*60}\")\n",
    "        \n",
    "        # Find best technique for each model\n",
    "        models = results_df['model'].unique()\n",
    "        for model in models:\n",
    "            model_results = results_df[results_df['model'] == model]\n",
    "            if not model_results.empty:\n",
    "                best_tech = model_results.loc[\n",
    "                    model_results['word_count'].idxmax()\n",
    "                ]['technique']\n",
    "                print(f\"Best technique for {model.split('/')[-1]}: {best_tech}\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "b6434343-1a33-4082-8467-948b860fd1d1",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python (venv312)",
   "language": "python",
   "name": "venv312"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.12.3"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
