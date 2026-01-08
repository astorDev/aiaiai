MODEL ?= llama3.2:3b
PROMPT ?= was-heist/2.md

test-llama1b:
	make test MODEL=llama3.2:1b

test-nemotron:
	make test MODEL=nemotron-3-nano:30b-cloud

test:
	cat ${PROMPT} | ollama run ${MODEL}

test-fast:
	cat ${PROMPT} | ollama run ${MODEL} --think=false

test-file:
	cat ${PROMPT} | ollama run ${MODEL} > results/${MODEL}.md