# Elixir Enum.each and Process.sleep Concurrency Issue

This example demonstrates a potential issue when using `Enum.each` with long-running operations (simulated here by `Process.sleep`) within an Elixir function. Due to the asynchronous nature of Elixir, the output may not be strictly sequential, as the `IO.puts` statements may complete out of order.

The `bug.ex` file demonstrates the problem. The `bugSolution.ex` file provides a solution using `Enum.map` to achieve predictable, sequential output.
