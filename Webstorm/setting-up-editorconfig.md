# Setting up .editorconfig file
EditorConfig helps developers define and maintain consistent coding styles between different editors and IDEs.

### My setting
    root = true

    [*]
    indent_style = space
    indent_size = 2
    end_of_line = lf
    charset = utf-8
    trim_trailing_whitespace = true
    insert_final_newline = true

    [*.md]
    trim_trailing_whitespace = false

### References
* [Webstorm: Configuring Code Style](https://www.jetbrains.com/help/webstorm/2016.2/configuring-code-style.html)
* [EditorConfig Website](http://editorconfig.org/)