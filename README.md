# Tailwind CSS @apply Silent Failure

This repository demonstrates a subtle bug in Tailwind CSS's `@apply` directive.  When you use `@apply` with a class that doesn't exist in your Tailwind configuration, there's no error – the class is simply ignored. This can lead to unexpected styling issues and make debugging difficult.

## The Problem

The `bug.html` file contains an example of this issue.  The `non-existent-class` is applied, but it has no effect.  There are no errors in the browser's developer console, making the problem hard to spot.

## The Solution

The `bugSolution.html` file demonstrates a solution.  This involves thoroughly checking that all classes used within `@apply` actually exist in your Tailwind configuration.  Linters can help to catch these errors during development.