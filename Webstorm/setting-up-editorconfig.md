# Setting up .editorconfig file

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

* root = true : A search for .editorconfig files will stop if the root file path is reached or an EditorConfig file with root = true is found.

### References
* [Webstorm: Configuring Code Style](https://www.jetbrains.com/help/webstorm/2016.2/configuring-code-style.html)
* [EditorConfig Website](http://editorconfig.org/)