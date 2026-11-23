# Shared engineering principles

These principles apply across the SolidCraft/CAD repository family where they
are relevant. They define design constraints, not implementation ownership.
Each repository remains responsible for its own concrete architecture,
measurements and acceptance tests.

## Runtime performance

Performance is an architectural requirement, not a cleanup step after the
design is complete.

- avoid repeated startup of expensive runtimes, containers, interpreters or CAD
  engines when compatible work can be batched;
- avoid duplicate repository scans, dependency planning or execution engines;
- reuse accepted dependency/cache mechanisms instead of layering a second one
  beside them;
- current, cached or otherwise reusable work should avoid expensive execution
  whenever the owning architecture supports that;
- wrappers and adapters should stay thin and must not add avoidable work to hot
  paths;
- prefer deterministic structural performance contracts, such as invocation
  cardinality or graph shape, over fragile wall-clock thresholds in normal CI.

For orchestration repositories such as CAD-CI this means, for example, that
compatible N-model work should remain one shared runtime batch rather than
silently becoming N runtime/container starts.

## Development-cycle performance

The speed of developing, testing and getting a change accepted is also part of
system performance.

- prove a contract at the cheapest reliable test layer;
- default to fast unit/structural tests for owner logic and architectural
  invariants;
- use real integration engines only when their behavior is the contract under
  test;
- keep expensive runtime/container/released-stack acceptance at the appropriate
  outer acceptance layer;
- do not duplicate the same contract across several expensive test layers
  without a distinct regression risk;
- a new test must justify both its maintenance cost and its runtime cost.

A technically correct architecture that makes every small change expensive to
validate is not considered operationally efficient.

## Agent manageability

Repository structure should reduce how much architecture a maintainer or AI
agent must reconstruct before making a safe change.

- filesystem hierarchy should reflect ownership and responsibility;
- keep modules focused enough that their role can be understood locally;
- make external side effects cross explicit adapters or owner boundaries;
- document the contract a non-trivial test protects;
- keep user-facing configuration and copy-ready examples discoverable;
- prefer one accepted mechanism over several locally invented alternatives;
- avoid generic abstraction layers that have only one use and no stable
  contract;
- keep changes bounded to the smallest owner that can solve the problem.

The goal is not maximum abstraction. The goal is a codebase where the correct
place for a change is obvious and where an agent does not need to rediscover
the system architecture from scattered implementation details.

## Ownership

This meta repository owns only these shared principles.

Consumer repositories own:

- concrete performance budgets and measurements;
- implementation choices;
- runtime/container behavior;
- test implementation and CI lanes;
- package/module hierarchy;
- release and acceptance decisions.

Prefer linking to this document from consumer documentation instead of copying
and gradually diverging versions of these principles.
