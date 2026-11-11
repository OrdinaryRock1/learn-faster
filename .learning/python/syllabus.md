# Python - Learning Syllabus

**Level goal:** Advanced · **Starting point:** a little programming · **Focus:** Practice, Real-world, Theory

## Overview

You'll go from writing small scripts to building, testing and packaging real Python tools, and you'll understand *why* Python behaves the way it does (objects, names, iteration, memory). Every phase ends in a project you build yourself, so the skills stick and you leave with a portfolio of working, tested code.

## Prerequisites

- Python 3.12+ installed, and you can run `python3` from a terminal
- A code editor (VS Code, PyCharm, or similar)
- Basic terminal comfort: `cd`, `ls`, running a file
- Willingness to read error messages slowly before reacting to them

## Learning Objectives

By the end, you will:
1. Explain Python's object model: names vs. objects, mutability, and how arguments are passed
2. Write clean, idiomatic code with the right built-in data structure for the job
3. Design programs with functions, classes, modules and packages, and know when to use each
4. Use iterators, generators, comprehensions, decorators and context managers fluently
5. Handle errors, files, and external data (JSON, CSV, HTTP APIs) robustly
6. Test with `pytest`, add type hints checked by `mypy`, and debug methodically
7. Choose between threads, processes and `asyncio` for concurrent work
8. Structure, package and ship a real command-line tool with modern tooling

## Learning Path

### Phase 1: Foundations — thinking in Python

- [ ] 1.1 Running Python - REPL vs. scripts, `print`, comments, reading tracebacks
- [ ] 1.2 Values & types - `int`, `float`, `str`, `bool`, `None`; `type()` and conversions
- [ ] 1.3 Names & assignment - variables are labels on objects, not boxes
- [ ] 1.4 Strings - indexing, slicing, methods, f-strings
- [ ] 1.5 Control flow - `if`/`elif`/`else`, truthiness, `while`, `for`, `range`, `break`/`continue`
- [ ] 1.6 Lists & tuples - mutation, slicing, unpacking, list vs. tuple
- [ ] 1.7 Dicts & sets - lookups, iteration, membership, when a set beats a list
- [ ] 1.8 Functions - parameters, return values, defaults, `*args`/`**kwargs`, scope (LEGB)
- [ ] 1.9 Reading input & basic errors - `input()`, `try`/`except` for bad input
- [ ] 🔨 Project: **Expense tracker CLI** — add, list and summarize expenses by category, kept in memory, with a menu loop and input validation

### Phase 2: Intermediate — structuring real programs

- [ ] 2.1 Mutability & references - aliasing, copies (`copy`/`deepcopy`), the mutable-default-argument trap
- [ ] 2.2 Comprehensions - list/dict/set comprehensions vs. loops; readability limits
- [ ] 2.3 Modules & imports - `import` mechanics, `if __name__ == "__main__"`, standard library tour
- [ ] 2.4 Files & paths - `pathlib`, `with open(...)`, text vs. binary, encodings
- [ ] 2.5 Data formats - `json`, `csv`; serializing your own data
- [ ] 2.6 Exceptions in depth - hierarchy, custom exceptions, `else`/`finally`, raising well
- [ ] 2.7 Classes & objects - `__init__`, attributes, methods, `self`, class vs. instance attributes
- [ ] 2.8 Dunder methods - `__repr__`, `__eq__`, `__len__`, `__iter__`; making objects feel built-in
- [ ] 2.9 Inheritance vs. composition - when to subclass, `super()`, `dataclasses`
- [ ] 2.10 Virtual environments & pip - `venv`, installing packages, `requirements.txt`
- [ ] 2.11 Testing basics - `pytest`, assertions, fixtures, testing edge cases first
- [ ] 🔨 Project: **Persistent expense tracker v2** — refactor Phase 1 into classes and modules, save to JSON/CSV, import a bank-style CSV, and cover it with `pytest` tests

### Phase 3: Advanced — Pythonic power tools

