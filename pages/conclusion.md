# 總結

<div class="max-h-[500px] overflow-y-auto py-10">

## 15.1 模板 DSL 的編譯器
- **編譯器**：將模板 DSL 轉換為 JavaScript 渲染函數的橋樑
- **編譯流程**：模板字串 → 模板 AST → JavaScript AST → 渲染函數
- **AST**：抽象語法樹，以樹狀結構描述程式碼的語法結構

## 15.2 Parser 的實作原理與狀態機
- **有限狀態自動機**：用於詞法分析，識別不同的 token（標籤、文本、指令等）
- **狀態轉換**：根據輸入字元在不同狀態間轉換，完成 token 掃描

## 15.3 建構 AST
- **語法分析**：將 token 序列轉換為具有層級結構的 AST
- **堆疊機制**：使用 elementStack 追蹤節點的嵌套關係

## 15.4 AST 的轉換與插件化架構
- **節點訪問**：深度優先遍歷（DFS）訪問所有節點
- **轉換上下文**：提供 `replaceNode`、`removeNode` 等節點操作介面
- **進入與退出**：支援後序遍歷（bottom-up），解決需要根據子節點決定父節點轉換的問題

## 15.5 將模板 AST 轉為 JavaScript AST
- **轉換目的**：瀏覽器只能執行 JavaScript，需要將模板結構轉換為 JavaScript 結構
- **轉換函式**：`transformText`、`transformElement`、`transformRoot`
- **JavaScript AST 節點**：FunctionDecl、CallExpression、StringLiteral、ArrayExpression 等

## 15.6 程式碼生成
- **生成原理**：根據 JavaScript AST 節點類型，呼叫對應的生成函式進行字串拼接
- **Context 管理**：使用 `code`、`push`、`indent`、`deIndent` 等方法管理程式碼生成過程
- **最終結果**：可執行的 JavaScript 渲染函數程式碼

</div>
