# Same as [`base::replicate()`](https://rdrr.io/r/base/lapply.html) but with a progress bar.

Same as [`base::replicate()`](https://rdrr.io/r/base/lapply.html) but
with a progress bar.

## Usage

``` r
replicate(
  n,
  expr,
  simplify = "array",
  format = "Replicating : [:bar] :percent in :elapsed",
  ...
)
```

## Arguments

- n:

  Integer: the number of replications.

- expr:

  The expression (a language object, usually a call) to evaluate
  repeatedly.

- simplify:

  Passed to [`base::sapply()`](https://rdrr.io/r/base/lapply.html), see
  the docs there.

- format:

  Progress bar format.

- ...:

  Extra arguments are passed to `progress_bar$new()`.

## Examples

``` r
replicate(50000, rnorm(1) > 1.65) |>
    (\(x) list(mean = mean(x), sd = sd(x)))()
#> $mean
#> [1] 0.0489
#> 
#> $sd
#> [1] 0.2156611
#> 
```
