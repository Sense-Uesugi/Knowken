# Knowken

**了解你的 Codex 用量。 · Understand your Codex usage. · Codex の使用量を確認。**

[下载 / Download / ダウンロード](https://github.com/Sense-Uesugi/Knowken/releases/latest)

## 简体中文

Knowken 1.8.0 · 开发者 Sense · Windows x64 / GNU/Linux x64 · 未签名

在本机按日期、模型、项目和任务查看 Codex Token 用量、API 估算费用或两者同时显示。支持简体中文、English、日本語、深浅色、字号和主题色；可导出当前筛选的 CSV，或保存默认隐藏任务和项目名称的分享图片。

### 1.8.0 新功能

- **代理树**：点击任务，在详情查看主／子会话自身用量、分支合计及贡献。分支沿用已有去重，筛选外祖先只补结构，不带入额外用量。
- **缓存与费用分析**：展开首页分析面板，查看缓存读取输入占比、普通输入、缓存读取、缓存写入与输出费用，以及相对标准输入价格的估算差额。
- **本地价格表**：设置中导入 JSON，核对预览后启用；可导出当前表、查看导入记录或恢复内置表。导入完整替换模型目录，未列模型保持未计价。
- **模型费用模拟**：用当前筛选下的同一批 Token，选择目标模型以及保留已记录缓存或全部输入按普通输入计价。差额为模拟金额减当前金额，不能保证实际节省或相同质量。
- **每月费用目标**：设置每月 USD 目标，查看页面内 80%／100% 状态与月底线性估算。按所选时区本月全部用量计算，独立于首页筛选；不提供系统通知或自动限额。

同时收入 1.7.1 的新模型精确价格更新；纯费用模式中项目按已知金额降序排列，完全未计价项目置后。

### 开始使用

从 [Releases](https://github.com/Sense-Uesugi/Knowken/releases/tag/v1.8.0) 下载对应系统的完整发行包，解压到当前用户可写的目录。Windows 双击 Knowken.exe；GNU/Linux 运行 ./Knowken，目录还需允许执行。无需单独安装 Node.js。操作与升级见 USAGE.txt，系统条件和启停见包内 README.md。

### 费用与本地数据

内置目录版本 **2026-10-03.1**，全部 33 个基础模型于 **2026-10-03** 核对，保留 21 个明确别名／快照。标准短上下文文本价格，单位为 **USD / 百万 Token**：

| Model | Input | Cache read | Cache write | Output |
| --- | ---: | ---: | ---: | ---: |
| gpt-6.1-sol | 2 | 0.1 | 2.5 | 10 |
| gpt-6-sol | 2 | 0.2 | 2.5 | 10 |
| gpt-6-luna | 0.1 | 0.01 | 0.125 | 0.5 |

价格不会联网自动更新。导入表的来源与日期由文件自述，应用校验格式与完整性，不认证价格来源；历史用量统一按当前启用目录重新估算，不重写日志。费用不是实际账单、订阅费用或官方账号额度，不还原历史价格、长上下文、服务档位、工具、地区及其他未记录附加费用。已记录缓存读取与写入分别计价，推理输出包含在输出内，不重复相加；缺失写入不作推断，0 不能证明实际无写入费。

未知金额显示“—”，部分覆盖显示已知下限“≥”，未计价不表示免费。缓存差额只对已计价输入比较，可以为负，不是实际节省。模拟使用固定 Token 假设，任何一侧覆盖不全时差额显示“—”。月底估算为本月已知金额 ÷ 已过日历天数（含今天）× 本月天数；覆盖不全时只是下限，跨阈值显示“至少”，不能证明未超目标。

Knowken 只读取本机现存 Codex 日志，不上传会话、用量或价格文件，也不跨设备同步。统计可能不完整。公开仓库只提供产品说明与第三方许可，应用通过 Releases 发行，源码不公开。

## English

Knowken 1.8.0 · Developed by Sense · Windows x64 / GNU/Linux x64 · Unsigned

Explore local Codex Tokens, estimated API costs or both by date, model, project and task. Chinese, English and Japanese, appearance preferences, filtered CSV exports and share images with task/project names hidden by default remain available.

### New in 1.8.0

- **Agent tree**: open a task to see each session's own usage, branch totals and contribution. Existing deduplication applies; ancestors outside the filter supply structure only.
- **Cache and cost analysis**: expand the home panel for cached-input share, regular input, cache reads, cache writes and output costs, and an estimated difference against standard input pricing.
- **Local price tables**: import JSON in Settings, review the preview, then activate. Export the current table, review import history or restore bundled prices. Imports replace the entire model catalog; omitted models remain unpriced.
- **Model cost simulation**: apply a target model to the same filtered Tokens, preserving recorded cache reads/writes or treating all input as regular input. The difference is simulated minus current cost; actual savings or equal quality are not guaranteed.
- **Monthly USD goal**: set a goal for in-page 80%/100% states and a linear month-end estimate. It uses all usage this month in the selected time zone, independently of home filters. It provides no system notifications or automatic usage cap.

Includes the 1.7.1 exact-model price update. In cost-only mode, projects sort by known cost descending, with fully unpriced projects last.

### Start and understand estimates

Download the complete package from [Releases](https://github.com/Sense-Uesugi/Knowken/releases/tag/v1.8.0), extract to a writable directory, and open Knowken.exe on Windows or run ./Knowken on GNU/Linux. The Linux location must permit execution. Node.js is included. See USAGE.txt for operations and upgrades, and the package README.md for system requirements and stopping.

Bundled catalog **2026-10-03.1** contains 33 base models checked on **October 3, 2026** and 21 explicit aliases/snapshots. The table above lists the three new models' regular input, cache read, cache write and output prices in **USD per million Tokens**. Prices use standard short-context text rates and are not refreshed online.

Imported source/date metadata is self-declared; format and integrity validation does not authenticate prices. All historical usage is re-estimated with the current catalog, without changing logs. Estimates are not actual bills, subscription fees or official account limits. Historical rates, long-context premiums, service tiers, tools, regional charges and other unrecorded costs are not reconstructed. Recorded cache reads/writes are priced separately; reasoning is already part of output. Missing cache writes are not inferred; zero does not prove no write charge occurred.

“—” means unknown; “≥” marks a known lower bound. Unpriced usage is not free. Cache differences cover priced input only and may be negative; they are not actual savings. Simulation holds Token counts fixed; its difference is unknown if either side has incomplete pricing. Month-end estimate = known monthly cost ÷ elapsed calendar days (including today) × days in the month. Partial coverage gives only a lower bound; threshold states say “at least” and cannot establish that usage is below the goal.

Knowken reads existing local Codex logs, uploads no conversations, usage or price files, and does not sync across devices. Results may be incomplete. The public repository contains product documentation and third-party licenses; the application is distributed through Releases and its source remains private.

## 日本語

Knowken 1.8.0 · 開発者 Sense · Windows x64 / GNU/Linux x64 · 未署名

端末内の Codex 使用量を日付・モデル・プロジェクト・タスク別に確認し、トークン、API 推定費用、両方の表示を選べます。中国語・英語・日本語、外観設定、絞り込んだ CSV 出力、タスク名とプロジェクト名を既定で隠す共有画像に対応します。

### 1.8.0 の新機能

- **エージェントツリー**：タスク詳細で各セッション自身の使用量、配下を含む合計と寄与を確認できます。既存の重複除外を維持し、絞り込み外の祖先は構造のみを補います。
- **キャッシュと費用の分析**：ホームのパネルでキャッシュ読み取り入力の割合、通常入力・読み取り・書き込み・出力の費用と、通常入力料金を基準とした推定差額を確認できます。
- **ローカル料金表**：設定で JSON を選択し、プレビュー確認後に有効化します。現在の表の出力、インポート履歴、内蔵料金への復帰に対応します。モデル一覧全体を置き換え、未掲載モデルは料金不明のままです。
- **モデル費用シミュレーション**：現在の絞り込みと同じトークン数に対象モデルの単価を適用します。記録済みキャッシュを維持するか、全入力を通常入力として計算します。差額はシミュレーション額 − 現在の推定額で、実際の節約や同等の品質は保証しません。
- **月間 USD 目標**：80%／100% のページ内表示と月末の線形推定を確認できます。選択したタイムゾーンの当月全使用量が対象で、ホームの絞り込みから独立しています。システム通知や利用制限はありません。

1.7.1 の正確なモデル名による料金更新も含みます。費用のみの表示では、プロジェクトを既知の費用の降順に並べ、全額不明の項目を最後に表示します。

### 起動と推定の範囲

[Releases](https://github.com/Sense-Uesugi/Knowken/releases/tag/v1.8.0) から対応パッケージを完全に展開し、書き込み可能な場所で Windows は Knowken.exe、GNU/Linux は ./Knowken を実行します。Linux では実行も許可されている必要があります。Node.js は同梱です。操作と更新は USAGE.txt、動作条件と停止はパッケージの README.md を参照してください。

内蔵料金表は **2026-10-03.1**、33 基本モデルの確認日は **2026 年 10 月 3 日**、明示的な別名／スナップショットは 21 件です。上の表は新しい 3 モデルの通常入力・キャッシュ読み取り・書き込み・出力の単価で、単位は **USD / 100 万トークン**です。標準の短コンテキスト・テキスト料金を用い、オンラインで自動更新しません。

インポートの出典と確認日はファイルの自己申告です。形式と整合性の検証は料金の認証ではありません。過去の使用量も現在の料金表で再計算し、ログは変更しません。実際の請求額、サブスクリプション料金、公式アカウント利用枠を示しません。過去の単価、長コンテキスト、サービス階層、ツール、地域料金、その他の未記録費用は再現しません。記録済みの読み取りと書き込みを別々に計算し、推論出力は出力に含めて二重加算しません。未記録の書き込みは推測せず、0 は書き込み料金がなかった証拠ではありません。

「—」は不明、「≥」は既知額の下限です。料金不明を無料として扱いません。キャッシュ差額は計算可能な入力のみを比較し、負になる場合もあり、実際の節約額ではありません。シミュレーションはトークン数を固定し、どちらかの料金が不完全なら差額は不明です。月末推定 = 当月既知額 ÷ 経過した暦日数（今日を含む）× 当月の日数。情報が不完全な場合は下限のみで、閾値表示は「少なくとも」となり、目標を下回るとは判断できません。

端末内の既存 Codex ログのみを読み取り、会話・使用量・料金ファイルを送信せず、端末間同期も行いません。集計が不完全な場合があります。公開リポジトリは製品説明と第三者ライセンスのみで、アプリは Releases で配布し、ソースは非公開です。
