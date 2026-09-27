# Contributing to Vid2Cam

Thank you for your interest in contributing to Vid2Cam! This document provides guidelines for contributing to the project.

## 🚀 Getting Started

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/camera-app.git
   cd camera-app
   ```
3. **Create a branch** for your feature:
   ```bash
   git checkout -b feature/your-feature-name
   ```

## 🛠️ Development Setup

### Prerequisites
- Android Studio or VS Code with Android extensions
- Android SDK 24+ 
- Java 8+
- Physical Android device (camera functionality requires real hardware)

### Building
```bash
cd android-app
./gradlew assembleDebug
adb install -r app/build/outputs/apk/debug/app-debug.apk
```

### Testing
```bash
# View logs during testing
adb logcat | grep Vid2Cam

# Test on multiple devices if possible
# Test with/without permissions granted
# Test camera switching and all features
```

## 📝 Code Style

### Java Guidelines
- Use **Java 8** compatible syntax
- Follow **Google Java Style Guide**
- Use **meaningful variable names**
- Add **comprehensive logging** with appropriate log levels:
  ```java
  Log.d(TAG, "Debug message");
  Log.w(TAG, "Warning message");  
  Log.e(TAG, "Error message", exception);
  ```

### Android Guidelines
- Use **Material Design** components
- Handle **all lifecycle events** properly
- Implement **proper error handling**
- Use **scoped storage** for Android 10+ compatibility
- Always check and request **runtime permissions**

### Example Code Structure
```java
private void someMethod() {
    Log.d(TAG, "Starting someMethod");
    
    try {
        // Your code here
        Log.d(TAG, "Operation successful");
    } catch (Exception e) {
        Log.e(TAG, "Error in someMethod", e);
        // Handle error appropriately
    }
}
```

## 🐛 Bug Reports

When reporting bugs, please include:

1. **Device information** (model, Android version)
2. **App version** 
3. **Steps to reproduce** the issue
4. **Expected behavior**
5. **Actual behavior**
6. **Logs** if available (`adb logcat | grep Vid2Cam`)
7. **Screenshots/videos** if helpful

## ✨ Feature Requests

For new features:

1. **Check existing issues** to avoid duplicates
2. **Describe the feature** clearly
3. **Explain the use case** and benefits
4. **Consider implementation complexity**
5. **Provide mockups/examples** if applicable

## 🔄 Pull Request Process

### Before Submitting
1. **Test thoroughly** on physical device
2. **Update documentation** if needed
3. **Add/update comments** in code
4. **Ensure no crashes** or major bugs
5. **Test permission flows**

### Pull Request Checklist
- [ ] Code follows project style guidelines
- [ ] Self-review completed
- [ ] Comments added for complex logic
- [ ] Documentation updated
- [ ] Tested on physical device
- [ ] No crashes or major bugs
- [ ] Camera functionality works properly
- [ ] Permissions handled correctly

### PR Description Template
```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing
- [ ] Tested on physical device
- [ ] Tested camera functionality
- [ ] Tested permissions
- [ ] Tested on Android X.X

## Screenshots/Videos
(if applicable)
```

## 🎯 Areas for Contribution

### High Priority
- **Bug fixes** - Always welcome
- **Performance improvements**
- **Camera stability** enhancements
- **Permission handling** improvements
- **UI/UX enhancements**

### Medium Priority  
- **New camera features** (manual controls, burst mode)
- **Video enhancements** (stabilization, effects)
- **Overlay improvements** (real-time muxing)
- **Testing** and device compatibility

### Low Priority
- **Code refactoring** 
- **Documentation** improvements
- **Build system** enhancements

## 🚫 What Not to Contribute

- **Breaking changes** without discussion
- **Major architectural changes** without approval
- **Features that compromise privacy/security**
- **Dependencies** that significantly increase APK size
- **Code that doesn't follow project standards**

## 🤝 Community Guidelines

- **Be respectful** and constructive
- **Help others** when possible
- **Follow the code of conduct**
- **Ask questions** if unsure
- **Provide context** in discussions

## 📞 Getting Help

- **GitHub Issues** - For bugs and feature requests
- **GitHub Discussions** - For questions and general discussion
- **Code Review** - Tag maintainers for review

## 🏆 Recognition

Contributors will be:
- **Listed in CONTRIBUTORS.md**
- **Mentioned in release notes** for significant contributions
- **Given credit** in documentation

Thank you for contributing to Vid2Cam! 🎉