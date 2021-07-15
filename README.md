# Books.jl issue

1. Clone the project.
2. Then `] instantiate` in project's root.
3. Then run `julia --project -e "using Books; serve()"` (on Windows at least).

```bash
booksjldemo>julia --project -e "using Books; serve()"
Watching .\Manifest.toml
Watching .\Project.toml
Watching .\README.md
Watching .\config.toml
Watching .\.git\COMMIT_EDITMSG
Watching .\.git\HEAD
Watching .\.git\config
Watching .\.git\description
Watching .\.git\index
Watching .\.git\hooks\applypatch-msg.sample
Watching .\.git\hooks\commit-msg.sample
Watching .\.git\hooks\fsmonitor-watchman.sample
Watching .\.git\hooks\post-update.sample
Watching .\.git\hooks\pre-applypatch.sample
Watching .\.git\hooks\pre-commit.sample
Watching .\.git\hooks\pre-merge-commit.sample
Watching .\.git\hooks\pre-push.sample
Watching .\.git\hooks\pre-rebase.sample
Watching .\.git\hooks\pre-receive.sample
Watching .\.git\hooks\prepare-commit-msg.sample
Watching .\.git\hooks\push-to-checkout.sample
Watching .\.git\hooks\update.sample
Watching .\.git\info\exclude
Watching .\.git\logs\HEAD
Watching .\.git\logs\refs\heads\master
Watching .\.git\objects\0c\cef9c6a348e14baa6721f1dd27bc7b3f499c0c
Watching .\.git\objects\35\52728b5278dfa4c60e9e639ed0c59e932513cd
Watching .\.git\objects\3f\ae69296005e3cbe04279848cd79b61e432658c
Watching .\.git\objects\7d\2f9932df333e1200ebd430a716e1c4ac40ba53
Watching .\.git\objects\9c\cc63cd947f3c67e1a0f63b1bd4e05765a6cc56
Watching .\.git\objects\aa\b12873f8ac513e31c1b45553193a8d7ad62e0e
Watching .\.git\objects\b9\a70b58acdf368904061ae302ca2c08877ab9ca
Watching .\.git\objects\fd\7368c199781cdf67f607c5b8c71f31dd1c4f14
Watching .\.git\refs\heads\master
Watching .\contents\index.md
Error running filter pandoc-crossref:
Could not find executable pandoc-crossref
ERROR: failed process: Process(`'C:\Users\cstamas\.julia\artifacts\102b684e96a547c8bc1dfa09ec622ffda2f216b5\bin\pandoc.exe' 'contents\index.md' 'contents\index.md' '--lua-filter=C:\Users\cstamas\.julia\packages\Books\5A4k8\src\include-codeblocks.lua' --filter=pandoc-crossref --citeproc --mathjax '--csl=C:\Users\cstamas\.julia\packages\Books\5A4k8\defaults\style.csl' '--metadata-file=_gen\metadata.yml' '--template=C:\Users\cstamas\.julia\packages\Books\5A4k8\defaults\template.html' --number-sections --top-level-division=chapter`, ProcessExited(83)) [83]

Stacktrace:
  [1] pipeline_error
    @ .\process.jl:525 [inlined]
  [2] run(::Base.CmdRedirect; wait::Bool)
    @ Base .\process.jl:440
  [3] run
    @ .\process.jl:438 [inlined]
  [4] (::Books.var"#16#18"{String, Vector{String}})(#unused#::String)
    @ Books C:\Users\cstamas\.julia\packages\Books\5A4k8\src\build.jl:58
  [5] (::JLLWrappers.var"#2#3"{Books.var"#16#18"{String, Vector{String}}, String})()
    @ JLLWrappers C:\Users\cstamas\.julia\packages\JLLWrappers\bkwIo\src\runtime.jl:49
  [6] withenv(f::JLLWrappers.var"#2#3"{Books.var"#16#18"{String, Vector{String}}, String}, keyvals::Pair{String, String})
    @ Base .\env.jl:161
  [7] withenv_executable_wrapper(f::Function, executable_path::String, PATH::String, LIBPATH::String, adjust_PATH::Bool, adjust_LIBPATH::Bool)
    @ JLLWrappers C:\Users\cstamas\.julia\packages\JLLWrappers\bkwIo\src\runtime.jl:48
  [8] invokelatest(::Any, ::Any, ::Vararg{Any, N} where N; kwargs::Base.Iterators.Pairs{Union{}, Union{}, Tuple{}, NamedTuple{(), Tuple{}}})
    @ Base .\essentials.jl:708
  [9] invokelatest(::Any, ::Any, ::Vararg{Any, N} where N)
    @ Base .\essentials.jl:706
 [10] pandoc_crossref(f::Function; adjust_PATH::Bool, adjust_LIBPATH::Bool)
    @ pandoc_crossref_jll C:\Users\cstamas\.julia\packages\JLLWrappers\bkwIo\src\products\executable_generators.jl:7
 [11] pandoc_crossref(f::Function)
    @ pandoc_crossref_jll C:\Users\cstamas\.julia\packages\JLLWrappers\bkwIo\src\products\executable_generators.jl:7
 [12] (::Books.var"#15#17"{Vector{String}})(pandoc_bin::String)
    @ Books C:\Users\cstamas\.julia\packages\Books\5A4k8\src\build.jl:55
 [13] (::JLLWrappers.var"#2#3"{Books.var"#15#17"{Vector{String}}, String})()
    @ JLLWrappers C:\Users\cstamas\.julia\packages\JLLWrappers\bkwIo\src\runtime.jl:49
 [14] withenv(f::JLLWrappers.var"#2#3"{Books.var"#15#17"{Vector{String}}, String}, keyvals::Pair{String, String})
    @ Base .\env.jl:161
 [15] withenv_executable_wrapper(f::Function, executable_path::String, PATH::String, LIBPATH::String, adjust_PATH::Bool, adjust_LIBPATH::Bool)
    @ JLLWrappers C:\Users\cstamas\.julia\packages\JLLWrappers\bkwIo\src\runtime.jl:48
 [16] invokelatest(::Any, ::Any, ::Vararg{Any, N} where N; kwargs::Base.Iterators.Pairs{Union{}, Union{}, Tuple{}, NamedTuple{(), Tuple{}}})
    @ Base .\essentials.jl:708
 [17] invokelatest(::Any, ::Any, ::Vararg{Any, N} where N)
    @ Base .\essentials.jl:706
 [18] pandoc(f::Function; adjust_PATH::Bool, adjust_LIBPATH::Bool)
    @ pandoc_jll C:\Users\cstamas\.julia\packages\JLLWrappers\bkwIo\src\products\executable_generators.jl:7
 [19] pandoc(f::Function)
    @ pandoc_jll C:\Users\cstamas\.julia\packages\JLLWrappers\bkwIo\src\products\executable_generators.jl:7
 [20] call_pandoc(args::Vector{String})
    @ Books C:\Users\cstamas\.julia\packages\Books\5A4k8\src\build.jl:54
 [21] pandoc_html(project::String)
    @ Books C:\Users\cstamas\.julia\packages\Books\5A4k8\src\build.jl:119
 [22] html(; project::String, extra_head::String)
    @ Books C:\Users\cstamas\.julia\packages\Books\5A4k8\src\build.jl:150
 [23] serve(; simplewatcher::Nothing, project::String, verbose::Bool, dir::String)
    @ Books C:\Users\cstamas\.julia\packages\Books\5A4k8\src\serve.jl:61
 [24] serve()
    @ Books C:\Users\cstamas\.julia\packages\Books\5A4k8\src\serve.jl:56
 [25] top-level scope
    @ none:1

```