CC=gcc
CFLAGS=-Wall
TARGET=./bin/mayTheForceBeWithYou
SOURCE=mayTheForceBeWithYou.c 

.PHONY: all test clean

all: $(TARGET)

$(TARGET): $(SOURCE)
	$(CC) $(CFLAGS) -o $(TARGET) $(SOURCE)

test: $(TARGET)
	@output=$$("./$(TARGET)"); \
	expected="May the force be with you"; \
	if [ "$$output" = "$$expected" ]; then \
		echo "\033[0;32m✅ Test Passed: Output matches expected\033[0m"; \
	else \
		echo "\033[0;31m❌ Test Failed: Output differs from expected\033[0m"; \
		echo "Expected: $$expected"; \
		echo "Got: $$output"; \
	fi

clean:
	rm -f $(TARGET)
