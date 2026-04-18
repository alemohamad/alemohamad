```swift
//
//  AleMohamad.swift
//  GitHub
//

struct AleMohamad: AppleDeveloper {
    let name: String = "Alejandro Mohamad"
    let mainLanguage: ProgrammingLanguage = .swift
    let tools: [String] = ["Xcode", "Swift Playground"]
    let platforms: [Platform] = [.iOS, .iPadOS, .macOS, .tvOS, .watchOS, .visionOS]
    let backendFrameworks = ["Vapor"]
    
    var website: URL { URL(string: "https://alemohamad.com")! }

    // What I build with ☕️ and Swift
    var appIdeas: [Platform: String] {
        platforms.reduce(into: [:]) { result, platform in
            result[platform] = "🚀 Coding an app for \(platform.name)..."
        }
    }
    
    func developApp(for platform: Platform) -> String {
        appIdeas[platform] ?? "🤔 That platform isn't on my radar... yet!"
    }
    
    func buildBackend(using framework: String) -> String {
        backendFrameworks
            .first(where: { $0 == framework })
            .map { "⚙️ Backend API using \(framework)..." }
            ?? "❌ Framework \(framework) is not in my toolbox!"
    }
    
    func dailyRoutine() -> [String] {
        ["Brew coffee", "Open Xcode", "Code", "Repeat"]
            .enumerated()
            .map { "Step \($0 + 1): \($1)" }
    }
}
```
