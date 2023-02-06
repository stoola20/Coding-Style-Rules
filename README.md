# Coding-Style-Rules
Common used rules for SwiftLint and SwiftFormat

## Setting Steps
1. Install SwiftLint and SwiftFormat by Homebrew
2. Select the project in the file navigator, then select the primary app target, and go to Build Phases. Click the + and select "New Run Script Phase". Insert the following as the script:

```
export PATH="$PATH:/opt/homebrew/bin"  // add this line if you run on Apple Silicon (M1, M2) 

if which swiftlint > /dev/null; then
  swiftlint
else
  echo "warning: SwiftLint not installed, download from https://github.com/realm/SwiftLint"
fi

if which swiftformat >/dev/null; then
  swiftformat .
else
  echo "warning: SwiftFormat not installed, download from https://github.com/nicklockwood/SwiftFormat"
fi
```

## Add the rules files to your project directory
> .swiftlint.yml

Rules for SwiftLint

> .swift-version

To specify the Swift version for SwiftFormat

> .swiftformat

Rules for SwiftFormat
