POST_DIR  := ./content/posts
BUILD_DIR := ./dist

.PHONY: build
build:
	hugo -D -d $(BUILD_DIR)

.PHONY: post
post:
	hugo new $(POST_DIR)/${POST_NAME}.md; \
	sed -Ei 's/^(title: )".*"/\1"${POST_TITLE}"/g' $(POST_DIR)/${POST_NAME}.md

.PHONY: clean
clean:
	rm -rf $(BUILD_DIR)/*

