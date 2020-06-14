# Example C++ code using Sentry

Written to a company this post: https://siedentop.dev/posts/sentry-cpp/

```cpp
#include <crow/crow.hpp>

int main(void) {
  nlohmann::crow sentry(
      "https://7c164e487bc24a0fadb32c461fc71764@sentry.io/1860700");

  sentry.capture_message("Hello, Sentry!");

  printf("Hello, World!\n");
}
```
