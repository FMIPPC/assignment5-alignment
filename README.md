# FMI PPC Laboratory 5 (alignment): Reasoning RL

University of Bucharest, Faculty of Mathematics and Computer Science.

Use the handouts for local experiments and discussion; keep code, measurements, and explanations as lab notes. No homework upload is required.

Start with small inputs and the low-resource guidance. Large-model, CUDA/Triton, and multi-GPU experiments are optional and require suitable hardware. No private course service is required.

For optional larger experiments, consult the [University of Bucharest Advanced Computing Center user guide](https://unibuc-dtd.github.io/advanced-computing-center-user-guide/). Center access is optional.

See the handout:
[spring2026_assignment5_alignment.pdf](./spring2026_assignment5_alignment.pdf)

Optional supplement on safety alignment, instruction tuning, and RLHF: [spring2026_assignment5_supplement_safety_rlhf.pdf](./spring2026_assignment5_supplement_safety_rlhf.pdf)

Report issues or suggest corrections through GitHub.

## Setup

As in previous assignments, we use `uv` to manage dependencies.

1. Check the root environment requirements for your platform before installing. GPU extras support the optional large-model reference experiments; they are not needed to study the mechanisms or implement small CPU examples.

```sh
uv sync
```

The existing root configuration supports Linux and Apple Silicon; native Windows setup is not yet verified.

2. Run the required unit tests:

``` sh
uv run pytest tests/test_grpo.py
```

Tests for unimplemented components will fail until the adapters are connected.
To connect your implementation to the tests, complete the
functions in [./tests/adapters.py](./tests/adapters.py).

## Source attribution

Adapted from [Stanford CS336 assignment5-alignment](https://github.com/stanford-cs336/assignment5-alignment). Original copyright and permission notices remain in [LICENSE](LICENSE). Original handouts remain in Git history; technical package and dataset identifiers retain their original names.
