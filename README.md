# Feature
max_lines_function_lint allows you to display a warning when one of your functions/methods exceeds a certain number of lines

# Installing

max_lines_function_lint is implemented using [custom_lint]. As such, it uses custom_lint's installation logic.  
Long story short:
  
- Add both max_lines_function_lint and custom_lint to your `pubspec.yaml`:
  ```yaml
  dev_dependencies:
    custom_lint:
    max_lines_function_lint:
  ```
- Enable `custom_lint`'s plugin in your `analysis_options.yaml`:

  ```yaml
  analyzer:
    plugins:
      - custom_lint
  ```
  
- Re-run in your IDE the analyzer or with command :

  ```sh
  dart analyze
  ```

# Custom limit

Limit the maximum of line with a custom value (default 30)

```yaml
analyzer:
  plugins:
    - custom_lint

custom_lint:
  rules:
    - function_max_lines:
      max_lines: 50
```
