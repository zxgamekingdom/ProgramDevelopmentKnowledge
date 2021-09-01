# 预定义参数

ReSharper 中预定义了以下模板参数：
| 预定义参数名  | 说明                                                         |
| ------------- | ------------------------------------------------------------ |
| `$END$`       | 应用模板后的插入符号位置。                                   |
| `$SELECTION$` | 用户在调用模板之前选择的文本。此参数仅用于[环绕声模板](https://www.jetbrains.com/help/resharper/Templates__Applying_Templates__Surrounding_Code_Fragments_with_Templates.html)。 |
| `$SELSTART$`  | 将选择的文本块的起始位置之后在应用模板。                     |
| `$SELEND$`    | 将所选择的文本块的结束位置后在应用模板。                     |

# 模板宏

## 英文

| Expression                                      | Description                                                  | Details                                                      |
| ----------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| `guessElementType()`                            | Guess element type of collection represented by **variable** | Analyzes code and guesses type of element of a collection.Macro parameters:**variable**- reference to another parameter in the template |
| `suggestIndexVariable()`                        | Suggest name for an index variable                           | Suggests non-used name which can be used for an index variable at the evaluation point. |
| `getAlphaNumericFileNameWithoutExtension()`     | Current file name without extension with all non-alphanumeric replaced with underscores | Evaluates current file name without extension with all non-alphanumeric replaced with underscores |
| `getAlphaNumericMainFileNameWithoutExtension()` | Name of the primary file without extension with all non-alphanumeric replaced with underscores | Evaluates primary file name without extension with all non-alphanumeric replaced with underscores |
| `arrayVariable()`                               | Suggest an array variable                                    | Suggests variable which type is array type                   |
| `fixedTypeName()`                               | Insert reference to **type**                                 | Evaluates to the selected type name.Macro parameters:**type**- type |
| `capitalize()`                                  | Value of **another variable** with the first letter in upper case | Capitalizes string value (i.e. changes case of the first letter to upper)Macro parameters:**another variable**- reference to another parameter in the template |
| `clipboard()`                                   | Clipboard content                                            | Evaluates to current textual clipboard content               |
| `complete()`                                    | Execute basic completion                                     | Show basic code completion list at the point where the variable is evaluated |
| `completeSmart()`                               | Execute smart completion                                     | Show smart code completion list at the point where the variable is evaluated |
| `completeType()`                                | Execute type completion                                      | Show type completion list at the point where the variable is evaluated |
| `constant()`                                    | **Constant value**                                           | Evaluates to the specified constant value.Macro parameters:**Constant value**- text string |
| `typeMember()`                                  | Containing type member name                                  | Evaluates to short name of the most inner containing type member (e.g. method or property). |
| `typeName()`                                    | Containing type name                                         | Evaluates to short name of the most inner containing type.   |
| `typeRef()`                                     | Containing type reference                                    | Evaluates to reference of the most inner containing type.    |
| `context()`                                     | Provides list of items describing current context            | Provides list of items describing current context. This includes file name, containing type name, namespace name, etc. |
| `getCreationTime()`                             | Date and time when the file was created in specified **format** | Evaluates file creation date and timeMacro parameters:**format**- text string |
| `getCurrentDate()`                              | Current date in specified **format**                         | Evaluates current dateMacro parameters:**format**- text stringFor more information, see [Standard Date and Time Format Strings](http://msdn.microsoft.com/en-us/library/az4se3k1.aspx). |
| `getCurrentTime()`                              | Current date and time in specified **format**                | Evaluates current dateMacro parameters:**format**- text stringFor more information, see [Standard Date and Time Format Strings](http://msdn.microsoft.com/en-us/library/az4se3k1.aspx). |
| `getCurrentNamespace()`                         | Containing namespace                                         | Evaluates name of the containing namespace                   |
| `decapitalize()`                                | Value of **another variable** with the first character in lower case | Decapitalizes string value (i.e. changes case of the first letter to lower)Macro parameters:**another variable**- reference to another parameter in the template |
| `getDefaultNamespace()`                         | Default namespace                                            | Gets default namespace for the current project               |
| `fileDefaultNamespace()`                        | Default namespace for current file                           | Gets default namespace for the current file                  |
| `getFileName()`                                 | Current file name                                            | Evaluates current file name                                  |
| `getFileNameWithoutExtension()`                 | Current file name without extension                          | Evaluates current file name without extension                |
| `getFullUserName()`                             | Full user name of the current user                           | Evaluates full name of the current user                      |
| `guessExpectedElementType()`                    | Guess element type for expected collection type              | Guess element type if a collection type is expected at this point |
| `guessExpectedType()`                           | Guess type expected at this point                            | Guess type expected at this point                            |
| `guid()`                                        | New GUID                                                     | Generates new Globally Unique Identifier (GUID)              |
| `lineNumber()`                                  | Current line number                                          | Evaluates to number of the line macro is evaluated at.       |
| `list()`                                        | **Comma-delimited list of values**                           | Displays the specified list of values.Macro parameters:**Comma-delimited list of values**- text stringTo add the comma (`,`) as a value to the list, escape it with the backslash (`\`). |
| `getOutputName()`                               | Current project output assembly name                         | Evaluates output assembly name for the current project       |
| `parameterOfType()`                             | Suggest parameter of **type**                                | Suggests parameters of the specified type.Macro parameters:**type**- type |
| `getProjectName()`                              | Name of the current project                                  | Evaluates current project name                               |
| `getSolutionName()`                             | Current solution name                                        | Evaluates current solution name                              |
| `spacestounderstrokes()`                        | Value of **another variable**, where spaces will be replaced with '_' | Changes spaces to '_' (i.e. "do something useful" into "do_something_useful"Macro parameters:**another variable**- reference to another parameter in the template |
| `enumerableVariable()`                          | Suggest enumerable variable                                  | Suggests visible variable that can be enumerated (that is, used in foreach loop as collection) |
| `suggestVariableName()`                         | Suggest name for a variable                                  | When executed in variable declaration (where variable name should stand), suggests name for the variable. |
| `variableOfType()`                              | Suggest variable of **type**                                 | Suggests variables of the specified type.Macro parameters:**type**- type |
| `suggestVariableType()`                         | Suggest type for a new variable                              | Suggest type for a new variable declared in the template     |
| `getUpperCaseAlphaNumericFileName()`            | Current file name in upper case with all non-alphanumeric replaced with underscores | Evaluates current file name in upper case with all non-alphanumeric replaced with underscores |
| `getUserName()`                                 | Short name of the current user                               | Evaluates current user name                                  |
| `dependencyPropertyType()`                      | DependencyProperty type                                      | Evaluates to dependency property type specific to current framework |
| `fullTagName()`                                 | Full tag name                                                | Inserts full name of containing tag                          |
| `suggestXmlAttributeNameByTag()`                | Suggests XML attribute name by tag                           | Suggests XML attribute name used in the same tags in current document |
| `suggestAttributeName()`                        | Suggests XML attribute name                                  | Suggests XML attribute name used in current document         |
| `suggestXmlTagName()`                           | Suggests XML tag name                                        | Suggests XML tag name used in current document               |
| `tagName()`                                     | Tag name                                                     | Inserts name of containing tag without namespace             |
| `tagNamespace()`                                | Tag namespace                                                | Inserts namespace of containing tag                          |
| `castToLeftSideType()`                          | Cast to the required type (if the cast is necessary)         | Inserts (if required) cast to the type which is expected at the left side of assignment expression. |
| `fileheader()`                                  | File header                                                  | Inserts the file header specified in the ReSharper options.  |
| `suggestAttributeNameByTag()`                   | Suggests attribute name by tag                               | Suggests attribute name used in the same tags in current document |
| `suggestAttributeValue()`                       | Suggest attribute value                                      | Suggest attribute value for current html tag attribute       |
| `suggestTagName()`                              | Suggest tag name                                             | Suggest tag name used in current document                    |
| `AspMasterpageContentGenerator()`               | ASP.NET Masterpage content generator                         | Generate content for masterpage content placeholders at the point where the variable is evaluated |
| `AspMvcAction()`                                | ASP.NET MVC Action                                           | Show completion list with available ASP.NET MVC Actions at the point where the variable is evaluated |
| `AspMvcController()`                            | ASP.NET MVC Controller                                       | Show completion list with available ASP.NET MVC Controllers at the point where the variable is evaluated |
| `runAtServer()`                                 | Insert runat="server" if server-side tag selected            | Insert runat="server" if server-side tag selected            |
| `substituteUnrealMacro()`                       | Substitute Unreal template macros                            | Substitute Unreal template macros                            |
| `constTypeName()`                               | Containing type name with const                              | Evaluates to the short name of the most inner containing type with a const specifier. |
| `cppExpandableTemplateNewline()`                | Newline in the documentation and enum-to-string templates    | Evaluates to a newline in the documentation and enum-to-string templates |
| `cppFunctionParameterList()`                    | Containing function parameter list                           | Evaluates to a comma-separated list of the parameter names of the containing function. |
| `cppEnumToStringEnumerator()`                   | Enum to string: enumerator name                              | Duplicates the containing template line for each enumerator and evaluates to the name of the enumerator. |
| `cppEnumToStringEnumeratorName()`               | Enum to string: enumerator name as a string                  | Duplicates the containing template line for each enumerator and evaluates to a string with the name of the enumerator. |
| `cppEnumToStringEnum()`                         | Enum to string: enum name                                    | The name of the enum that the action is invoked on.          |
| `cppFileheader()`                               | File header                                                  | Inserts the file header specified in the ReSharper options.  |
| `cppFunctionParameter()`                        | Documentation: function parameter type with name             | Duplicates the containing template line for each function parameter and evaluates to the parameter type with name |
| `cppFunctionParameterName()`                    | Documentation: function parameter name                       | Duplicates the containing template line for each function parameter and evaluates to the parameter name |
| `cppFunctionParameterType()`                    | Documentation: function parameter type                       | Duplicates the containing template line for each function parameter and evaluates to the parameter type |
| `cppFunctionReturnValue()`                      | Documentation: function return value                         | Keeps the containing template line only if the function return type is non-void |
| `cppTemplateParameterName()`                    | Documentation: template parameter name                       | Duplicates the containing template line for each template parameter and evaluates to the template parameter name |
| `cppMacroParameterName()`                       | Documentation: macro parameter name                          | Duplicates the containing template line for each macro parameter and evaluates to the macro parameter name |
| `cppFunctionReturnType()`                       | Documentation: function return type                          | Evaluates to the function return type                        |
| `cppEntityShortName()`                          | Documentation: entity short name                             | Evaluates to the short name of the entity that is being documented |
| `cppEntityQualifiedName()`                      | Documentation: entity qualified name                         | Evaluates to the qualified name of the entity that is being documented |
| `cppPchIncludeDirective()`                      | Precompiled header file include directive                    | Evaluates to an include directive for the precompiled header file or to an empty string if the project does not use precompiled headers. |

## 中文

| 表达                                            | 描述                                                   | 细节                                                         |
| ----------------------------------------------- | ------------------------------------------------------ | ------------------------------------------------------------ |
| `guessElementType()`                            | 猜测**变量**表示的集合的元素类型                       | 分析代码并猜测集合元素的类型。宏参数：**变量**- 对模板中另一个参数的引用 |
| `suggestIndexVariable()`                        | 索引变量的建议名称                                     | 建议未使用的名称，可用于评估点的索引变量。                   |
| `getAlphaNumericFileNameWithoutExtension()`     | 没有扩展名的当前文件名，所有非字母数字都用下划线替换   | 评估没有扩展名的当前文件名，所有非字母数字都用下划线替换     |
| `getAlphaNumericMainFileNameWithoutExtension()` | 没有扩展名的主文件的名称，所有非字母数字都用下划线替换 | 评估没有扩展名的主文件名，所有非字母数字都用下划线替换       |
| `arrayVariable()`                               | 建议一个数组变量                                       | 建议变量类型是数组类型                                       |
| `fixedTypeName()`                               | 插入对**类型的**引用                                   | 评估选定的类型名称。宏参数：**类型**- 类型                   |
| `capitalize()`                                  | 首字母大写的**另一个变量的**值                         | 大写字符串值（即将第一个字母的大小写更改为大写）宏参数：**另一个变量**- 引用模板中的另一个参数 |
| `clipboard()`                                   | 剪贴板内容                                             | 评估当前文本剪贴板内容                                       |
| `complete()`                                    | 执行基本完成                                           | 在评估变量的地方显示基本代码完成列表                         |
| `completeSmart()`                               | 执行智能完成                                           | 在评估变量的位置显示智能代码完成列表                         |
| `completeType()`                                | 执行类型补全                                           | 在评估变量的位置显示类型完成列表                             |
| `constant()`                                    | **常数值**                                             | 计算为指定的常量值。宏参数：**常量值**- 文本字符串           |
| `typeMember()`                                  | 包含类型成员名称                                       | 计算最内部包含类型成员（例如方法或属性）的短名称。           |
| `typeName()`                                    | 包含类型名称                                           | 计算最内部包含类型的短名称。                                 |
| `typeRef()`                                     | 包含类型引用                                           | 评估最内部包含类型的引用。                                   |
| `context()`                                     | 提供描述当前上下文的项目列表                           | 提供描述当前上下文的项目列表。这包括文件名、包含类型名称、命名空间名称等。 |
| `getCreationTime()`                             | 以指定**格式**创建文件的日期和时间                     | 评估文件创建日期和时间宏参数：**格式**- 文本字符串           |
| `getCurrentDate()`                              | 指定**格式的**当前日期                                 | 评估当前日期宏参数：**格式**- 文本字符串有关更多信息，请参阅[标准日期和时间格式字符串](http://msdn.microsoft.com/en-us/library/az4se3k1.aspx)。 |
| `getCurrentTime()`                              | 指定**格式的**当前日期和时间                           | 评估当前日期宏参数：**格式**- 文本字符串有关更多信息，请参阅[标准日期和时间格式字符串](http://msdn.microsoft.com/en-us/library/az4se3k1.aspx)。 |
| `getCurrentNamespace()`                         | 包含命名空间                                           | 评估包含命名空间的名称                                       |
| `decapitalize()`                                | 第一个字符为小写的**另一个变量的**值                   | 取消大写字符串值（即将第一个字母的大小写更改为小写）宏参数：**另一个变量**- 引用模板中的另一个参数 |
| `getDefaultNamespace()`                         | 默认命名空间                                           | 获取当前项目的默认命名空间                                   |
| `fileDefaultNamespace()`                        | 当前文件的默认命名空间                                 | 获取当前文件的默认命名空间                                   |
| `getFileName()`                                 | 当前文件名                                             | 评估当前文件名                                               |
| `getFileNameWithoutExtension()`                 | 不带扩展名的当前文件名                                 | 评估没有扩展名的当前文件名                                   |
| `getFullUserName()`                             | 当前用户的完整用户名                                   | 评估当前用户的全名                                           |
| `guessExpectedElementType()`                    | 猜测预期集合类型的元素类型                             | 如果此时需要集合类型，请猜测元素类型                         |
| `guessExpectedType()`                           | 此时预期的猜测类型                                     | 此时预期的猜测类型                                           |
| `guid()`                                        | 新的 GUID                                              | 生成新的全局唯一标识符 (GUID)                                |
| `lineNumber()`                                  | 当前行号                                               | 评估到行宏被评估的数量。                                     |
| `list()`                                        | **逗号分隔的值列表**                                   | 显示指定的值列表。宏参数：**逗号分隔的值列表**- 文本字符串要将逗号 ( `,`) 作为值添加到列表中，请使用反斜杠 ( `\`)对其进行转义。 |
| `getOutputName()`                               | 当前项目输出程序集名称                                 | 评估当前项目的输出程序集名称                                 |
| `parameterOfType()`                             | 建议参数**类型**                                       | 建议指定类型的参数。宏参数：**类型**- 类型                   |
| `getProjectName()`                              | 当前项目名称                                           | 评估当前项目名称                                             |
| `getSolutionName()`                             | 当前解决方案名称                                       | 评估当前解决方案名称                                         |
| `spacestounderstrokes()`                        | 价值**另一个变量**，其中的空格将被替换为“_”            | 将空格更改为“_”（即“做一些有用的事情”到“do_something_useful”宏参数：**另一个变量**- 引用模板中的另一个参数 |
| `enumerableVariable()`                          | 建议可枚举变量                                         | 建议可以枚举的可见变量（即在foreach循环中作为集合使用）      |
| `suggestVariableName()`                         | 建议变量名称                                           | 当在变量声明中执行时（变量名应该代表），建议变量的名称。     |
| `variableOfType()`                              | 建议变量**类型**                                       | 建议指定类型的变量。宏参数：**类型**- 类型                   |
| `suggestVariableType()`                         | 建议新变量的类型                                       | 为模板中声明的新变量建议类型                                 |
| `getUpperCaseAlphaNumericFileName()`            | 大写的当前文件名，所有非字母数字都用下划线替换         | 以大写形式评估当前文件名，所有非字母数字都用下划线替换       |
| `getUserName()`                                 | 当前用户的简称                                         | 评估当前用户名                                               |
| `dependencyPropertyType()`                      | 依赖属性类型                                           | 评估特定于当前框架的依赖属性类型                             |
| `fullTagName()`                                 | 完整的标签名称                                         | 插入包含标签的全名                                           |
| `suggestXmlAttributeNameByTag()`                | 按标签建议 XML 属性名称                                | 建议在当前文档中的相同标签中使用的 XML 属性名称              |
| `suggestAttributeName()`                        | 建议 XML 属性名称                                      | 建议在当前文档中使用的 XML 属性名称                          |
| `suggestXmlTagName()`                           | 建议 XML 标签名称                                      | 建议在当前文档中使用的 XML 标记名称                          |
| `tagName()`                                     | 标签名称                                               | 插入没有命名空间的包含标签的名称                             |
| `tagNamespace()`                                | 标签命名空间                                           | 插入包含标签的命名空间                                       |
| `castToLeftSideType()`                          | 强制转换为所需的类型（如果需要强制转换）               | 插入（如果需要）转换为赋值表达式左侧预期的类型。             |
| `fileheader()`                                  | 文件头                                                 | 插入在 ReSharper 选项中指定的文件头。                        |
| `suggestAttributeNameByTag()`                   | 按标签建议属性名称                                     | 建议在当前文档中的相同标签中使用的属性名称                   |
| `suggestAttributeValue()`                       | 建议属性值                                             | 建议当前 html 标签属性的属性值                               |
| `suggestTagName()`                              | 建议标签名称                                           | 建议在当前文档中使用的标签名称                               |
| `AspMasterpageContentGenerator()`               | ASP.NET 母版页内容生成器                               | 在评估变量的位置为母版内容占位符生成内容                     |
| `AspMvcAction()`                                | ASP.NET MVC 操作                                       | 在评估变量的位置显示包含可用 ASP.NET MVC 操作的完成列表      |
| `AspMvcController()`                            | ASP.NET MVC 控制器                                     | 在评估变量的位置显示带有可用 ASP.NET MVC 控制器的完成列表    |
| `runAtServer()`                                 | 如果选择了服务器端标记，则插入 runat="server"          | 如果选择了服务器端标记，则插入 runat="server"                |
| `substituteUnrealMacro()`                       | 替换虚幻模板宏                                         | 替换虚幻模板宏                                               |
| `constTypeName()`                               | 使用 const 包含类型名称                                | 使用 const 说明符计算最内部包含类型的短名称。                |
| `cppExpandableTemplateNewline()`                | 文档和 enum-to-string 模板中的换行符                   | 评估文档和 enum-to-string 模板中的换行符                     |
| `cppFunctionParameterList()`                    | 包含函数参数列表                                       | 计算包含函数的参数名称的逗号分隔列表。                       |
| `cppEnumToStringEnumerator()`                   | 枚举到字符串：枚举器名称                               | 为每个枚举器复制包含模板行并计算为枚举器的名称。             |
| `cppEnumToStringEnumeratorName()`               | 枚举到字符串：枚举器名称作为字符串                     | 复制每个枚举器的包含模板行，并计算为具有枚举器名称的字符串。 |
| `cppEnumToStringEnum()`                         | 枚举到字符串：枚举名称                                 | 调用操作的枚举的名称。                                       |
| `cppFileheader()`                               | 文件头                                                 | 插入在 ReSharper 选项中指定的文件头。                        |
| `cppFunctionParameter()`                        | 文档：带名称的函数参数类型                             | 复制每个函数参数的包含模板行，并计算为具有名称的参数类型     |
| `cppFunctionParameterName()`                    | 文档：函数参数名称                                     | 复制每个函数参数的包含模板行并计算为参数名称                 |
| `cppFunctionParameterType()`                    | 文档：函数参数类型                                     | 复制每个函数参数的包含模板行并计算参数类型                   |
| `cppFunctionReturnValue()`                      | 文档：函数返回值                                       | 仅当函数返回类型为非空时才保留包含模板行                     |
| `cppTemplateParameterName()`                    | 文档：模板参数名称                                     | 复制每个模板参数的包含模板行并计算为模板参数名称             |
| `cppMacroParameterName()`                       | 文档：宏参数名称                                       | 复制每个宏参数的包含模板行并计算为宏参数名称                 |
| `cppFunctionReturnType()`                       | 文档：函数返回类型                                     | 评估函数返回类型                                             |
| `cppEntityShortName()`                          | 文档：实体短名称                                       | 评估正在记录的实体的短名称                                   |
| `cppEntityQualifiedName()`                      | 文档：实体限定名称                                     | 评估正在记录的实体的限定名称                                 |
| `cppPchIncludeDirective()`                      | 预编译头文件包含指令                                   | 如果项目不使用预编译头文件，则计算为包含指令的预编译头文件或空字符串。 |

## 中英文

|                           英文描述                           |                        中文描述                        |                     表达式                      |                             细节                             |
| :----------------------------------------------------------: | :----------------------------------------------------: | :---------------------------------------------: | :----------------------------------------------------------: |
| Guess element type of collection represented by **variable** |            猜测**变量**表示的集合的元素类型            |              `guessElementType()`               | 分析代码并猜测集合元素的类型。宏参数：**变量**- 对模板中另一个参数的引用 |
|              Suggest name for an index variable              |                   索引变量的建议名称                   |            `suggestIndexVariable()`             |          建议未使用的名称，可用于评估点的索引变量。          |
| Current file name without extension with all non-alphanumeric replaced with underscores | 没有扩展名的当前文件名，所有非 字母数字都用下划线替换  |   `getAlphaNumericFileNameWithoutExtension()`   |  评估没有扩展名的当前文件名，所有非字母数字都用下划线 替换   |
| Name of the primary file without extension with all non-alphanumeric replaced with underscores | 没有扩展名的主文件的名称，所有非字母数字都用下划线替换 | `getAlphaNumericMainFileNameWithoutExtension()` |   评估没有扩展名的主文件名，所有非字母数字 都用下划线替换    |
|                  Suggest an array variable                   |                    建议一个数组变量                    |                `arrayVariable()`                |                    建议变量类型是数组类型                    |
|                 Insert reference to **type**                 |                  插入对**类型的**引用                  |                `fixedTypeName()`                |          评估选定的类型名称。宏参数：**类型**- 类型          |
| Value of **another variable** with the first letter in upper case |             首字母大写的**另一个变量的**值             |                 `capitalize()`                  | 大写字 符串值（即将第一个字母的大小写更改为大写）宏参数：**另一个变量**- 引用模板中的另一个参数 |
|                      Clipboard content                       |                       剪贴板内容                       |                  `clipboard()`                  |                    评估当前文本剪贴板内容                    |
|                   Execute basic completion                   |                      执行基本完成                      |                  `complete()`                   |             在评估变量的地方显示基本代码完成列表             |
|                   Execute smart completion                   |                      执行智能完成                      |                `completeSmart()`                |             在评估变量的位置显示智能代码完成列表             |
|                   Execute type completion                    |                      执行类型补全                      |                `completeType()`                 |               在评估变量的位置显示类型完成列表               |
|                      **Constant value**                      |                       **常数值**                       |                  `constant()`                   |      计算为指定的常量值。宏参数：**常量值**- 文本字符串      |
|                 Containing type member name                  |                    包含类型成员名称                    |                 `typeMember()`                  |      计算最内部包含类型成员（例如方法或属性）的短名称。      |
|                     Containing type name                     |                      包含类型名称                      |                  `typeName()`                   |                 计算最内部包含类型的短名称。                 |
|                  Containing type reference                   |                      包含类型引用                      |                   `typeRef()`                   |                  评估最内部包含类型的引用。                  |
|      Provides list of items describing current context       |              提供描述当前上下文的项目列表              |                   `context()`                   | 提供描述当前上下文的项目列表。这包括文件名、包含类型名称、命名空间名称等。 |
| Date and time when the file was created in specified **format** |           以指定**格式**创建文件的日期和时间           |               `getCreationTime()`               |      评估文件创建日期和时间宏参数：**格式**- 文本字符串      |
|             Current date in specified **format**             |                 指定**格式的**当前日期                 |               `getCurrentDate()`                | 评估当前日期宏参数：**格式**- 文本字符串有关更多信息，请参阅[标准日期和时间格式字符串](http://msdn.microsoft.com/en-us/library/az4se3k1.aspx)。 |
|        Current date and time in specified **format**         |              指定**格式的**当前日期和时间              |               `getCurrentTime()`                | 评估当前日期宏参数：**格 式**- 文本字符串有关更多信息，请参阅[标准日期和时间格式字符串](http://msdn.microsoft.com/en-us/library/az4se3k1.aspx)。 |
|                     Containing namespace                     |                      包含命名空间                      |             `getCurrentNamespace()`             |                    评估包含命名空间的名称                    |
| Value of **another variable** with the first character in lower case |          第一个字符为小写的**另一个变量的**值          |                `decapitalize()`                 | 取消大写字符串值（即将第一个字母的大小写更改为小写）宏参数：**另一个变量**- 引用模板中的另一个参数 |
|                      Default namespace                       |                      默认命名空间                      |             `getDefaultNamespace()`             |                  获取当前项目的默认命名空间                  |
|              Default namespace for current file              |                 当前文件的默认命名空间                 |            `fileDefaultNamespace()`             |                  获取当前文件的默认命名空间                  |
|                      Current file name                       |                       当前文件名                       |                 `getFileName()`                 |                        评估当前文件名                        |
|             Current file name without extension              |                 不带扩展名的当前文件名                 |         `getFileNameWithoutExtension()`         |                  评估没有扩展名的当前文件名                  |
|              Full user name of the current user              |                  当前用户的完整用户名                  |               `getFullUserName()`               |                      评估当前用户的全名                      |
|       Guess element type for expected collection type        |               猜测预期集合类型的元素类型               |          `guessExpectedElementType()`           |            如果此时需要集 合类型，请猜测元素类型             |
|              Guess type expected at this point               |                   此时预期的猜测类型                   |              `guessExpectedType()`              |                      此时预期的猜测类型                      |
|                           New GUID                           |                       新的 GUID                        |                    `guid()`                     |                生成新的全局唯一标识符 (GUID)                 |
|                     Current line number                      |                        当前行号                        |                 `lineNumber()`                  |                   评估到行宏被评估的数量。                   |
|              **Comma-delimited list of values**              |                  **逗号分隔的值列表**                  |                    `list()`                     | 显示指定的值列表。宏参数：**逗号分隔的值列表**- 文本字符串要将逗号 ( `,`) 作为值添加到列表中，请使用反斜杠 ( `\`)对其进行转义。 |
|             Current project output assembly name             |                 当前项目输出程序集名称                 |                `getOutputName()`                |                 评估当前项目的输出程序集名称                 |
|                Suggest parameter of **type**                 |                    建议参数**类型**                    |               `parameterOfType()`               |          建议指定类型的参数。宏参数：**类型**- 类型          |
|                 Name of the current project                  |                      当前项目名称                      |               `getProjectName()`                |                       评估当前项目名称                       |
|                    Current solution name                     |                    当前解决方案名称                    |               `getSolutionName()`               |                     评估当前解决方案名称                     |
| Value of **another variable**, where spaces will be replaced with '_' |      价值**另一个变量**，其中的空格将被替换为“_”       |            `spacestounderstrokes()`             | 将空格更改为“_”（即“做一些有用的事情”到“do_something_useful”宏参数：**另一个变量**- 引用模板中的另一个参数 |
|                 Suggest enumerable variable                  |                     建议可枚举变量                     |             `enumerableVariable()`              |   建议可以枚举的可见变量（即在foreach循环中作为集合使用）    |
|                 Suggest name for a variable                  |                      建议变量名称                      |             `suggestVariableName()`             |   当在变量声明中执行时（变量名应该代表），建议变量的名称。   |
|                 Suggest variable of **type**                 |                    建议变量**类型**                    |               `variableOfType()`                |          建议指定类型的变量。宏参数：**类型**- 类型          |
|               Suggest type for a new variable                |                    建议新变量的类型                    |             `suggestVariableType()`             |                 为模板中声明的新变量建议类型                 |
| Current file name in upper case with all non-alphanumeric replaced with underscores |    大写的当前文件名，所有非字母数字都 用下划线替换     |      `getUpperCaseAlphaNumericFileName()`       |    以大写形式评估当前文件名，所有非字母数字都用下划线替换    |
|                Short name of the current user                |                     当前用户的简称                     |                 `getUserName()`                 |                        评估当前用户名                        |
|                   DependencyProperty type                    |                      依赖属性类型                      |           `dependencyPropertyType()`            |               评估特定于当前框架的依赖属性类型               |
|                        Full tag name                         |                     完整的标签名称                     |                 `fullTagName()`                 |                      插入包含标签的全名                      |
|              Suggests XML attribute name by tag              |                按标签建议 XML 属性名称                 |        `suggestXmlAttributeNameByTag()`         |       建议在当前文档中的相同标签 中使用的 XML 属性名称       |
|                 Suggests XML attribute name                  |                   建议 XML 属性名称                    |            `suggestAttributeName()`             |             建议在当前文档中使用的 XML 属性名称              |
|                    Suggests XML tag name                     |                   建议 XML 标签名称                    |              `suggestXmlTagName()`              |             建议在当前文档中使用的 XML 标记名称              |
|                           Tag name                           |                        标签名称                        |                   `tagName()`                   |               插入没有命名空间的包含标签的名称               |
|                        Tag namespace                         |                      标签命名空间                      |                `tagNamespace()`                 |                    插入包含标签的命名空间                    |
|     Cast to the required type (if the cast is necessary)     |        强制转换为所需的类型（如果需要强制转换）        |             `castToLeftSideType()`              |       插入（如果需要）转换为赋值表达式左侧预期的类型。       |
|                         File header                          |                         文件头                         |                 `fileheader()`                  |            插入在 ReSharper 选项中指定的文件头。             |
|                Suggests attribute name by tag                |                   按标签建议属性名称                   |          `suggestAttributeNameByTag()`          |         建议在当前文档中的相同标签中使用的属性 名称          |
|                   Suggest attribute value                    |                       建议属性值                       |            `suggestAttributeValue()`            |                建议当前 html 标签属性的属性值                |
|                       Suggest tag name                       |                      建议标签名称                      |               `suggestTagName()`                |                建议在当前文档中使用的标签名称                |
|             ASP.NET Masterpage content generator             |                ASP.NET 母版页内容生成器                |        `AspMasterpageContentGenerator()`        |          在评估变量的位置为母版 内容占位符生成内容           |
|                      ASP.NET MVC Action                      |                    ASP.NET MVC 操作                    |                `AspMvcAction()`                 |   在评估变量的位置显示包含可用 ASP.NET MVC 操作的完成列表    |
|                    ASP.NET MVC Controller                    |                   ASP.NET MVC 控制器                   |              `AspMvcController()`               |  在评估变量的位置显示带有可用 ASP.NET MVC 控制器的完成列 表  |
|      Insert runat="server" if server-side tag selected       |     如果选择了服务器端标记，则插入 runat="server"      |                 `runAtServer()`                 |        如果选 择了服务器端标记，则插入 runat="server"        |
|              Substitute Unreal template macros               |                     替换虚幻模板宏                     |            `substituteUnrealMacro()`            |                        替换虚幻模板宏                        |
|               Containing type name with const                |                使用 const 包含类型名称                 |                `constTypeName()`                |        使用 const 说明符计算最内部包含类型的短名称。         |
|  Newline in the documentation and enum-to-string templates   |          文档和 enum-to-string 模板中的换行符          |        `cppExpandableTemplateNewline()`         |           评估文档和 enum-to-string 模板中的换行符           |
|              Containing function parameter list              |                    包含函数参数列表                    |          `cppFunctionParameterList()`           |            计算包含函数的参数名称的逗号分隔列表。            |
|               Enum to string: enumerator name                |                枚举到字符串：枚举器名称                |          `cppEnumToStringEnumerator()`          |       为每个枚举器复制包含模板行并计算为枚举器的名称。       |
|         Enum to string: enumerator name as a string          |           枚举到字符串：枚举器名称作为字符串           |        `cppEnumToStringEnumeratorName()`        | 复制每个枚举器的包含模板行，并计算为具有枚举器名称的字符串。 |
|                  Enum to string: enum name                   |                 枚举到字符串：枚举名称                 |             `cppEnumToStringEnum()`             |                    调用操作的枚举的名称。                    |
|                         File header                          |                         文件头                         |                `cppFileheader()`                |            插入在 ReSharper 选项中指定的文件头。             |
|       Documentation: function parameter type with name       |               文档：带名称的函数参数类型               |            `cppFunctionParameter()`             |   复制每个函数参数的包含模板行，并计算为具有名称的参数类型   |
|            Documentation: function parameter name            |                   文档：函数参数名称                   |          `cppFunctionParameterName()`           |         复制每个函数参数的包含模板行并计算为参数名称         |
|            Documentation: function parameter type            |                   文档：函数参数类型                   |          `cppFunctionParameterType()`           |          复制每个函数参数的包含模板行并计算参数类型          |
|             Documentation: function return value             |                    文档：函数返回值                    |           `cppFunctionReturnValue()`            |           仅当函数返回类型为非空时才保留包含模板行           |
|            Documentation: template parameter name            |                   文档：模板参数名称                   |          `cppTemplateParameterName()`           |       复制每个模板参数的包含模板行并计算为模板参数名称       |
|             Documentation: macro parameter name              |                    文档：宏参数名称                    |            `cppMacroParameterName()`            |         复制每个宏参数的包含模板行并计算为宏参数名称         |
|             Documentation: function return type              |                   文档：函数返回类型                   |            `cppFunctionReturnType()`            |                       评估函数返回类型                       |
|               Documentation: entity short name               |                    文档：实体短名称                    |             `cppEntityShortName()`              |                  评估正在记录的实体的短名称                  |
|             Documentation: entity qualified name             |                   文档：实体限定名称                   |           `cppEntityQualifiedName()`            |                 评估正在记录的实体的限定名称                 |
|          Precompiled header file include directive           |                  预编译头文件包含指令                  |           `cppPchIncludeDirective()`            | 如果项目不使用预编译头文件， 则计算为包含指令的预编译头文件或空字符串。 |

