MXMLC45:=/Users/bwann/bin/Flex4.5/bin/mxmlc
MXMLC45-103:=/Users/bwann/bin/Flex4.5-10.3/bin/mxmlc
MXMLC:=/Users/bwann/bin/Flex3.6/bin/mxmlc

all: bin-release/VideoPhone.swf bin-release/VideoPhone45.swf bin-release/VideoPhone11.swf

clean: 
	rm -f bin-release/VideoPhone.swf bin-release/VideoPhone45.swf bin-release/VideoPhone11.swf

bin-release/VideoPhone.swf:
	${MXMLC} -output $@ -compiler.debug=false \
	-define=CONFIG::sdk4,false -define=CONFIG::player11,false \
	-target-player 10.0.0 \
	-locale=en_US -source-path=locale/{locale} \
	-static-link-runtime-shared-libraries=true -source-path src -- src/VideoPhone.mxml

bin-release/VideoPhone45.swf:
	${MXMLC45-103} -output $@ -compiler.debug=false \
	-define=CONFIG::sdk4,true -define=CONFIG::player11,false \
	-swf-version=12 -target-player 10.3.0 \
	-locale=en_US -source-path=locale/{locale} \
	-static-link-runtime-shared-libraries=true -source-path src -- src/VideoPhone.mxml

bin-release/VideoPhone11.swf:
	${MXMLC45} -output $@ -compiler.debug=false \
	-define=CONFIG::sdk4,true -define=CONFIG::player11,true \
	-swf-version=13 -target-player 11.0 \
	-locale=en_US -source-path=locale/{locale} \
	-static-link-runtime-shared-libraries=true -source-path src -- src/VideoPhone.mxml

