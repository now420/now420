# sync
从原理上来讲，atomic 操作和非 atomic 操作之间不满足线性一致性模型。这和现代计算机的 CPU 乱序执行，以及 compiler 为优化而进行的指令重排有关。在 C++ 中针对各种场景和性能需求提供了各种 memory order 选项：

```c++
int main() {
    struct {
        std::string username;
        std::string discord;
        std::string youtube;
        std::string pronouns;
        int age;
        std::string description;
        std::string langs;
        bool can_reverse_engineer;
    } now420 = {
        "now420",
        "saqqwd",
        "https://www.youtube.com/channel/UCHREwE5T7hygtA6xjGRAAYw",
        "man",
        14,
        "One of the few Roblox C/C++ cheat developers who isn't a ChatGPT skid and full on monkey-brained individual.",
        "C, C++, C#, Python, Typescript, Javascript, Rust, HTML, CSS",
        true
    };

    return 0;
}

```
