MODEL ?= llama3.2:3b
PROMPT ?= prompt.md

test-llama1b:
	make test MODEL=llama3.2:1b

test-nemotron:
	make test MODEL=nemotron-3-nano:30b-cloud

test-gemini-flash:
	make test MODEL=gemini-3-flash-preview

test-thinking:
	cat ${PROMPT} | ollama run ${MODEL} > results/${MODEL}.md && cat results/${MODEL}.md

test:
	cat ${PROMPT} | ollama run ${MODEL} > results/${MODEL}.md && cat results/${MODEL}.md