# Expo Linking API Issue with Special Characters in Deep Links

This repository demonstrates a bug in the Expo `Linking` API related to handling deep links with special characters in their query parameters.  When the app is launched via a deep link containing such characters, `Linking.getInitialURL()` may return `null` or an incomplete URL, leading to unexpected app behavior.

## Bug Reproduction

1. Clone this repository.
2. Run `npm install`.
3. Run the app on a physical device or emulator.
4. Open a deep link with special characters in query parameters (see example in `bug.js`).
5. Observe that the app does not correctly handle the deep link due to the `Linking.getInitialURL()` issue.

## Solution

The provided solution in `bugSolution.js` demonstrates how to properly handle URLs with special characters, using URL encoding to ensure accurate parsing by the Linking API.

## Contributing

Contributions to improve this example or provide alternative solutions are welcome.