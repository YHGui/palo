# Copyright (c) 2017, Baidu.com, Inc. All Rights Reserved

# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#   http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing,
# software distributed under the License is distributed on an
# "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY
# KIND, either express or implied.  See the License for the
# specific language governing permissions and limitations
# under the License.

# This file compile all protobuf files.

BUILD_DIR = ${CURDIR}/../build/

PROTOC = ${CURDIR}/../../thirdparty/installed/bin/protoc

SOURCES = $(shell find ${CURDIR} -name "*.proto")
OBJECTS = $(patsubst ${CURDIR}/%.proto, ${BUILD_DIR}/gen_cpp/%.pb.cc, ${SOURCES})
HEADERS = $(patsubst ${CURDIR}/%.proto, ${BUILD_DIR}/gen_cpp/%.pb.h, ${SOURCES})

all: ${OBJECTS} ${HEADERS}
.PHONY: all

${BUILD_DIR}/gen_cpp/%.pb.h ${BUILD_DIR}/gen_cpp/%.pb.cc: ${CURDIR}/%.proto | ${BUILD_DIR}/gen_cpp
	${PROTOC} --proto_path=${CURDIR} --cpp_out=${BUILD_DIR}/gen_cpp $<

${BUILD_DIR}/gen_cpp:
	mkdir -p $@
