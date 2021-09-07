# @NotNull with primitive types

Annotation `@NotNull` doesn't work with primitive types in Spring so, for example, instead of `int` we should use `Integer` because if this field is blank or has white spaces it will be trimmed to `null`.

<hr>

[Return](../../../)