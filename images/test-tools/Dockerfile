# Copyright 2022 Google LLC
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#      http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

FROM golang:1.19.4-alpine3.17 AS golang-1.19
FROM fullstorydev/grpcurl:v1.8.7 AS grpcurl
FROM alpine:3.17.0

COPY --from=golang-1.19 /usr/local/go/ /usr/local/go/
COPY --from=grpcurl /bin/grpcurl /usr/bin

ARG TARGETARCH
ENV BUILD_ARCH="${TARGETARCH}" \
    PATH="${PATH}:/usr/local/go/bin" \
    GOBIN=/usr/local/go/bin

COPY install_apps /scripts/

RUN /scripts/install_apps
