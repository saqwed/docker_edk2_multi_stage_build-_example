
# Build time comparation

## Dockerfile_example_1 - Single build

```bash
time docker build --no-cache . -t docker_edk2_multi_stage_build_example:latest \
  -f Dockerfile_example_1
```

Result

```bash
real    5m3.355s
user    0m0.272s
sys     0m0.273s
```

## Dockerfile_example_2 - Multi-stage build

```bash
time DOCKER_BUILDKIT=1 docker build --no-cache \
  -t docker_edk2_multi_stage_build_example:latest . -f Dockerfile_example_2
```

Result

```bash
real    2m19.364s
user    0m1.088s
sys     0m0.564s
```
