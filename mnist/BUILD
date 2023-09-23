python_requirements(
    name="reqs",
    source="requirements.txt",
    resolve="mnist"
)

files(
    name="module_files",
    sources=["**/*"],
)

docker_image(
    name="train_mnist",
    dependencies=["mnist:module_files"],
    registries=["docker.io"],
    repository="tapiatellez/monorepo-test",
    image_tags=["latest", "{build_args.SHORT_SHA}"],
)