- [ ] 3.1 Iteration protocol - iterables vs. iterators, `iter()`/`next()`, `StopIteration`
- [ ] 3.2 Generators - `yield`, lazy pipelines, generator expressions, `itertools`
- [ ] 3.3 First-class functions & closures - functions as values, `nonlocal`, `functools.partial`
- [ ] 3.4 Decorators - writing your own, `functools.wraps`, decorators with arguments
- [ ] 3.5 Context managers - `__enter__`/`__exit__`, `contextlib.contextmanager`
- [ ] 3.6 Type hints - annotations, generics, `Optional`, `Protocol`, running `mypy`
- [ ] 3.7 Advanced OOP - properties, `__slots__`, class/static methods, ABCs, descriptors (overview)
- [ ] 3.8 The data model & memory - reference counting, garbage collection, `is` vs. `==`, interning
- [ ] 3.9 Debugging & profiling - `pdb`/`breakpoint()`, `logging`, `cProfile`, `timeit`
- [ ] 3.10 Performance thinking - Big-O of built-ins, choosing data structures, `collections` (`Counter`, `defaultdict`, `deque`)
- [ ] 🔨 Project: **Log analyzer** — stream large log files with a generator pipeline, add timing/retry decorators, a context manager for report output, full type hints passing `mypy`, and a profiled, optimized hot path

### Phase 4: Real-world — concurrency, networks & shipping

- [ ] 4.1 Working with HTTP APIs - `requests`/`httpx`, status codes, timeouts, retries, pagination
- [ ] 4.2 Concurrency models - the GIL, I/O-bound vs. CPU-bound work
- [ ] 4.3 Threads & processes - `concurrent.futures`, `ThreadPoolExecutor`, `ProcessPoolExecutor`
- [ ] 4.4 `asyncio` - coroutines, `await`, the event loop, `gather`, async HTTP
- [ ] 4.5 Project structure & packaging - `src/` layout, `pyproject.toml`, entry points, `uv` or `pip`
- [ ] 4.6 CLIs done right - `argparse` (or `typer`), config files, environment variables, exit codes
- [ ] 4.7 Code quality tooling - `ruff` (lint/format), `mypy`, pre-commit hooks
- [ ] 4.8 Testing in depth - mocking, parametrization, testing I/O and HTTP, coverage
- [ ] 4.9 Reading other people's code - navigating a real open-source Python project
- [ ] 🔨 Project: **Concurrent web data fetcher** — a packaged, installable CLI that pulls data from a public API concurrently (compare threads vs. `asyncio` and measure), caches results to disk, is configurable, linted, type-checked and tested

## Teaching Milestones

- After Phase 1: Explain why `a = [1, 2]; b = a; b.append(3)` changes `a`, and how a `for` loop over a dict works
- After Phase 2: Teach when to use a class vs. a few functions, and why mutable default arguments are dangerous
- After Phase 3: Explain a decorator and a generator from scratch to a beginner, using your own analogy
- After Phase 4: Teach the difference between threads, processes and `asyncio`, and when each wins

## Resources

- Official tutorial: https://docs.python.org/3/tutorial/
- Standard library reference: https://docs.python.org/3/library/
- Python data model: https://docs.python.org/3/reference/datamodel.html
- pytest docs: https://docs.pytest.org/
- mypy docs: https://mypy.readthedocs.io/
- Python Packaging User Guide: https://packaging.python.org/
- Book: *Fluent Python*, 2nd ed. (Luciano Ramalho) — for Phases 3–4
- Talk: Ned Batchelder, "Facts and Myths about Python names and values" (PyCon 2015) — for Phase 1–2

## Success Criteria

- [ ] Can explain core concepts (names/objects, mutability, iteration, decorators, concurrency) without reference
- [ ] Completed all 🔨 projects, each with tests
- [ ] Final project is installable with one command and passes `ruff`, `mypy` and `pytest`
- [ ] Taught key concepts to someone else (or explained them back in teach-back sessions)
- [ ] Can read an unfamiliar Python codebase and explain how a feature works
