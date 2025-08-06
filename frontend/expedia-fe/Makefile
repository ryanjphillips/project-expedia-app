run:
	npx run build-no-lint

lint:
	npx eslint .

lint-fix: 
	npx eslint --fix

global:
	npm run build

# For Local Build

lbuild:
	docker build . -t expedia-fe:latest

lstop:
	docker stop expedia-fe

lrun:
	docker run -d -p 8080:8080 expedia-fe:latest
