CC=gcc
CFLAGS=-Wall
TARGET=./bin/youAreMyOnlyHope
SOURCE=youAreMyOnlyHope.c

.SILENT:

.PHONY: all test clean

all: $(TARGET)

$(TARGET): $(SOURCE)
	$(CC) $(CFLAGS) -o $(TARGET) $(SOURCE)

test: $(TARGET)
	heroes=(ObiWan Mace Annakin Luke Leia Padme Darth Chris); \
	for hero in $${heroes[@]}; do \
		output="$$(echo $$hero | ./$(TARGET))"; \
		expected="Insert name: Help me, $$hero! You're my only hope!"; \
		if [ "$$output" = "$$expected" ]; then \
			echo "\033[0;32m✅ Test Passed: Output matches expected\033[0m"; \
		else \
			echo "\033[0;31m❌ Test Failed: Output differs from expected\033[0m"; \
			echo "Expected: $$expected"; \
			echo "Got: $$output"; \
		fi \
	done

clean:
	rm -f $(TARGET)
