<!-- Generated with Stardoc: http://skydoc.bazel.build -->


run_binary() build rule implementation.

Runs a binary as a build action. This rule does not require Bash (unlike native.genrule()).


<a id="#run_binary"></a>

## run_binary

<pre>
run_binary(<a href="#run_binary-name">name</a>, <a href="#run_binary-args">args</a>, <a href="#run_binary-env">env</a>, <a href="#run_binary-outs">outs</a>, <a href="#run_binary-srcs">srcs</a>, <a href="#run_binary-tool">tool</a>)
</pre>

Runs a binary as a build action.<br/><br/>This rule does not require Bash (unlike <code>native.genrule</code>).

**ATTRIBUTES**


| Name  | Description | Type | Mandatory | Default |
| :------------- | :------------- | :------------- | :------------- | :------------- |
| <a id="run_binary-name"></a>name |  A unique name for this target.   | <a href="https://bazel.build/docs/build-ref.html#name">Name</a> | required |  |
| <a id="run_binary-args"></a>args |  Command line arguments of the binary.&lt;br/&gt;&lt;br/&gt;Subject to&lt;code&gt;&lt;a href="https://docs.bazel.build/versions/main/be/make-variables.html#location"&gt;$(location)&lt;/a&gt;&lt;/code&gt; expansion.   | List of strings | optional | [] |
| <a id="run_binary-env"></a>env |  Environment variables of the action.&lt;br/&gt;&lt;br/&gt;Subject to  &lt;code&gt;&lt;a href="https://docs.bazel.build/versions/main/be/make-variables.html#location"&gt;$(location)&lt;/a&gt;&lt;/code&gt; expansion.   | <a href="https://bazel.build/docs/skylark/lib/dict.html">Dictionary: String -> String</a> | optional | {} |
| <a id="run_binary-outs"></a>outs |  Output files generated by the action.&lt;br/&gt;&lt;br/&gt;These labels are available for &lt;code&gt;$(location)&lt;/code&gt; expansion in &lt;code&gt;args&lt;/code&gt; and &lt;code&gt;env&lt;/code&gt;.   | List of labels | required |  |
| <a id="run_binary-srcs"></a>srcs |  Additional inputs of the action.&lt;br/&gt;&lt;br/&gt;These labels are available for &lt;code&gt;$(location)&lt;/code&gt; expansion in &lt;code&gt;args&lt;/code&gt; and &lt;code&gt;env&lt;/code&gt;.   | <a href="https://bazel.build/docs/build-ref.html#labels">List of labels</a> | optional | [] |
| <a id="run_binary-tool"></a>tool |  The tool to run in the action.&lt;br/&gt;&lt;br/&gt;Must be the label of a *_binary rule, of a rule that generates an executable file, or of a file that can be executed as a subprocess (e.g. an .exe or .bat file on Windows or a binary with executable permission on Linux). This label is available for &lt;code&gt;$(location)&lt;/code&gt; expansion in &lt;code&gt;args&lt;/code&gt; and &lt;code&gt;env&lt;/code&gt;.   | <a href="https://bazel.build/docs/build-ref.html#labels">Label</a> | required |  |

