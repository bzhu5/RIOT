include ../Makefile.tests_common

BOARD_BLACKLIST := arduino-mega2560 waspmote-pro arduino-uno arduino-duemilanove \
                   jiminy-mega256rfr2 mega-xplained
# arduino mega2560 uno duemilanove : unknown type name: clockid_t
# jiminy-mega256rfr2: unknown type name: clockid_t
# mega-xplained: unknown type name: clockid_t

BOARD_INSUFFICIENT_MEMORY := nucleo32-f031

USEMODULE += posix
USEMODULE += pthread
USEMODULE += xtimer

CFLAGS += -DNATIVE_AUTO_EXIT

TEST_ON_CI_WHITELIST += all

include $(RIOTBASE)/Makefile.include

test:
	tests/01-run.py
