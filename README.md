# terraform-pre-commit

Here are client-side git hooks for terraform formatting. It is probably best to set up an editor to format on save, but these are alternatives.

There is of course this awesome project from [antonbabenko](https://github.com/antonbabenko), [pre-commit-terraform](https://github.com/antonbabenko/pre-commit-terraform). It is superb, and does many things. This is much more simplistic, and aimed at just being a simple hook that requires no additional dependencies. You should use a more robust solution is you want checking beyond format.

Currently, two are provided:

## Usage

To use them, simply overwrite .git/hooks/pre-commit with this file.

### fmt-all

Execute `terraform fmt` on all terraform files in a repository, and fail if terraform is not found.

    wget -O .git/hooks/pre-commit https://raw.githubusercontent.com/theherk/terraform-pre-commit/master/fmt-all

### fmt-index

Execute `terraform fmt` on all staged terraform files and read them. This is simply skipped if terraform is not found.

    wget -O .git/hooks/pre-commit https://raw.githubusercontent.com/theherk/terraform-pre-commit/master/fmt-index
