```swift
//
//  AleMohamad.swift
//  GitHub
//

struct AleMohamad: AppleDeveloper {
    let name: String = "Alejandro Mohamad"
    let mainLanguage: ProgrammingLanguage = .swift
    let tools: [String] = ["Xcode", "Swift Playgrounds"]
    let platforms: [Platform] = [.iOS, .iPadOS, .macOS, .tvOS, .watchOS, .visionOS]
    let backendFrameworks: [String] = ["Vapor"]
    
    var website: String {
        "https://alemohamad.com"
    }
    
    var bento: String {
        "https://bento.me/alemohamad"
    }
    
    func developApp(for platform: Platform) -> String {
        "🚀 Coding an app for \(platform.name)..."
    }
    
    func buildBackend(using framework: String) -> String {
        backendFrameworks.contains(framework) ?
            "⚙️ Backend API using \(framework)..." :
            "❌ Framework \(framework) is not in my toolbox!"
    }
}
```
