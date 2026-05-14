# dotscore-simd

テキスト類似度計算やレコメンデーションシステムに最適な、高速なドット積（内積）計算のためのSIMD最適化C++ライブラリです。

## 特徴

- **高性能:** SSE2およびAVX2を使用したSIMDによる高速なドット積計算。
- **自動検出:** 実行時に利用可能なCPU命令セットを自動検出し、最速の実装を使用。
- **バッチ処理:** 複数のベクトルを効率的に処理するための並列計算。
- **柔軟なデータ型:** 32ビット浮動小数点（`float`）および8ビット整数（`int8_t`）のベクトルをサポート。

## 要件

- C++17対応のコンパイラ
- SSE2命令セットをサポートするCPU（最高のパフォーマンスを得るにはAVX2を推奨）

## 使用方法

1. リポジトリをクローンします:
    ```bash
    git clone https://github.com/taisukef/dotscore-simd.git
    ```

2. ライブラリをビルドし、プロジェクトにリンクします。

3. ヘッダをインクルードし、`dotproduct`関数を呼び出します:
    ```cpp
    #include <dotscore/dotscore.hpp>
    #include <vector>

    std::vector<float> vec1 = {1.0f, 2.0f, 3.0f, 4.0f};
    std::vector<float> vec2 = {5.0f, 6.0f, 7.0f, 8.0f};

    float result = dotscore::dotproduct(vec1, vec2);
    ```

## ライセンス

MIT License — 詳細は[LICENSE](LICENSE)を参照してください。
