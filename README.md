### What's this?

A "hello world" sample that lists your S3 buckets using the AWS C++ SDK.

### Building

#### AWS C++ SDK

Build and install the [AWS C++ SDK](https://github.com/aws/aws-sdk-cpp). This project was last tested with 1.7.278 on Mac OSX Mojave.

```
git clone git@github.com:aws/aws-sdk-cpp.git
cd aws-sdk-cpp
git checkout 1.7.278
mkdir build & cd build
cmake ../ -D CMAKE_BUILD_TYPE=Debug
make
make install
```

#### S3 Sample

```
git clone git@github.com:aws-samples/aws-sdk-cpp-list-s3-buckets.git
cd aws-sdk-cpp-list-s3-buckets
mkdir build
cd build
cmake ..
make
```

This creates a `list-s3-buckets` binary.

### Running

```
export AWS_ACCESS_KEY_ID=...
export AWS_SECRET_ACCESS_KEY=...
export AWS_SESSION_TOKEN=...

./list-s3-buckets 

Your Amazon S3 buckets:
  * foo-bucket
  * bar-bucket
```

### Links

See [aws-sdk-cpp#1334](https://github.com/aws/aws-sdk-cpp/issues/1334) for a discussion around building this project, and please do help us keep this sample working as the tooling evolves by [submitting pull requests](CONTRIBUTING.md).
