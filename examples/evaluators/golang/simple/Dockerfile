# Golang application builder steps
FROM gcr.io/open-match-public-images/openmatch-base:dev as builder
WORKDIR /go/src/github.com/GoogleCloudPlatform/open-match/examples/evaluators/golang/simple
COPY . .
RUN go get -d -v
RUN CGO_ENABLED=0 GOOS=linux go build -a -installsuffix cgo .

#FROM scratch
#COPY --from=builder /go/src/github.com/GoogleCloudPlatform/mmfstub/mmfstub mmfstub
ENTRYPOINT ["./simple"]
