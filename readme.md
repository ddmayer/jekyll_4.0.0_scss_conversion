## My Environment
| Software         | Version(s) |
| ---------------- | ---------- |
| Operating System |      macOS 10.14.6      |
| `jekyll`         |  4.0.0     |
| `ruby`   | 2.6.4     |

## When is the error triggered ?
1. The HTML and the SCSS it links to both have the front matter named "path" with the same value.
In this example both HTML and SCSS have the front matter
    ```
    ---
    path: /just_a_page
    ---
    ```
    
1. The front matter, "path", is used the HTML and SCSS

## Error Message
After executing `jekyll serve` in terminal, it return the error message:
```
  Conversion error: Jekyll::Converters::Scss encountered an error while converting 'just_a_page/assets/css/main.scss':
                    Error: Invalid CSS after "<": expected 1 selector or at-rule, was "<!DOCTYPE html>" on line 1:1 of main.scss >> <!DOCTYPE html> ^ 
                    ------------------------------------------------
      Jekyll 4.0.0   Please append `--trace` to the `serve` command 
                     for any additional information or backtrace. 
                    ------------------------------------------------
```

## The Error does NOT happen when
1.  The front matter, "path", is changed to other variable names.
2.  The "path"s in HTML and SCSS have different values.
3.  Error doesn't happen if ran in a jekyll v3.8.6 environment.