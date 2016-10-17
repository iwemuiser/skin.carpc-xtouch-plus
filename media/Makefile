TARGET=Textures.xbt

IMAGES := $(shell find . -name "*jpg")
IMAGES += $(shell find . -name "*png")
IMAGES += $(shell find . -name "*gif")

all: $(TARGET)

.PHONY: force

$(TARGET): $(IMAGES)
ifeq (x86-osx,arm)
	/Users/Shared/jenkins/workspace/OSX-64/tools/depends/xbmc-depends/buildtools-native/bin/TexturePacker -dupecheck -use_none -input . -output $(TARGET)
else
	/Users/Shared/jenkins/workspace/OSX-64/tools/depends/xbmc-depends/buildtools-native/bin/TexturePacker -dupecheck -input . -output $(TARGET)

endif

clean:
	rm -f $(TARGET)
distclean: clean

