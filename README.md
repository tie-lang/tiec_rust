# tiec_rust

**tie 璇█鐨?Rust 鍙傝€冪紪璇戝櫒 / 绉嶅瓙缂栬瘧鍣紙bootstrap seed锛?*

> 鈿狅笍 **鍘嗗彶淇濈暀浠撳簱**锛氳嚜涓?v2 瀹屾垚鍚庯紝tie 鐨勬寮忕紪璇戝櫒 `tiec` 宸茬敤 tie 璇█鑷韩
> 閲嶅啓锛堣 [TIE-LANG](https://github.com/houyangbaoxin2009/TIE-LANG) 鐨?> `compiler/` 鐩綍锛歵ie 鑷啓鍓嶇/IR 鐢熸垚/瑙ｉ噴鍣級銆傛湰浠撳簱淇濈暀 Rust 鐗堝伐鍏烽摼锛?> 浣滀负绉嶅瓙缂栬瘧鍣紙`target/release/tie-llvm.exe` 缂栬瘧鍑虹涓€鐗?tiec锛変笌鍙傝€冨疄鐜般€?
## Crate 缁撴瀯

| Crate | 鑱岃矗 |
| --- | --- |
| `tie-prep` | 棰勫鐞嗭細娓呯悊浠ｇ爜銆佹彁鍙栧ご銆佽瘑鍒枃浠惰鑹诧紙logic/ui/db/data/library锛?|
| `tie-frontend` | 鍓嶇锛氳瘝娉曪紙鍚?ASI锛夆啋 璇硶 鈫?璇箟锛堢鍙疯〃/绫诲瀷妫€鏌ワ級+ import 灞曞紑 |
| `tie-llvm` | 涓+鍚庣椹卞姩锛欰ST 鈫?LLVM IR 鏂囨湰鐢熸垚锛涜皟鐢?opt/clang/lld |
| `tie-lsp` | 璇█鏈嶅姟鍣細JSON-RPC 2.0 over stdio锛堣瘖鏂?/ hover / 璺宠浆 / 琛ュ叏锛?|
| `tie-interp` | 瑙ｉ噴鎵ц锛氭爲閬嶅巻姹傚€?AST + C ABI 妗ワ紙staticlib锛孯EPL 鑷妇鏍稿績锛?|
| `tie` | CLI 涓诲叆鍙ｏ細瑙掕壊鍒嗘淳璋冨害鍣?+ REPL + 鍗忚皟缁熺 |

## 鏋勫缓

```bash
cargo build --release
# 浜у嚭锛?#   target/release/tie-llvm.exe    缂栬瘧鍣紙绉嶅瓙锛?#   target/release/tie-interp.lib  瑙ｉ噴鍣ㄩ潤鎬佸簱锛圕 ABI 妗ワ級
#   target/release/tie.exe         鎬诲叆鍙?CLI
#   target/release/tie-prep.exe    棰勫鐞?#   target/release/tie-frontend.exe 鍓嶇涓夐樁娈?#   target/release/tie-lsp.exe     璇█鏈嶅姟鍣?```

## 浣跨敤锛堢瀛愮紪璇戝櫒锛?
```bash
target/release/tie-llvm.exe <input.tie> -o <out.exe>   # 缂栬瘧閫昏緫绋嬪簭
target/release/tie-llvm.exe <lib.tie> -o <lib.a>       # 缂栬瘧闈欐€佸簱锛坱ie:library锛?```

## 涓庤嚜涓?tiec 鐨勫叧绯?
```
Rust 绉嶅瓙锛坱ie-llvm.exe锛屾湰浠撳簱锛?   鈹斺攢 缂栬瘧 compiler/driver.tie 鈫?tiec.exe   鈫?bootstrap 鐣岄檺
        鈹斺攢 tiec 缂栬瘧鐢ㄦ埛绋嬪簭 / tie 鑷啓杩愯鏃讹紙std/runtime.a锛夆啋 0-Rust 璺緞
```

## 璁稿彲璇?
MIT
