# Clangd

I[20:14:39.112] clangd version 17.0.3 (https://github.com/llvm/llvm-project 888437e1b60011b8a375dd30928ec925b448da57)
I[20:14:39.113] Features: windows+grpc
I[20:14:39.113] PID: 28816
I[20:14:39.113] Working directory: d:\CS\竞赛\服创赛\文档
I[20:14:39.113] argv[0]: c:\Users\Shelly\AppData\Roaming\Code\User\globalStorage\llvm-vs-code-extensions.vscode-clangd\install\17.0.3\clangd_17.0.3\bin\clangd.exe
I[20:14:39.119] Starting LSP over stdin/stdout
I[20:14:39.431] <-- initialize(0)
I[20:14:39.476] --> reply:initialize(0) 45 ms
I[20:14:39.541] <-- initialized
I[20:14:39.553] <-- textDocument/didOpen
I[20:14:39.556] <-- textDocument/documentLink(1)
I[20:14:39.557] <-- textDocument/inlayHint(2)
I[20:14:39.557] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:39.557] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 1 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:39.621] --> textDocument/clangd.fileStatus
I[20:14:39.638] Built preamble of size 233300 for file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 1 in 0.02 seconds
I[20:14:39.641] --> workspace/semanticTokens/refresh(0)
I[20:14:39.641] --> textDocument/clangd.fileStatus
I[20:14:39.643] <-- reply(0)
I[20:14:39.644] <-- textDocument/semanticTokens/full(3)
I[20:14:39.645] Indexing c++14 standard library in the context of d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:39.667] <-- $/cancelRequest
I[20:14:39.673] --> textDocument/publishDiagnostics
I[20:14:39.673] --> textDocument/inactiveRegions
I[20:14:39.674] --> reply:textDocument/documentLink(1) 117 ms, error: Task was cancelled.
I[20:14:39.674] --> reply:textDocument/inlayHint(2) 117 ms
I[20:14:39.674] --> reply:textDocument/semanticTokens/full(3) 30 ms
I[20:14:39.674] --> textDocument/clangd.fileStatus
I[20:14:40.043] <-- textDocument/documentLink(4)
I[20:14:40.043] --> reply:textDocument/documentLink(4) 0 ms
I[20:14:40.043] --> textDocument/clangd.fileStatus
[Error - 20:14:40] Request textDocument/documentLink failed.
[object Object]
I[20:14:40.067] <-- textDocument/foldingRange(5)
I[20:14:40.068] --> reply:textDocument/foldingRange(5) 0 ms
I[20:14:40.069] <-- textDocument/documentSymbol(6)
I[20:14:40.069] --> reply:textDocument/documentSymbol(6) 0 ms
I[20:14:40.069] --> textDocument/clangd.fileStatus
I[20:14:41.107] Indexed c++14 standard library (incomplete due to errors): 12107 symbols, 1167 filtered
I[20:14:43.555] <-- textDocument/didChange
I[20:14:43.555] --> textDocument/clangd.fileStatus
I[20:14:43.610] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:43.611] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 2 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:43.612] <-- textDocument/completion(7)
I[20:14:43.619] --> textDocument/clangd.fileStatus
I[20:14:43.633] Built preamble of size 233300 for file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 2 in 0.01 seconds
I[20:14:43.633] --> workspace/semanticTokens/refresh(1)
I[20:14:43.634] <-- reply(1)
I[20:14:43.635] <-- textDocument/semanticTokens/full/delta(8)
I[20:14:43.644] Code complete: sema context TopLevel, query scopes [] (AnyScope=true), expected type <none>
I[20:14:43.644] Code complete: 0 results from Sema, 0 from Index, 0 matched, 0 from identifiers, 0 returned (incomplete).
I[20:14:43.644] --> reply:textDocument/completion(7) 31 ms
I[20:14:43.644] --> textDocument/publishDiagnostics
I[20:14:43.644] --> textDocument/inactiveRegions
I[20:14:43.668] --> textDocument/publishDiagnostics
I[20:14:43.668] --> textDocument/inactiveRegions
I[20:14:43.668] --> reply:textDocument/semanticTokens/full/delta(8) 32 ms
I[20:14:43.668] --> textDocument/clangd.fileStatus
I[20:14:43.876] <-- textDocument/foldingRange(9)
I[20:14:43.876] --> reply:textDocument/foldingRange(9) 0 ms
I[20:14:43.925] <-- textDocument/codeAction(10)
I[20:14:43.925] --> reply:textDocument/codeAction(10) 0 ms
I[20:14:43.925] --> textDocument/clangd.fileStatus
I[20:14:44.093] <-- textDocument/documentSymbol(11)
I[20:14:44.093] --> reply:textDocument/documentSymbol(11) 0 ms
I[20:14:44.093] --> textDocument/clangd.fileStatus
I[20:14:44.156] <-- textDocument/didChange
I[20:14:44.156] --> textDocument/clangd.fileStatus
I[20:14:44.218] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:44.218] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 3 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:44.230] --> textDocument/clangd.fileStatus
I[20:14:44.242] Built preamble of size 233300 for file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 3 in 0.01 seconds
I[20:14:44.242] --> workspace/semanticTokens/refresh(2)
I[20:14:44.243] <-- reply(2)
I[20:14:44.244] <-- textDocument/semanticTokens/full/delta(12)
I[20:14:44.254] --> textDocument/publishDiagnostics
I[20:14:44.254] --> textDocument/inactiveRegions
I[20:14:44.277] --> textDocument/publishDiagnostics
I[20:14:44.277] --> textDocument/inactiveRegions
I[20:14:44.277] --> reply:textDocument/semanticTokens/full/delta(12) 33 ms
I[20:14:44.277] --> textDocument/clangd.fileStatus
I[20:14:44.414] <-- textDocument/didChange
I[20:14:44.414] --> textDocument/clangd.fileStatus
I[20:14:44.466] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:44.466] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 4 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:44.476] --> textDocument/clangd.fileStatus
I[20:14:44.488] Built preamble of size 233300 for file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 4 in 0.01 seconds
I[20:14:44.488] --> workspace/semanticTokens/refresh(3)
I[20:14:44.500] --> textDocument/publishDiagnostics
I[20:14:44.500] --> textDocument/inactiveRegions
I[20:14:44.507] <-- reply(3)
I[20:14:44.508] <-- textDocument/semanticTokens/full/delta(13)
I[20:14:44.524] --> textDocument/publishDiagnostics
I[20:14:44.524] --> textDocument/inactiveRegions
I[20:14:44.524] --> reply:textDocument/semanticTokens/full/delta(13) 16 ms
I[20:14:44.524] --> textDocument/clangd.fileStatus
I[20:14:44.669] <-- textDocument/codeAction(14)
I[20:14:44.671] --> reply:textDocument/codeAction(14) 1 ms
I[20:14:44.671] --> textDocument/clangd.fileStatus
I[20:14:44.715] <-- textDocument/foldingRange(15)
I[20:14:44.715] --> reply:textDocument/foldingRange(15) 0 ms
I[20:14:44.764] <-- textDocument/didChange
I[20:14:44.764] --> textDocument/clangd.fileStatus
I[20:14:44.780] <-- textDocument/completion(16)
I[20:14:44.810] Code complete: sema context PreprocessorDirective, query scopes [] (AnyScope=true), expected type <none>
I[20:14:44.811] Code complete: 7 results from Sema, 0 from Index, 0 matched, 0 from identifiers, 7 returned.
I[20:14:44.811] --> reply:textDocument/completion(16) 31 ms
I[20:14:44.823] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:44.823] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 5 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:44.833] --> textDocument/clangd.fileStatus
I[20:14:44.856] --> textDocument/publishDiagnostics
I[20:14:44.856] --> textDocument/inactiveRegions
I[20:14:44.856] --> textDocument/clangd.fileStatus
I[20:14:44.996] <-- textDocument/didChange
I[20:14:44.997] --> textDocument/clangd.fileStatus
I[20:14:44.997] <-- textDocument/completion(17)
I[20:14:45.028] Code complete: sema context PreprocessorDirective, query scopes [] (AnyScope=true), expected type <none>
I[20:14:45.028] Code complete: 4 results from Sema, 0 from Index, 0 matched, 0 from identifiers, 4 returned.
I[20:14:45.028] --> reply:textDocument/completion(17) 31 ms
I[20:14:45.057] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:45.057] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 6 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:45.069] --> textDocument/clangd.fileStatus
I[20:14:45.091] --> textDocument/publishDiagnostics
I[20:14:45.091] --> textDocument/inactiveRegions
I[20:14:45.091] --> textDocument/clangd.fileStatus
I[20:14:45.213] <-- textDocument/semanticTokens/full/delta(18)
I[20:14:45.213] --> reply:textDocument/semanticTokens/full/delta(18) 0 ms
I[20:14:45.213] --> textDocument/clangd.fileStatus
I[20:14:45.293] <-- textDocument/didChange
I[20:14:45.293] --> textDocument/clangd.fileStatus
I[20:14:45.293] <-- textDocument/completion(19)
I[20:14:45.324] Code complete: sema context PreprocessorDirective, query scopes [] (AnyScope=true), expected type <none>
I[20:14:45.324] Code complete: 4 results from Sema, 0 from Index, 0 matched, 0 from identifiers, 4 returned.
I[20:14:45.324] --> reply:textDocument/completion(19) 30 ms
I[20:14:45.353] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:45.353] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 7 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:45.364] --> textDocument/clangd.fileStatus
I[20:14:45.387] --> textDocument/publishDiagnostics
I[20:14:45.387] --> textDocument/inactiveRegions
I[20:14:45.387] --> textDocument/clangd.fileStatus
I[20:14:45.462] <-- textDocument/didChange
I[20:14:45.462] --> textDocument/clangd.fileStatus
I[20:14:45.462] <-- textDocument/completion(20)
I[20:14:45.493] Code complete: sema context PreprocessorDirective, query scopes [] (AnyScope=true), expected type <none>
I[20:14:45.493] Code complete: 4 results from Sema, 0 from Index, 0 matched, 0 from identifiers, 4 returned.
I[20:14:45.494] --> reply:textDocument/completion(20) 31 ms
I[20:14:45.526] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:45.527] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 8 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:45.537] --> textDocument/clangd.fileStatus
I[20:14:45.560] --> textDocument/publishDiagnostics
I[20:14:45.560] --> textDocument/inactiveRegions
I[20:14:45.560] --> textDocument/clangd.fileStatus
I[20:14:45.668] <-- textDocument/didChange
I[20:14:45.668] --> textDocument/clangd.fileStatus
I[20:14:45.668] <-- textDocument/completion(21)
I[20:14:45.699] Code complete: sema context PreprocessorDirective, query scopes [] (AnyScope=true), expected type <none>
I[20:14:45.699] Code complete: 4 results from Sema, 0 from Index, 0 matched, 0 from identifiers, 4 returned.
I[20:14:45.699] --> reply:textDocument/completion(21) 30 ms
I[20:14:45.728] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:45.728] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 9 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:45.740] --> textDocument/clangd.fileStatus
I[20:14:45.745] <-- textDocument/semanticTokens/full/delta(22)
I[20:14:45.761] --> textDocument/publishDiagnostics
I[20:14:45.762] --> textDocument/inactiveRegions
I[20:14:45.762] --> reply:textDocument/semanticTokens/full/delta(22) 16 ms
I[20:14:45.762] --> textDocument/clangd.fileStatus
I[20:14:46.049] <-- textDocument/foldingRange(23)
I[20:14:46.049] --> reply:textDocument/foldingRange(23) 0 ms
I[20:14:46.050] <-- textDocument/codeAction(24)
I[20:14:46.050] --> reply:textDocument/codeAction(24) 0 ms
I[20:14:46.050] --> textDocument/clangd.fileStatus
I[20:14:46.202] <-- textDocument/documentSymbol(25)
I[20:14:46.202] --> reply:textDocument/documentSymbol(25) 0 ms
I[20:14:46.202] --> textDocument/clangd.fileStatus
I[20:14:46.623] <-- textDocument/didChange
I[20:14:46.623] --> textDocument/clangd.fileStatus
I[20:14:46.684] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:46.684] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 10 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:46.695] --> textDocument/clangd.fileStatus
I[20:14:46.707] Built preamble of size 233312 for file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 10 in 0.01 seconds
I[20:14:46.707] --> workspace/semanticTokens/refresh(4)
I[20:14:46.708] <-- reply(4)
I[20:14:46.709] <-- textDocument/semanticTokens/full/delta(26)
I[20:14:46.716] --> textDocument/publishDiagnostics
I[20:14:46.716] --> textDocument/inactiveRegions
I[20:14:46.739] --> textDocument/publishDiagnostics
I[20:14:46.739] --> textDocument/inactiveRegions
I[20:14:46.739] --> reply:textDocument/semanticTokens/full/delta(26) 30 ms
I[20:14:46.739] --> textDocument/clangd.fileStatus
I[20:14:46.933] <-- textDocument/foldingRange(27)
I[20:14:46.933] --> reply:textDocument/foldingRange(27) 0 ms
I[20:14:47.011] <-- textDocument/codeAction(28)
I[20:14:47.011] --> reply:textDocument/codeAction(28) 0 ms
I[20:14:47.011] --> textDocument/clangd.fileStatus
I[20:14:47.150] <-- textDocument/documentSymbol(29)
I[20:14:47.150] --> reply:textDocument/documentSymbol(29) 0 ms
I[20:14:47.150] --> textDocument/clangd.fileStatus
I[20:14:47.655] <-- textDocument/didSave
I[20:14:47.655] File version went from 10 to 10
I[20:14:47.655] --> textDocument/clangd.fileStatus
I[20:14:47.668] <-- textDocument/didChange
I[20:14:47.668] --> textDocument/clangd.fileStatus
I[20:14:47.727] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:47.728] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 11 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:47.740] --> textDocument/clangd.fileStatus
I[20:14:47.753] Built preamble of size 233312 for file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 11 in 0.01 seconds
I[20:14:47.753] --> workspace/semanticTokens/refresh(5)
I[20:14:47.754] <-- reply(5)
I[20:14:47.754] <-- textDocument/semanticTokens/full/delta(30)
I[20:14:47.763] --> textDocument/publishDiagnostics
I[20:14:47.763] --> textDocument/inactiveRegions
I[20:14:47.785] --> textDocument/publishDiagnostics
I[20:14:47.785] --> textDocument/inactiveRegions
I[20:14:47.785] --> reply:textDocument/semanticTokens/full/delta(30) 31 ms
I[20:14:47.786] --> textDocument/clangd.fileStatus
I[20:14:47.978] <-- textDocument/foldingRange(31)
I[20:14:47.978] --> reply:textDocument/foldingRange(31) 0 ms
I[20:14:48.092] <-- textDocument/didChange
I[20:14:48.092] --> textDocument/clangd.fileStatus
I[20:14:48.093] <-- textDocument/completion(32)
I[20:14:48.148] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:48.148] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 12 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:48.160] Code complete: sema context IncludedFile, query scopes [] (AnyScope=true), expected type <none>
I[20:14:48.160] Code complete: 2680 results from Sema, 0 from Index, 0 matched, 0 from identifiers, 100 returned (incomplete).
I[20:14:48.162] --> textDocument/clangd.fileStatus
I[20:14:48.164] --> reply:textDocument/completion(32) 70 ms
I[20:14:48.174] Built preamble of size 233312 for file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 12 in 0.01 seconds
I[20:14:48.175] --> workspace/semanticTokens/refresh(6)
I[20:14:48.186] --> textDocument/publishDiagnostics
I[20:14:48.186] --> textDocument/inactiveRegions
I[20:14:48.199] <-- reply(6)
I[20:14:48.210] --> textDocument/publishDiagnostics
I[20:14:48.210] --> textDocument/inactiveRegions
I[20:14:48.210] --> textDocument/clangd.fileStatus
I[20:14:48.214] <-- textDocument/semanticTokens/full/delta(33)
I[20:14:48.214] --> reply:textDocument/semanticTokens/full/delta(33) 0 ms
I[20:14:48.214] --> textDocument/clangd.fileStatus
I[20:14:48.215] <-- textDocument/signatureHelp(34)
I[20:14:48.250] --> reply:textDocument/signatureHelp(34) 34 ms
I[20:14:48.399] <-- textDocument/foldingRange(35)
I[20:14:48.400] --> reply:textDocument/foldingRange(35) 0 ms
I[20:14:48.429] <-- textDocument/didChange
I[20:14:48.429] --> textDocument/clangd.fileStatus
I[20:14:48.429] <-- textDocument/completion(36)
I[20:14:48.469] Code complete: sema context IncludedFile, query scopes [] (AnyScope=true), expected type <none>
I[20:14:48.470] Code complete: 262 results from Sema, 0 from Index, 0 matched, 0 from identifiers, 100 returned (incomplete).
I[20:14:48.473] --> reply:textDocument/completion(36) 43 ms
I[20:14:48.493] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:48.493] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 13 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:48.503] --> textDocument/clangd.fileStatus
I[20:14:48.515] Built preamble of size 233312 for file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 13 in 0.01 seconds
I[20:14:48.515] --> workspace/semanticTokens/refresh(7)
I[20:14:48.516] <-- reply(7)
I[20:14:48.517] <-- textDocument/semanticTokens/full/delta(37)
I[20:14:48.526] --> textDocument/publishDiagnostics
I[20:14:48.526] --> textDocument/inactiveRegions
I[20:14:48.549] --> textDocument/publishDiagnostics
I[20:14:48.549] --> textDocument/inactiveRegions
I[20:14:48.549] --> reply:textDocument/semanticTokens/full/delta(37) 32 ms
I[20:14:48.549] --> textDocument/clangd.fileStatus
I[20:14:48.596] <-- textDocument/didChange
I[20:14:48.596] --> textDocument/clangd.fileStatus
I[20:14:48.596] <-- textDocument/completion(38)
I[20:14:48.633] Code complete: sema context IncludedFile, query scopes [] (AnyScope=true), expected type <none>
I[20:14:48.634] Code complete: 14 results from Sema, 0 from Index, 0 matched, 0 from identifiers, 14 returned.
I[20:14:48.634] --> reply:textDocument/completion(38) 37 ms
I[20:14:48.648] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:48.648] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 14 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:48.658] --> textDocument/clangd.fileStatus
I[20:14:48.676] <-- textDocument/didChange
I[20:14:48.677] <-- textDocument/completion(39)
I[20:14:48.681] --> textDocument/clangd.fileStatus
I[20:14:48.681] Built preamble of size 233316 for file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 14 in 0.02 seconds
I[20:14:48.681] --> workspace/semanticTokens/refresh(8)
I[20:14:48.681] --> textDocument/publishDiagnostics
I[20:14:48.681] --> textDocument/inactiveRegions
I[20:14:48.682] <-- reply(8)
I[20:14:48.684] <-- textDocument/semanticTokens/full/delta(40)
I[20:14:48.704] --> textDocument/publishDiagnostics
I[20:14:48.704] --> textDocument/inactiveRegions
I[20:14:48.704] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:48.704] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 15 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:48.714] --> textDocument/clangd.fileStatus
I[20:14:48.715] Code complete: sema context IncludedFile, query scopes [] (AnyScope=true), expected type <none>
I[20:14:48.716] Code complete: 3 results from Sema, 0 from Index, 0 matched, 0 from identifiers, 3 returned.
I[20:14:48.716] --> reply:textDocument/completion(39) 39 ms
I[20:14:48.726] Built preamble of size 233316 for file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 15 in 0.01 seconds
I[20:14:48.726] --> workspace/semanticTokens/refresh(9)
I[20:14:48.727] <-- reply(9)
I[20:14:48.737] --> textDocument/publishDiagnostics
I[20:14:48.737] --> textDocument/inactiveRegions
I[20:14:48.760] --> textDocument/publishDiagnostics
I[20:14:48.760] --> textDocument/inactiveRegions
I[20:14:48.760] --> reply:textDocument/semanticTokens/full/delta(40) 75 ms
I[20:14:48.760] --> textDocument/clangd.fileStatus
I[20:14:48.932] <-- textDocument/didChange
I[20:14:48.932] --> textDocument/clangd.fileStatus
I[20:14:48.932] <-- textDocument/completion(41)
I[20:14:48.971] Code complete: sema context IncludedFile, query scopes [] (AnyScope=true), expected type <none>
I[20:14:48.971] Code complete: 1 results from Sema, 0 from Index, 0 matched, 0 from identifiers, 1 returned.
I[20:14:48.971] --> reply:textDocument/completion(41) 38 ms
I[20:14:48.991] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:48.992] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 16 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:49.003] --> textDocument/clangd.fileStatus
I[20:14:49.014] Built preamble of size 233316 for file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 16 in 0.01 seconds
I[20:14:49.014] --> workspace/semanticTokens/refresh(10)
I[20:14:49.015] <-- reply(10)
I[20:14:49.015] <-- textDocument/semanticTokens/full/delta(42)
I[20:14:49.025] --> textDocument/publishDiagnostics
I[20:14:49.025] --> textDocument/inactiveRegions
I[20:14:49.049] --> textDocument/publishDiagnostics
I[20:14:49.049] --> textDocument/inactiveRegions
I[20:14:49.049] --> reply:textDocument/semanticTokens/full/delta(42) 33 ms
I[20:14:49.049] --> textDocument/clangd.fileStatus
I[20:14:49.242] <-- textDocument/foldingRange(43)
I[20:14:49.242] --> reply:textDocument/foldingRange(43) 0 ms
I[20:14:49.305] <-- textDocument/codeAction(44)
I[20:14:49.305] --> reply:textDocument/codeAction(44) 0 ms
I[20:14:49.305] --> textDocument/clangd.fileStatus
I[20:14:49.458] <-- textDocument/documentSymbol(45)
I[20:14:49.458] --> reply:textDocument/documentSymbol(45) 0 ms
I[20:14:49.458] --> textDocument/clangd.fileStatus
I[20:14:49.517] <-- textDocument/didChange
I[20:14:49.517] --> textDocument/clangd.fileStatus
I[20:14:49.567] --> textDocument/clangd.fileStatus
I[20:14:49.583] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:49.583] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 17 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:49.595] --> textDocument/clangd.fileStatus
I[20:14:49.772] <-- textDocument/codeAction(46)
I[20:14:49.819] <-- textDocument/foldingRange(47)
I[20:14:49.821] --> reply:textDocument/foldingRange(47) 1 ms
I[20:14:49.915] Built preamble of size 5194604 for file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 17 in 0.32 seconds
I[20:14:49.916] --> workspace/semanticTokens/refresh(11)
I[20:14:49.916] <-- reply(11)
I[20:14:49.917] <-- textDocument/semanticTokens/full/delta(48)
I[20:14:49.958] <-- textDocument/didChange
I[20:14:49.958] <-- $/cancelRequest
I[20:14:50.086] --> textDocument/publishDiagnostics
I[20:14:50.086] --> textDocument/inactiveRegions
I[20:14:50.125] --> textDocument/publishDiagnostics
I[20:14:50.125] --> textDocument/inactiveRegions
I[20:14:50.125] --> reply:textDocument/codeAction(46) 352 ms, error: Task was cancelled.
I[20:14:50.125] --> reply:textDocument/semanticTokens/full/delta(48) 208 ms
I[20:14:50.125] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:50.125] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 18 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
[Error - 20:14:50] Request textDocument/codeAction failed.
[object Object]
I[20:14:50.135] --> textDocument/clangd.fileStatus
I[20:14:50.164] --> textDocument/clangd.fileStatus
I[20:14:50.164] --> textDocument/publishDiagnostics
I[20:14:50.164] --> textDocument/inactiveRegions
I[20:14:50.164] --> textDocument/clangd.fileStatus
I[20:14:50.236] <-- textDocument/didChange
I[20:14:50.236] --> textDocument/clangd.fileStatus
I[20:14:50.248] <-- textDocument/completion(49)
I[20:14:50.288] Code complete: sema context TopLevel, query scopes [] (AnyScope=true), expected type <none>
I[20:14:50.289] Code complete: 4 results from Sema, 100 from Index, 0 matched, 0 from identifiers, 100 returned (incomplete).
I[20:14:50.289] --> textDocument/clangd.fileStatus
I[20:14:50.289] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:50.290] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 19 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:50.296] --> reply:textDocument/completion(49) 48 ms
I[20:14:50.302] --> textDocument/clangd.fileStatus
I[20:14:50.334] --> textDocument/clangd.fileStatus
I[20:14:50.334] --> textDocument/publishDiagnostics
I[20:14:50.334] --> textDocument/inactiveRegions
I[20:14:50.334] --> textDocument/clangd.fileStatus
I[20:14:50.407] <-- textDocument/semanticTokens/full/delta(50)
I[20:14:50.407] --> textDocument/clangd.fileStatus
I[20:14:50.407] --> reply:textDocument/semanticTokens/full/delta(50) 0 ms
I[20:14:50.407] --> textDocument/clangd.fileStatus
I[20:14:50.476] <-- textDocument/didChange
I[20:14:50.476] --> textDocument/clangd.fileStatus
I[20:14:50.477] <-- textDocument/completion(51)
I[20:14:50.490] Built preamble of size 5194608 for file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 18 in 0.35 seconds
I[20:14:50.490] --> workspace/semanticTokens/refresh(12)
I[20:14:50.490] --> textDocument/clangd.fileStatus
I[20:14:50.490] --> textDocument/clangd.fileStatus
I[20:14:50.491] <-- reply(12)
I[20:14:50.491] --> textDocument/clangd.fileStatus
I[20:14:50.491] <-- textDocument/semanticTokens/full/delta(52)
I[20:14:50.510] <-- textDocument/didChange
I[20:14:50.520] Code complete: sema context TopLevel, query scopes [] (AnyScope=true), expected type <none>
I[20:14:50.521] Code complete: 3 results from Sema, 96 from Index, 0 matched, 0 from identifiers, 99 returned (incomplete).
I[20:14:50.526] --> textDocument/clangd.fileStatus
I[20:14:50.526] --> textDocument/publishDiagnostics
I[20:14:50.526] --> textDocument/inactiveRegions
I[20:14:50.526] --> textDocument/clangd.fileStatus
I[20:14:50.527] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:50.527] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 20 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:50.528] --> reply:textDocument/completion(51) 51 ms
I[20:14:50.537] <-- textDocument/completion(53)
I[20:14:50.538] --> textDocument/clangd.fileStatus
I[20:14:50.569] --> textDocument/clangd.fileStatus
I[20:14:50.569] --> textDocument/publishDiagnostics
I[20:14:50.569] --> textDocument/inactiveRegions
I[20:14:50.570] --> textDocument/clangd.fileStatus
I[20:14:50.570] --> reply:textDocument/semanticTokens/full/delta(52) 78 ms
I[20:14:50.570] --> textDocument/clangd.fileStatus
I[20:14:50.570] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:50.570] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 21 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:50.577] Code complete: sema context TopLevel, query scopes [] (AnyScope=true), expected type <none>
I[20:14:50.578] Code complete: 1 results from Sema, 94 from Index, 0 matched, 0 from identifiers, 95 returned (incomplete).
I[20:14:50.581] --> textDocument/clangd.fileStatus
I[20:14:50.584] --> reply:textDocument/completion(53) 46 ms
I[20:14:50.591] <-- textDocument/didChange
I[20:14:50.616] --> textDocument/clangd.fileStatus
I[20:14:50.616] --> textDocument/publishDiagnostics
I[20:14:50.616] --> textDocument/inactiveRegions
I[20:14:50.616] --> textDocument/clangd.fileStatus
I[20:14:50.646] --> textDocument/clangd.fileStatus
I[20:14:50.646] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:50.647] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 22 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:50.657] --> textDocument/clangd.fileStatus
I[20:14:50.676] <-- textDocument/didChange
I[20:14:50.686] <-- textDocument/completion(54)
I[20:14:50.688] --> textDocument/clangd.fileStatus
I[20:14:50.688] --> textDocument/publishDiagnostics
I[20:14:50.688] --> textDocument/inactiveRegions
I[20:14:50.688] --> textDocument/clangd.fileStatus
I[20:14:50.726] Failed to generate include insertion edits for adding header (FileURI='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h', IncludeHeader='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h') into d:\CS\竞赛\服创赛\文档\demo\demo.cpp: Header not on include path
I[20:14:50.726] Failed to generate include insertion edits for adding header (FileURI='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h', IncludeHeader='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h') into d:\CS\竞赛\服创赛\文档\demo\demo.cpp: Header not on include path
I[20:14:50.726] Failed to generate include insertion edits for adding header (FileURI='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h', IncludeHeader='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h') into d:\CS\竞赛\服创赛\文档\demo\demo.cpp: Header not on include path
I[20:14:50.726] Failed to generate include insertion edits for adding header (FileURI='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h', IncludeHeader='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h') into d:\CS\竞赛\服创赛\文档\demo\demo.cpp: Header not on include path
I[20:14:50.726] Failed to generate include insertion edits for adding header (FileURI='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h', IncludeHeader='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h') into d:\CS\竞赛\服创赛\文档\demo\demo.cpp: Header not on include path
I[20:14:50.726] Failed to generate include insertion edits for adding header (FileURI='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h', IncludeHeader='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h') into d:\CS\竞赛\服创赛\文档\demo\demo.cpp: Header not on include path
I[20:14:50.726] Failed to generate include insertion edits for adding header (FileURI='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h', IncludeHeader='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h') into d:\CS\竞赛\服创赛\文档\demo\demo.cpp: Header not on include path
I[20:14:50.726] Failed to generate include insertion edits for adding header (FileURI='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h', IncludeHeader='file:///C:/Users/Shelly/AppData/Roaming/Code/User/globalStorage/llvm-vs-code-extensions.vscode-clangd/install/17.0.3/clangd_17.0.3/lib/clang/17/include/stdatomic.h') into d:\CS\竞赛\服创赛\文档\demo\demo.cpp: Header not on include path
I[20:14:50.726] Code complete: sema context SymbolOrNewName, query scopes [] (AnyScope=true), expected type <none>
I[20:14:50.726] Code complete: 2 results from Sema, 89 from Index, 0 matched, 0 from identifiers, 91 returned (incomplete).
I[20:14:50.731] --> reply:textDocument/completion(54) 45 ms
I[20:14:50.739] --> textDocument/clangd.fileStatus
I[20:14:50.739] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:50.741] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 23 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:50.751] --> textDocument/clangd.fileStatus
I[20:14:50.782] --> textDocument/clangd.fileStatus
I[20:14:50.782] --> textDocument/publishDiagnostics
I[20:14:50.782] --> textDocument/inactiveRegions
I[20:14:50.782] --> textDocument/clangd.fileStatus
I[20:14:50.819] <-- textDocument/didChange
I[20:14:50.819] --> textDocument/clangd.fileStatus
I[20:14:50.820] <-- textDocument/completion(55)
I[20:14:50.859] Code complete: sema context SymbolOrNewName, query scopes [] (AnyScope=true), expected type <none>
I[20:14:50.860] Code complete: 2 results from Sema, 72 from Index, 0 matched, 0 from identifiers, 74 returned (incomplete).
I[20:14:50.861] Built preamble of size 5194608 for file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 19 in 0.37 seconds
I[20:14:50.861] --> workspace/semanticTokens/refresh(13)
I[20:14:50.861] --> textDocument/clangd.fileStatus
I[20:14:50.861] --> textDocument/clangd.fileStatus
I[20:14:50.862] --> textDocument/clangd.fileStatus
I[20:14:50.862] <-- reply(13)
I[20:14:50.863] <-- textDocument/semanticTokens/full/delta(56)
I[20:14:50.864] --> reply:textDocument/completion(55) 44 ms
I[20:14:50.885] <-- textDocument/didChange
I[20:14:50.885] <-- textDocument/completion(57)
I[20:14:50.895] --> textDocument/publishDiagnostics
I[20:14:50.895] --> textDocument/inactiveRegions
I[20:14:50.895] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:50.896] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 24 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:50.906] --> textDocument/clangd.fileStatus
I[20:14:50.922] Code complete: sema context SymbolOrNewName, query scopes [] (AnyScope=true), expected type <none>
I[20:14:50.922] Code complete: 0 results from Sema, 2 from Index, 0 matched, 0 from identifiers, 2 returned.
I[20:14:50.923] --> reply:textDocument/completion(57) 37 ms
I[20:14:50.939] --> textDocument/publishDiagnostics
I[20:14:50.939] --> textDocument/inactiveRegions
I[20:14:50.940] --> reply:textDocument/semanticTokens/full/delta(56) 76 ms
I[20:14:50.940] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:50.940] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 25 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:50.951] --> textDocument/clangd.fileStatus
I[20:14:50.987] --> textDocument/publishDiagnostics
I[20:14:50.987] --> textDocument/inactiveRegions
I[20:14:50.987] --> textDocument/clangd.fileStatus
I[20:14:51.092] <-- textDocument/didChange
I[20:14:51.092] --> textDocument/clangd.fileStatus
I[20:14:51.093] <-- textDocument/completion(58)
I[20:14:51.131] Code complete: sema context SymbolOrNewName, query scopes [] (AnyScope=true), expected type <none>
I[20:14:51.131] Code complete: 0 results from Sema, 2 from Index, 0 matched, 0 from identifiers, 2 returned.
I[20:14:51.131] --> reply:textDocument/completion(58) 38 ms
I[20:14:51.143] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:51.145] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 26 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:51.154] --> textDocument/clangd.fileStatus
I[20:14:51.184] --> textDocument/publishDiagnostics
I[20:14:51.184] --> textDocument/inactiveRegions
I[20:14:51.184] --> textDocument/clangd.fileStatus
I[20:14:51.335] <-- textDocument/semanticTokens/full/delta(59)
I[20:14:51.335] --> reply:textDocument/semanticTokens/full/delta(59) 0 ms
I[20:14:51.335] --> textDocument/clangd.fileStatus
I[20:14:51.396] <-- textDocument/foldingRange(60)
I[20:14:51.396] --> reply:textDocument/foldingRange(60) 0 ms
I[20:14:51.443] <-- textDocument/codeAction(61)
I[20:14:51.443] --> reply:textDocument/codeAction(61) 0 ms
I[20:14:51.444] --> textDocument/clangd.fileStatus
I[20:14:51.621] <-- textDocument/documentSymbol(62)
I[20:14:51.622] --> reply:textDocument/documentSymbol(62) 0 ms
I[20:14:51.622] --> textDocument/clangd.fileStatus
I[20:14:51.828] <-- textDocument/didChange
I[20:14:51.828] --> textDocument/clangd.fileStatus
I[20:14:51.877] --> textDocument/clangd.fileStatus
I[20:14:51.893] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:51.895] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 27 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:51.905] --> textDocument/clangd.fileStatus
I[20:14:51.934] --> textDocument/publishDiagnostics
I[20:14:51.934] --> textDocument/inactiveRegions
I[20:14:51.934] --> textDocument/clangd.fileStatus
I[20:14:51.987] <-- textDocument/signatureHelp(63)
I[20:14:52.024] --> reply:textDocument/signatureHelp(63) 36 ms
I[20:14:52.143] <-- textDocument/foldingRange(64)
I[20:14:52.143] --> reply:textDocument/foldingRange(64) 0 ms
I[20:14:52.191] <-- textDocument/codeAction(65)
I[20:14:52.191] --> reply:textDocument/codeAction(65) 0 ms
I[20:14:52.191] --> textDocument/clangd.fileStatus
I[20:14:52.283] <-- textDocument/semanticTokens/full/delta(66)
I[20:14:52.283] --> reply:textDocument/semanticTokens/full/delta(66) 0 ms
I[20:14:52.284] --> textDocument/clangd.fileStatus
I[20:14:52.398] <-- textDocument/documentSymbol(67)
I[20:14:52.398] --> reply:textDocument/documentSymbol(67) 0 ms
I[20:14:52.398] --> textDocument/clangd.fileStatus
I[20:14:52.851] <-- textDocument/didSave
I[20:14:52.851] File version went from 27 to 27
I[20:14:52.851] --> textDocument/clangd.fileStatus
I[20:14:52.908] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:52.908] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 27 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:52.920] --> textDocument/clangd.fileStatus
I[20:14:52.920] --> textDocument/clangd.fileStatus
I[20:14:52.933] --> textDocument/clangd.fileStatus
I[20:14:52.933] --> textDocument/clangd.fileStatus
I[20:14:53.110] <-- textDocument/inlayHint(68)
I[20:14:53.111] --> reply:textDocument/inlayHint(68) 0 ms
I[20:14:53.111] --> textDocument/clangd.fileStatus
I[20:14:53.330] <-- textDocument/documentLink(69)
I[20:14:53.330] --> reply:textDocument/documentLink(69) 0 ms
I[20:14:53.330] --> textDocument/clangd.fileStatus
I[20:14:53.464] <-- textDocument/hover(70)
I[20:14:53.466] --> reply:textDocument/hover(70) 1 ms
I[20:14:53.466] --> textDocument/clangd.fileStatus
I[20:14:53.616] <-- textDocument/codeAction(71)
I[20:14:53.616] --> reply:textDocument/codeAction(71) 0 ms
I[20:14:53.616] --> textDocument/clangd.fileStatus
I[20:14:54.761] <-- textDocument/codeAction(72)
I[20:14:54.762] --> reply:textDocument/codeAction(72) 0 ms
I[20:14:54.762] --> textDocument/clangd.fileStatus
I[20:14:55.021] <-- textDocument/hover(73)
I[20:14:55.024] --> reply:textDocument/hover(73) 3 ms
I[20:14:55.024] --> textDocument/clangd.fileStatus
I[20:14:56.112] <-- textDocument/hover(74)
I[20:14:56.113] --> reply:textDocument/hover(74) 1 ms
I[20:14:56.113] --> textDocument/clangd.fileStatus
I[20:14:56.381] <-- textDocument/codeAction(75)
I[20:14:56.381] --> reply:textDocument/codeAction(75) 0 ms
I[20:14:56.382] --> textDocument/clangd.fileStatus
I[20:14:56.898] <-- textDocument/hover(76)
I[20:14:56.900] --> reply:textDocument/hover(76) 1 ms
I[20:14:56.900] --> textDocument/clangd.fileStatus
I[20:14:57.484] <-- textDocument/codeAction(77)
I[20:14:57.485] --> reply:textDocument/codeAction(77) 0 ms
I[20:14:57.485] --> textDocument/clangd.fileStatus
I[20:14:57.524] <-- textDocument/hover(78)
I[20:14:57.525] --> reply:textDocument/hover(78) 1 ms
I[20:14:57.525] --> textDocument/clangd.fileStatus
I[20:14:58.726] <-- textDocument/didChange
I[20:14:58.726] --> textDocument/clangd.fileStatus
I[20:14:58.778] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:58.779] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 28 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:58.790] --> textDocument/clangd.fileStatus
I[20:14:58.821] --> textDocument/publishDiagnostics
I[20:14:58.821] --> textDocument/inactiveRegions
I[20:14:58.821] --> textDocument/clangd.fileStatus
I[20:14:58.856] <-- textDocument/signatureHelp(79)
I[20:14:58.893] --> reply:textDocument/signatureHelp(79) 36 ms
I[20:14:58.956] <-- textDocument/didChange
I[20:14:58.956] --> textDocument/clangd.fileStatus
I[20:14:59.013] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:14:59.014] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 29 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:14:59.025] --> textDocument/clangd.fileStatus
I[20:14:59.056] --> textDocument/publishDiagnostics
I[20:14:59.056] --> textDocument/inactiveRegions
I[20:14:59.056] --> textDocument/clangd.fileStatus
I[20:14:59.176] <-- textDocument/semanticTokens/full/delta(80)
I[20:14:59.177] --> reply:textDocument/semanticTokens/full/delta(80) 0 ms
I[20:14:59.177] --> textDocument/clangd.fileStatus
I[20:14:59.263] <-- textDocument/foldingRange(81)
I[20:14:59.263] --> reply:textDocument/foldingRange(81) 0 ms
I[20:14:59.482] <-- textDocument/documentSymbol(82)
I[20:14:59.482] --> reply:textDocument/documentSymbol(82) 0 ms
I[20:14:59.482] --> textDocument/clangd.fileStatus
I[20:14:59.981] <-- textDocument/didSave
I[20:14:59.981] File version went from 29 to 29
I[20:14:59.981] --> textDocument/clangd.fileStatus
I[20:15:00.040] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:00.040] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 29 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:00.051] --> textDocument/clangd.fileStatus
I[20:15:00.051] --> textDocument/clangd.fileStatus
I[20:15:00.063] --> textDocument/clangd.fileStatus
I[20:15:00.063] --> textDocument/clangd.fileStatus
I[20:15:00.211] <-- textDocument/inlayHint(83)
I[20:15:00.211] --> reply:textDocument/inlayHint(83) 0 ms
I[20:15:00.211] --> textDocument/clangd.fileStatus
I[20:15:00.461] <-- textDocument/documentLink(84)
I[20:15:00.461] --> reply:textDocument/documentLink(84) 0 ms
I[20:15:00.461] --> textDocument/clangd.fileStatus
I[20:15:00.638] <-- textDocument/didChange
I[20:15:00.638] --> textDocument/clangd.fileStatus
I[20:15:00.658] <-- textDocument/completion(85)
I[20:15:00.693] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:00.694] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 30 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:00.700] Code complete: sema context Statement, query scopes [] (AnyScope=true), expected type <none>
I[20:15:00.701] Code complete: 12 results from Sema, 87 from Index, 0 matched, 0 from identifiers, 99 returned (incomplete).
I[20:15:00.707] --> textDocument/clangd.fileStatus
I[20:15:00.708] --> reply:textDocument/completion(85) 49 ms
I[20:15:00.739] --> textDocument/publishDiagnostics
I[20:15:00.739] --> textDocument/inactiveRegions
I[20:15:00.739] --> textDocument/clangd.fileStatus
I[20:15:00.869] <-- textDocument/didChange
I[20:15:00.869] --> textDocument/clangd.fileStatus
I[20:15:00.869] <-- textDocument/completion(86)
I[20:15:00.909] Code complete: sema context Statement, query scopes [] (AnyScope=true), expected type <none>
I[20:15:00.910] Code complete: 7 results from Sema, 86 from Index, 0 matched, 0 from identifiers, 93 returned (incomplete).
I[20:15:00.912] --> reply:textDocument/completion(86) 42 ms
I[20:15:00.926] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:00.927] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 31 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:00.937] --> textDocument/clangd.fileStatus
I[20:15:00.966] --> textDocument/publishDiagnostics
I[20:15:00.966] --> textDocument/inactiveRegions
I[20:15:00.966] --> textDocument/clangd.fileStatus
I[20:15:01.089] <-- textDocument/semanticTokens/full/delta(87)
I[20:15:01.089] --> reply:textDocument/semanticTokens/full/delta(87) 0 ms
I[20:15:01.089] --> textDocument/clangd.fileStatus
I[20:15:01.099] <-- textDocument/didChange
I[20:15:01.099] --> textDocument/clangd.fileStatus
I[20:15:01.100] <-- textDocument/completion(88)
I[20:15:01.139] Code complete: sema context Statement, query scopes [] (AnyScope=true), expected type <none>
I[20:15:01.140] Code complete: 1 results from Sema, 7 from Index, 1 matched, 0 from identifiers, 7 returned.
I[20:15:01.140] --> reply:textDocument/completion(88) 40 ms
I[20:15:01.159] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:01.160] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 32 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:01.170] --> textDocument/clangd.fileStatus
I[20:15:01.202] --> textDocument/publishDiagnostics
I[20:15:01.202] --> textDocument/inactiveRegions
I[20:15:01.202] --> textDocument/clangd.fileStatus
I[20:15:01.407] <-- textDocument/foldingRange(89)
I[20:15:01.408] --> reply:textDocument/foldingRange(89) 0 ms
I[20:15:01.472] <-- textDocument/codeAction(90)
I[20:15:01.472] --> reply:textDocument/codeAction(90) 0 ms
I[20:15:01.472] --> textDocument/clangd.fileStatus
I[20:15:01.485] <-- textDocument/didChange
I[20:15:01.485] --> textDocument/clangd.fileStatus
I[20:15:01.485] <-- textDocument/completion(91)
I[20:15:01.485] --> reply:textDocument/completion(91) 0 ms
I[20:15:01.546] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:01.547] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 33 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:01.550] <-- textDocument/semanticTokens/full/delta(92)
I[20:15:01.559] --> textDocument/clangd.fileStatus
I[20:15:01.589] --> textDocument/publishDiagnostics
I[20:15:01.589] --> textDocument/inactiveRegions
I[20:15:01.589] --> reply:textDocument/semanticTokens/full/delta(92) 38 ms
I[20:15:01.589] --> textDocument/clangd.fileStatus
I[20:15:01.627] <-- textDocument/didChange
I[20:15:01.627] --> textDocument/clangd.fileStatus
I[20:15:01.628] <-- textDocument/completion(93)
I[20:15:01.667] Code complete: sema context Symbol, query scopes [std::] (AnyScope=false), expected type <none>
I[20:15:01.668] Code complete: 0 results from Sema, 89 from Index, 0 matched, 0 from identifiers, 89 returned (incomplete).
I[20:15:01.672] --> reply:textDocument/completion(93) 44 ms
I[20:15:01.686] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:01.688] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 34 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:01.697] --> textDocument/clangd.fileStatus
I[20:15:01.727] --> textDocument/publishDiagnostics
I[20:15:01.727] --> textDocument/inactiveRegions
I[20:15:01.727] --> textDocument/clangd.fileStatus
I[20:15:01.861] <-- textDocument/didChange
I[20:15:01.861] --> textDocument/clangd.fileStatus
I[20:15:01.861] <-- textDocument/completion(94)
I[20:15:01.883] <-- textDocument/didChange
I[20:15:01.883] --> textDocument/clangd.fileStatus
I[20:15:01.901] Code complete: sema context Symbol, query scopes [std::] (AnyScope=false), expected type <none>
I[20:15:01.901] Code complete: 0 results from Sema, 91 from Index, 0 matched, 0 from identifiers, 91 returned (incomplete).
I[20:15:01.905] --> reply:textDocument/completion(94) 44 ms
I[20:15:01.911] <-- textDocument/completion(95)
I[20:15:01.935] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:01.937] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 36 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:01.946] --> textDocument/clangd.fileStatus
I[20:15:01.949] Code complete: sema context Symbol, query scopes [std::] (AnyScope=false), expected type <none>
I[20:15:01.950] Code complete: 0 results from Sema, 85 from Index, 0 matched, 0 from identifiers, 85 returned (incomplete).
I[20:15:01.954] --> reply:textDocument/completion(95) 42 ms
I[20:15:01.993] --> textDocument/publishDiagnostics
I[20:15:01.993] --> textDocument/inactiveRegions
I[20:15:01.993] --> textDocument/clangd.fileStatus
I[20:15:02.067] <-- textDocument/didChange
I[20:15:02.067] --> textDocument/clangd.fileStatus
I[20:15:02.068] <-- textDocument/completion(96)
I[20:15:02.077] <-- textDocument/semanticTokens/full/delta(97)
I[20:15:02.077] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:02.079] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 37 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:02.088] --> textDocument/clangd.fileStatus
I[20:15:02.105] Code complete: sema context Symbol, query scopes [std::] (AnyScope=false), expected type <none>
I[20:15:02.105] Code complete: 0 results from Sema, 6 from Index, 0 matched, 0 from identifiers, 6 returned.
I[20:15:02.106] --> reply:textDocument/completion(96) 37 ms
I[20:15:02.135] --> textDocument/publishDiagnostics
I[20:15:02.135] --> textDocument/inactiveRegions
I[20:15:02.135] --> reply:textDocument/semanticTokens/full/delta(97) 58 ms
I[20:15:02.135] --> textDocument/clangd.fileStatus
I[20:15:02.156] <-- textDocument/didChange
I[20:15:02.156] --> textDocument/clangd.fileStatus
I[20:15:02.156] <-- textDocument/completion(98)
I[20:15:02.194] Code complete: sema context Symbol, query scopes [std::] (AnyScope=false), expected type <none>
I[20:15:02.195] Code complete: 0 results from Sema, 4 from Index, 0 matched, 0 from identifiers, 4 returned.
I[20:15:02.195] --> reply:textDocument/completion(98) 38 ms
I[20:15:02.214] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:02.216] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 38 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:02.226] --> textDocument/clangd.fileStatus
I[20:15:02.256] --> textDocument/publishDiagnostics
I[20:15:02.256] --> textDocument/inactiveRegions
I[20:15:02.257] --> textDocument/clangd.fileStatus
I[20:15:02.464] <-- textDocument/foldingRange(99)
I[20:15:02.465] --> reply:textDocument/foldingRange(99) 0 ms
I[20:15:02.510] <-- textDocument/codeAction(100)
I[20:15:02.510] --> reply:textDocument/codeAction(100) 0 ms
I[20:15:02.510] --> textDocument/clangd.fileStatus
I[20:15:02.556] <-- textDocument/didChange
I[20:15:02.556] --> textDocument/clangd.fileStatus
I[20:15:02.557] <-- textDocument/completion(101)
I[20:15:02.557] --> reply:textDocument/completion(101) 0 ms
I[20:15:02.618] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:02.619] <-- textDocument/semanticTokens/full/delta(102)
I[20:15:02.620] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 39 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:02.634] --> textDocument/clangd.fileStatus
I[20:15:02.663] --> textDocument/publishDiagnostics
I[20:15:02.663] --> textDocument/inactiveRegions
I[20:15:02.664] --> reply:textDocument/semanticTokens/full/delta(102) 44 ms
I[20:15:02.664] --> textDocument/clangd.fileStatus
I[20:15:02.680] <-- textDocument/signatureHelp(103)
I[20:15:02.699] <-- textDocument/didChange
I[20:15:02.699] --> textDocument/clangd.fileStatus
I[20:15:02.700] <-- textDocument/completion(104)
I[20:15:02.700] --> reply:textDocument/completion(104) 0 ms
I[20:15:02.717] --> reply:textDocument/signatureHelp(103) 37 ms
I[20:15:02.759] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:02.760] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 40 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:02.770] --> textDocument/clangd.fileStatus
I[20:15:02.799] --> textDocument/publishDiagnostics
I[20:15:02.799] --> textDocument/inactiveRegions
I[20:15:02.799] --> textDocument/clangd.fileStatus
I[20:15:02.822] <-- textDocument/signatureHelp(105)
I[20:15:02.857] --> reply:textDocument/signatureHelp(105) 35 ms
I[20:15:03.011] <-- textDocument/foldingRange(106)
I[20:15:03.011] --> reply:textDocument/foldingRange(106) 0 ms
I[20:15:03.056] <-- textDocument/codeAction(107)
I[20:15:03.057] --> reply:textDocument/codeAction(107) 0 ms
I[20:15:03.057] --> textDocument/clangd.fileStatus
I[20:15:03.149] <-- textDocument/semanticTokens/full/delta(108)
I[20:15:03.149] --> reply:textDocument/semanticTokens/full/delta(108) 0 ms
I[20:15:03.149] --> textDocument/clangd.fileStatus
I[20:15:03.225] <-- textDocument/documentSymbol(109)
I[20:15:03.225] --> reply:textDocument/documentSymbol(109) 0 ms
I[20:15:03.225] --> textDocument/clangd.fileStatus
I[20:15:03.668] <-- textDocument/didChange
I[20:15:03.668] --> textDocument/clangd.fileStatus
I[20:15:03.729] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:03.730] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 41 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:03.741] --> textDocument/clangd.fileStatus
I[20:15:03.769] --> textDocument/publishDiagnostics
I[20:15:03.769] --> textDocument/inactiveRegions
I[20:15:03.769] --> textDocument/clangd.fileStatus
I[20:15:03.979] <-- textDocument/foldingRange(110)
I[20:15:03.979] --> reply:textDocument/foldingRange(110) 0 ms
I[20:15:04.023] <-- textDocument/codeAction(111)
I[20:15:04.023] --> reply:textDocument/codeAction(111) 0 ms
I[20:15:04.023] --> textDocument/clangd.fileStatus
I[20:15:04.108] <-- textDocument/didChange
I[20:15:04.108] --> textDocument/clangd.fileStatus
I[20:15:04.119] <-- textDocument/semanticTokens/full/delta(112)
I[20:15:04.119] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:04.120] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 42 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:04.131] --> textDocument/clangd.fileStatus
I[20:15:04.164] --> textDocument/publishDiagnostics
I[20:15:04.164] --> textDocument/inactiveRegions
I[20:15:04.164] --> reply:textDocument/semanticTokens/full/delta(112) 44 ms
I[20:15:04.164] --> textDocument/clangd.fileStatus
I[20:15:04.418] <-- textDocument/foldingRange(113)
I[20:15:04.418] <-- textDocument/codeAction(114)
I[20:15:04.418] --> reply:textDocument/foldingRange(113) 0 ms
I[20:15:04.418] --> reply:textDocument/codeAction(114) 0 ms
I[20:15:04.418] --> textDocument/clangd.fileStatus
I[20:15:04.428] <-- textDocument/didChange
I[20:15:04.428] --> textDocument/clangd.fileStatus
I[20:15:04.467] <-- textDocument/didChange
I[20:15:04.467] --> textDocument/clangd.fileStatus
I[20:15:04.527] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:04.528] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 44 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:04.539] --> textDocument/clangd.fileStatus
I[20:15:04.570] --> textDocument/publishDiagnostics
I[20:15:04.570] --> textDocument/inactiveRegions
I[20:15:04.570] --> textDocument/clangd.fileStatus
I[20:15:04.635] <-- textDocument/didChange
I[20:15:04.635] --> textDocument/clangd.fileStatus
I[20:15:04.685] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:04.687] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 45 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:04.698] --> textDocument/clangd.fileStatus
I[20:15:04.728] --> textDocument/publishDiagnostics
I[20:15:04.728] --> textDocument/inactiveRegions
I[20:15:04.728] --> textDocument/clangd.fileStatus
I[20:15:04.804] <-- textDocument/didChange
I[20:15:04.804] --> textDocument/clangd.fileStatus
I[20:15:04.858] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:04.859] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 46 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:04.870] --> textDocument/clangd.fileStatus
I[20:15:04.881] <-- textDocument/semanticTokens/full/delta(115)
I[20:15:04.901] --> textDocument/publishDiagnostics
I[20:15:04.901] --> textDocument/inactiveRegions
I[20:15:04.901] --> reply:textDocument/semanticTokens/full/delta(115) 19 ms
I[20:15:04.901] --> textDocument/clangd.fileStatus
I[20:15:05.012] <-- textDocument/didChange
I[20:15:05.012] --> textDocument/clangd.fileStatus
I[20:15:05.077] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:05.078] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 47 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:05.089] --> textDocument/clangd.fileStatus
I[20:15:05.120] --> textDocument/publishDiagnostics
I[20:15:05.121] --> textDocument/inactiveRegions
I[20:15:05.121] --> textDocument/clangd.fileStatus
I[20:15:05.156] <-- textDocument/didChange
I[20:15:05.156] --> textDocument/clangd.fileStatus
I[20:15:05.215] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:05.216] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 48 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:05.228] --> textDocument/clangd.fileStatus
I[20:15:05.260] --> textDocument/publishDiagnostics
I[20:15:05.260] --> textDocument/inactiveRegions
I[20:15:05.260] --> textDocument/clangd.fileStatus
I[20:15:05.332] <-- textDocument/didChange
I[20:15:05.332] --> textDocument/clangd.fileStatus
I[20:15:05.386] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:05.387] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 49 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:05.397] --> textDocument/clangd.fileStatus
I[20:15:05.430] --> textDocument/publishDiagnostics
I[20:15:05.430] --> textDocument/inactiveRegions
I[20:15:05.430] --> textDocument/clangd.fileStatus
I[20:15:05.485] <-- textDocument/semanticTokens/full/delta(116)
I[20:15:05.485] --> reply:textDocument/semanticTokens/full/delta(116) 0 ms
I[20:15:05.485] --> textDocument/clangd.fileStatus
I[20:15:05.486] <-- textDocument/didChange
I[20:15:05.486] --> textDocument/clangd.fileStatus
I[20:15:05.542] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:05.543] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 50 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:05.554] --> textDocument/clangd.fileStatus
I[20:15:05.585] --> textDocument/publishDiagnostics
I[20:15:05.585] --> textDocument/inactiveRegions
I[20:15:05.585] --> textDocument/clangd.fileStatus
I[20:15:05.643] <-- textDocument/didChange
I[20:15:05.643] --> textDocument/clangd.fileStatus
I[20:15:05.698] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:05.700] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 51 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:05.711] --> textDocument/clangd.fileStatus
I[20:15:05.741] --> textDocument/publishDiagnostics
I[20:15:05.741] --> textDocument/inactiveRegions
I[20:15:05.741] --> textDocument/clangd.fileStatus
I[20:15:05.931] <-- textDocument/semanticTokens/full/delta(117)
I[20:15:05.931] --> reply:textDocument/semanticTokens/full/delta(117) 0 ms
I[20:15:05.931] --> textDocument/clangd.fileStatus
I[20:15:05.946] <-- textDocument/foldingRange(118)
I[20:15:05.947] --> reply:textDocument/foldingRange(118) 0 ms
I[20:15:05.994] <-- textDocument/codeAction(119)
I[20:15:05.995] --> reply:textDocument/codeAction(119) 0 ms
I[20:15:05.995] --> textDocument/clangd.fileStatus
I[20:15:06.179] <-- textDocument/documentSymbol(120)
I[20:15:06.180] --> reply:textDocument/documentSymbol(120) 0 ms
I[20:15:06.180] --> textDocument/clangd.fileStatus
I[20:15:06.443] <-- textDocument/didChange
I[20:15:06.443] --> textDocument/clangd.fileStatus
I[20:15:06.507] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:06.508] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 52 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:06.519] --> textDocument/clangd.fileStatus
I[20:15:06.548] --> textDocument/publishDiagnostics
I[20:15:06.548] --> textDocument/inactiveRegions
I[20:15:06.548] --> textDocument/clangd.fileStatus
I[20:15:06.692] <-- textDocument/didChange
I[20:15:06.692] --> textDocument/clangd.fileStatus
I[20:15:06.692] <-- textDocument/completion(121)
I[20:15:06.692] --> reply:textDocument/completion(121) 0 ms
I[20:15:06.755] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:06.756] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 53 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:06.767] --> textDocument/clangd.fileStatus
I[20:15:06.796] --> textDocument/publishDiagnostics
I[20:15:06.796] --> textDocument/inactiveRegions
I[20:15:06.796] --> textDocument/clangd.fileStatus
I[20:15:06.893] <-- textDocument/semanticTokens/full/delta(122)
I[20:15:06.893] --> reply:textDocument/semanticTokens/full/delta(122) 0 ms
I[20:15:06.893] --> textDocument/clangd.fileStatus
I[20:15:07.004] <-- textDocument/foldingRange(123)
I[20:15:07.004] --> reply:textDocument/foldingRange(123) 0 ms
I[20:15:07.052] <-- textDocument/codeAction(124)
I[20:15:07.052] --> reply:textDocument/codeAction(124) 0 ms
I[20:15:07.052] --> textDocument/clangd.fileStatus
I[20:15:07.155] <-- textDocument/didChange
I[20:15:07.155] --> textDocument/clangd.fileStatus
I[20:15:07.206] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:07.207] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 54 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:07.218] --> textDocument/clangd.fileStatus
I[20:15:07.249] --> textDocument/publishDiagnostics
I[20:15:07.249] --> textDocument/inactiveRegions
I[20:15:07.249] --> textDocument/clangd.fileStatus
I[20:15:07.455] <-- textDocument/foldingRange(125)
I[20:15:07.456] --> reply:textDocument/foldingRange(125) 0 ms
I[20:15:07.503] <-- textDocument/codeAction(126)
I[20:15:07.503] --> reply:textDocument/codeAction(126) 0 ms
I[20:15:07.503] --> textDocument/clangd.fileStatus
I[20:15:07.646] <-- textDocument/semanticTokens/full/delta(127)
I[20:15:07.646] --> reply:textDocument/semanticTokens/full/delta(127) 0 ms
I[20:15:07.646] --> textDocument/clangd.fileStatus
I[20:15:07.684] <-- textDocument/didChange
I[20:15:07.684] --> textDocument/clangd.fileStatus
I[20:15:07.684] <-- textDocument/completion(128)
I[20:15:07.684] --> reply:textDocument/completion(128) 0 ms
I[20:15:07.733] --> textDocument/clangd.fileStatus
I[20:15:07.748] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:07.749] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 55 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:07.761] --> textDocument/clangd.fileStatus
I[20:15:07.792] --> textDocument/publishDiagnostics
I[20:15:07.792] --> textDocument/inactiveRegions
I[20:15:07.792] --> textDocument/clangd.fileStatus
I[20:15:07.994] <-- textDocument/foldingRange(129)
I[20:15:07.994] --> reply:textDocument/foldingRange(129) 0 ms
I[20:15:08.019] <-- textDocument/didChange
I[20:15:08.019] --> textDocument/clangd.fileStatus
I[20:15:08.074] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:08.075] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 56 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:08.087] --> textDocument/clangd.fileStatus
I[20:15:08.118] --> textDocument/publishDiagnostics
I[20:15:08.118] --> textDocument/inactiveRegions
I[20:15:08.118] --> textDocument/clangd.fileStatus
I[20:15:08.134] <-- textDocument/semanticTokens/full/delta(130)
I[20:15:08.134] --> reply:textDocument/semanticTokens/full/delta(130) 0 ms
I[20:15:08.134] --> textDocument/clangd.fileStatus
I[20:15:08.325] <-- textDocument/foldingRange(131)
I[20:15:08.325] --> reply:textDocument/foldingRange(131) 0 ms
I[20:15:08.331] <-- textDocument/didChange
I[20:15:08.331] --> textDocument/clangd.fileStatus
I[20:15:08.387] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:08.388] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 57 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:08.396] <-- textDocument/didChange
I[20:15:08.402] --> textDocument/clangd.fileStatus
I[20:15:08.433] --> textDocument/publishDiagnostics
I[20:15:08.433] --> textDocument/inactiveRegions
I[20:15:08.433] --> textDocument/clangd.fileStatus
I[20:15:08.451] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:08.452] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 58 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:08.461] --> textDocument/clangd.fileStatus
I[20:15:08.491] --> textDocument/publishDiagnostics
I[20:15:08.491] --> textDocument/inactiveRegions
I[20:15:08.491] --> textDocument/clangd.fileStatus
I[20:15:08.563] <-- textDocument/didChange
I[20:15:08.563] --> textDocument/clangd.fileStatus
I[20:15:08.623] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:08.624] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 59 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:08.635] --> textDocument/clangd.fileStatus
I[20:15:08.666] --> textDocument/publishDiagnostics
I[20:15:08.666] --> textDocument/inactiveRegions
I[20:15:08.666] --> textDocument/clangd.fileStatus
I[20:15:08.717] <-- textDocument/didChange
I[20:15:08.717] --> textDocument/clangd.fileStatus
I[20:15:08.779] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:08.781] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 60 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:08.782] <-- textDocument/semanticTokens/full/delta(132)
I[20:15:08.792] --> textDocument/clangd.fileStatus
I[20:15:08.823] --> textDocument/publishDiagnostics
I[20:15:08.823] --> textDocument/inactiveRegions
I[20:15:08.823] --> reply:textDocument/semanticTokens/full/delta(132) 40 ms
I[20:15:08.823] --> textDocument/clangd.fileStatus
I[20:15:08.924] <-- textDocument/didChange
I[20:15:08.924] --> textDocument/clangd.fileStatus
I[20:15:08.983] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:08.984] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 61 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:08.995] --> textDocument/clangd.fileStatus
I[20:15:09.027] --> textDocument/publishDiagnostics
I[20:15:09.027] --> textDocument/inactiveRegions
I[20:15:09.027] --> textDocument/clangd.fileStatus
I[20:15:09.230] <-- textDocument/foldingRange(133)
I[20:15:09.230] --> reply:textDocument/foldingRange(133) 0 ms
I[20:15:09.386] <-- textDocument/semanticTokens/full/delta(134)
I[20:15:09.386] --> reply:textDocument/semanticTokens/full/delta(134) 0 ms
I[20:15:09.386] --> textDocument/clangd.fileStatus
I[20:15:09.464] <-- textDocument/documentSymbol(135)
I[20:15:09.464] --> reply:textDocument/documentSymbol(135) 0 ms
I[20:15:09.464] --> textDocument/clangd.fileStatus
I[20:15:09.486] <-- textDocument/codeAction(136)
I[20:15:09.486] --> reply:textDocument/codeAction(136) 0 ms
I[20:15:09.486] --> textDocument/clangd.fileStatus
I[20:15:09.949] <-- textDocument/didSave
I[20:15:09.949] File version went from 61 to 61
I[20:15:09.949] --> textDocument/clangd.fileStatus
I[20:15:10.007] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:10.007] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 61 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:10.018] --> textDocument/clangd.fileStatus
I[20:15:10.018] --> textDocument/clangd.fileStatus
I[20:15:10.031] --> textDocument/clangd.fileStatus
I[20:15:10.031] --> textDocument/clangd.fileStatus
I[20:15:10.178] <-- textDocument/inlayHint(137)
I[20:15:10.179] --> reply:textDocument/inlayHint(137) 1 ms
I[20:15:10.180] --> textDocument/clangd.fileStatus
I[20:15:10.425] <-- textDocument/documentLink(138)
I[20:15:10.425] --> reply:textDocument/documentLink(138) 0 ms
I[20:15:10.425] --> textDocument/clangd.fileStatus
I[20:15:10.733] <-- textDocument/didChange
I[20:15:10.733] --> textDocument/clangd.fileStatus
I[20:15:10.797] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:10.798] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 62 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:10.808] --> textDocument/clangd.fileStatus
I[20:15:10.839] --> textDocument/publishDiagnostics
I[20:15:10.839] --> textDocument/inactiveRegions
I[20:15:10.839] --> textDocument/clangd.fileStatus
I[20:15:10.982] <-- textDocument/didChange
I[20:15:10.982] --> textDocument/clangd.fileStatus
I[20:15:11.046] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:11.047] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 63 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:11.058] --> textDocument/clangd.fileStatus
I[20:15:11.089] --> textDocument/publishDiagnostics
I[20:15:11.089] --> textDocument/inactiveRegions
I[20:15:11.089] --> textDocument/clangd.fileStatus
I[20:15:11.188] <-- textDocument/semanticTokens/full/delta(139)
I[20:15:11.188] --> reply:textDocument/semanticTokens/full/delta(139) 0 ms
I[20:15:11.188] --> textDocument/clangd.fileStatus
I[20:15:11.297] <-- textDocument/foldingRange(140)
I[20:15:11.298] --> reply:textDocument/foldingRange(140) 0 ms
I[20:15:11.520] <-- textDocument/documentSymbol(141)
I[20:15:11.520] --> reply:textDocument/documentSymbol(141) 0 ms
I[20:15:11.520] --> textDocument/clangd.fileStatus
I[20:15:11.995] <-- textDocument/didSave
I[20:15:11.995] File version went from 63 to 63
I[20:15:11.995] --> textDocument/clangd.fileStatus
I[20:15:12.046] Failed to find compilation database for d:\CS\竞赛\服创赛\文档\demo\demo.cpp
I[20:15:12.046] ASTWorker building file d:\CS\竞赛\服创赛\文档\demo\demo.cpp version 63 with command clangd fallback
[d:\CS\竞赛\服创赛\文档\demo]
"C:\\Program Files\\mingw64\\bin\\clang" "-resource-dir=c:\\Users\\Shelly\\AppData\\Roaming\\Code\\User\\globalStorage\\llvm-vs-code-extensions.vscode-clangd\\install\\17.0.3\\clangd_17.0.3\\lib\\clang\\17" -- "d:\\CS\\\xE7\xAB\x9E\xE8\xB5\x9B\\\xE6\x9C\x8D\xE5\x88\x9B\xE8\xB5\x9B\\\xE6\x96\x87\xE6\xA1\xA3\\demo\\demo.cpp"
I[20:15:12.057] --> textDocument/clangd.fileStatus
I[20:15:12.057] --> textDocument/clangd.fileStatus
I[20:15:12.070] --> textDocument/clangd.fileStatus
I[20:15:12.070] --> textDocument/clangd.fileStatus
I[20:15:12.234] <-- textDocument/inlayHint(142)
I[20:15:12.234] --> reply:textDocument/inlayHint(142) 0 ms
I[20:15:12.234] --> textDocument/clangd.fileStatus
I[20:15:12.484] <-- textDocument/documentLink(143)
I[20:15:12.484] --> reply:textDocument/documentLink(143) 0 ms
I[20:15:12.485] --> textDocument/clangd.fileStatus
I[20:15:26.045] <-- textDocument/inlayHint(144)
I[20:15:26.047] --> reply:textDocument/inlayHint(144) 1 ms
I[20:15:26.047] --> textDocument/clangd.fileStatus
I[20:15:55.657] <-- textDocument/hover(145)
I[20:15:55.660] --> reply:textDocument/hover(145) 3 ms
I[20:15:55.660] --> textDocument/clangd.fileStatus
I[20:15:55.714] <-- textDocument/documentHighlight(146)
I[20:15:55.714] --> reply:textDocument/documentHighlight(146) 0 ms
I[20:15:55.714] --> textDocument/clangd.fileStatus
I[20:15:55.959] <-- textDocument/codeAction(147)
I[20:15:55.959] --> reply:textDocument/codeAction(147) 0 ms
I[20:15:55.959] --> textDocument/clangd.fileStatus