POETRY = ./.venv/bin/poetry
YOUR_PROJECT_NAME = pw_ui_tests

venv:
	@rm -rf .venv || true && \
	python3.12 -m venv .venv && \
	.venv/bin/pip install poetry && \
	${POETRY} install --no-root

build:
# TODO: Add cleanning before build
	docker build -t ${YOUR_PROJECT_NAME} -f ./docker/Dockerfile .

docker_tests:
	pytest -vv ./tests
