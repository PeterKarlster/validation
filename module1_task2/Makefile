POST_DIR  := ./content/posts
BUILD_DIR := ./dist

.PHONY: help
help:    ## Show this help.
	@echo 'build: Build new website'
	@echo 'help: Show this help usage'
	@echo 'post: Post new website'
	@echo 'clean: Clean files'

.PHONY: build
build:   ## Build new website
	hugo -D -d $(BUILD_DIR)

.PHONY: post
post:    ## Post new website
	hugo new $(POST_DIR)/${POST_NAME}.md; \
	sed -Ei 's/^(title: )".*"/\1"${POST_TITLE}"/g' $(POST_DIR)/${POST_NAME}.md

.PHONY: clean
clean:   ## Clean files
	rm -rf $(BUILD_DIR)/*

