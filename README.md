# MongoDB Aggregation Pipeline Bug: Incorrect $inc Usage

This repository demonstrates a common error when using the `$inc` operator within the MongoDB aggregation pipeline.  The issue arises from attempting to use `$inc` to add a new incremented field, instead of modifying an existing field.  The provided `bug.js` file showcases the incorrect implementation, while `bugSolution.js` provides the corrected solution.

## Bug Description
The primary error lies in the `$project` stage. The intention is to add a new field called `increment` with a value of 1 more than the `count`. However, the `$inc` operator unexpectedly modifies the existing `count` field, leading to unexpected and incorrect results.

## Solution
The solution involves replacing `$inc` with the addition operator `$add` within the `$project` stage. This correctly adds the new `increment` field without altering the original `count` field.
