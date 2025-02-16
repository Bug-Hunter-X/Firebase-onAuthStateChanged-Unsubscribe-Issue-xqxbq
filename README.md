# Firebase onAuthStateChanged Unsubscribe Issue

This repository demonstrates a common issue with Firebase's `onAuthStateChanged` listener: improper unsubscription leading to memory leaks.  The provided code shows how to correctly unsubscribe to avoid this issue.

## Problem
The original `onAuthStateChanged` listener is not properly unsubscribed when the component unmounts, resulting in continued execution even after the component is destroyed. This causes memory leaks and can lead to unexpected behavior.