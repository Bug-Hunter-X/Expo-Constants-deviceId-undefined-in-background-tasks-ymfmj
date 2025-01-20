# Expo Constants.deviceId Undefined in Background Tasks

This repository demonstrates a common issue when using Expo's `Constants.deviceId` within background tasks or services.  The problem arises because the device ID may not be readily available while the app is in the background due to OS-level restrictions.

**The bug:** Accessing `Constants.deviceId` within a background task can result in the value being `undefined` or `null`, leading to app crashes or unexpected behavior.  This repo shows how this can happen and provides a solution.

**The solution:** The solution involves checking if the `deviceId` is available *before* using it.  If it's undefined, the app handles this gracefully to avoid crashes.