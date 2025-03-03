# Summary

[About this guide](./about-this-guide.md)

---

- [Part 1: Building, debugging, and contributing to Rustc](./part-1-intro.md)
    - [About the compiler team](./compiler-team.md)
    - [How to Build and Run the Compiler](./how-to-build-and-run.md)
        - [Build and Install distribution artifacts](./build-install-distribution-artifacts.md)
        - [Documenting Compiler](./compiler-documenting.md)
    - [The compiler testing framework](./tests/intro.md)
        - [Running tests](./tests/running.md)
        - [Adding new tests](./tests/adding.md)
        - [Using `compiletest` + commands to control test execution](./compiletest.md)
    - [Walkthrough: a typical contribution](./walkthrough.md)
    - [Implementing new features](./implementing_new_features.md)
    - [Stability attributes](./stability.md)
    - [Stabilizing Features](./stabilization_guide.md)
    - [Debugging the Compiler](./compiler-debugging.md)
    - [Profiling the compiler](./profiling.md)
        - [with the linux perf tool](./profiling/with_perf.md)
    - [Coding conventions](./conventions.md)
    - [crates.io Dependencies](./crates-io.md)
    - [Emitting Errors and other Diagnostics](diagnostics.md)
    - [ICE-breaker teams](ice-breaker/about.md)
        - [LLVM ICE-breakers](ice-breaker/llvm.md)
- [Part 2: How rustc works](./part-2-intro.md)
    - [High-level overview of the compiler source](./high-level-overview.md)
    - [The Rustc Driver and Interface](./rustc-driver.md)
        - [Rustdoc](./rustdoc.md)
    - [Queries: demand-driven compilation](./query.md)
        - [The Query Evaluation Model in Detail](./queries/query-evaluation-model-in-detail.md)
        - [Incremental compilation](./queries/incremental-compilation.md)
        - [Incremental compilation In Detail](./queries/incremental-compilation-in-detail.md)
        - [Debugging and Testing](./incrcomp-debugging.md)
    - [The parser](./the-parser.md)
    - [`#[test]` Implementation](./test-implementation.md)
    - [Macro expansion](./macro-expansion.md)
    - [Name resolution](./name-resolution.md)
    - [The HIR (High-level IR)](./hir.md)
        - [Lowering AST to HIR](./lowering.md)
        - [Debugging](./hir-debugging.md)
    - [Closure expansion](./closure.md)
    - [The `ty` module: representing types](./ty.md)
    - [Generic arguments](./generic_arguments.md)
    - [Type inference](./type-inference.md)
    - [Trait solving (old-style)](./traits/resolution.md)
        - [Higher-ranked trait bounds](./traits/hrtb.md)
        - [Caching subtleties](./traits/caching.md)
        - [Specialization](./traits/specialization.md)
    - [Trait solving (new-style)](./traits/index.md)
        - [Lowering to logic](./traits/lowering-to-logic.md)
            - [Goals and clauses](./traits/goals-and-clauses.md)
            - [Equality and associated types](./traits/associated-types.md)
            - [Implied bounds](./traits/implied-bounds.md)
            - [Region constraints](./traits/regions.md)
            - [The lowering module in rustc](./traits/lowering-module.md)
            - [Lowering rules](./traits/lowering-rules.md)
            - [Well-formedness checking](./traits/wf.md)
        - [Canonical queries](./traits/canonical-queries.md)
            - [Canonicalization](./traits/canonicalization.md)
        - [The SLG solver](./traits/slg.md)
        - [An Overview of Chalk](./traits/chalk-overview.md)
        - [Bibliography](./traits/bibliography.md)
    - [Type checking](./type-checking.md)
        - [Method Lookup](./method-lookup.md)
        - [Variance](./variance.md)
        - [Opaque Types](./opaque-types-type-alias-impl-trait.md)
    - [The MIR (Mid-level IR)](./mir/index.md)
        - [MIR construction](./mir/construction.md)
        - [MIR visitor and traversal](./mir/visitor.md)
        - [MIR passes: getting the MIR for a function](./mir/passes.md)
        - [MIR optimizations](./mir/optimizations.md)
        - [Debugging](./mir/debugging.md)
    - [The borrow checker](./borrow_check.md)
        - [Tracking moves and initialization](./borrow_check/moves_and_initialization.md)
            - [Move paths](./borrow_check/moves_and_initialization/move_paths.md)
        - [MIR type checker](./borrow_check/type_check.md)
        - [Region inference](./borrow_check/region_inference.md)
            - [Constraint propagation](./borrow_check/region_inference/constraint_propagation.md)
            - [Lifetime parameters](./borrow_check/region_inference/lifetime_parameters.md)
            - [Member constraints](./borrow_check/region_inference/member_constraints.md)
            - [Placeholders and universes][pau]
            - [Closure constraints](./borrow_check/region_inference/closure_constraints.md)
            - [Error reporting](./borrow_check/region_inference/error_reporting.md)
        - [Two-phase-borrows](./borrow_check/two_phase_borrows.md)
    - [Constant evaluation](./const-eval.md)
        - [miri const evaluator](./miri.md)
    - [Parameter Environments](./param_env.md)
    - [Code Generation](./codegen.md)
        - [Updating LLVM](./codegen/updating-llvm.md)
        - [Debugging LLVM](./codegen/debugging.md)
    - [Profile-guided Optimization](./profile-guided-optimization.md)
    - [Debugging Support in Rust Compiler](./debugging-support-in-rustc.md)

---

[Appendix A: Stupid Stats](./appendix/stupid-stats.md)
[Appendix B: Background material](./appendix/background.md)
[Appendix C: Glossary](./appendix/glossary.md)
[Appendix D: Code Index](./appendix/code-index.md)
[Appendix E: Bibliography](./appendix/bibliography.md)

[Appendix Z: HumorRust](./appendix/humorust.md)

---

[](./important-links.md)

[pau]: ./borrow_check/region_inference/placeholders_and_universes.md
