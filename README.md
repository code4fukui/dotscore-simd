# dotscore-simd

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

A SIMD-optimized C++ library for fast dot product calculations, ideal for text similarity and recommendation systems.

## Features

- **High Performance:** SIMD-accelerated dot product computation using SSE2 and AVX2.
- **Automatic Detection:** Automatically detects the available CPU instruction set at runtime to use the fastest implementation.
- **Batch Processing:** Parallelized computation for efficiently processing multiple vectors.
- **Flexible Data Types:** Supports 32-bit floating-point (`float`) and 8-bit integer (`int8_t`) vectors.

## Requirements

- C++17 compatible compiler
- CPU with SSE2 instruction set support (AVX2 recommended for best performance)

## Usage

1.  Clone the repository:
    ```bash
    git clone https://github.com/taisukef/dotscore-simd.git
    ```

2.  Build the library and link it in your project.

3.  Include the header and call the `dotproduct` function:
    ```cpp
    #include <dotscore/dotscore.hpp>
    #include <vector>

    std::vector<float> vec1 = {1.0f, 2.0f, 3.0f, 4.0f};
    std::vector<float> vec2 = {5.0f, 6.0f, 7.0f, 8.0f};

    float result = dotscore::dotproduct(vec1, vec2);
    ```

## License

MIT License — see [LICENSE](LICENSE).