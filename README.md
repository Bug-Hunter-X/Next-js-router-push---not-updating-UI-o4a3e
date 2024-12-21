# Next.js router.push() UI Update Issue

This repository demonstrates a bug where `router.push()` in Next.js does not correctly update the UI after navigation.  The URL changes, but the content remains on the previous page.

## Steps to Reproduce

1. Clone the repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Navigate to the '/about' page.
5. Click the 'Go Back Home' button.

The URL will change to '/', but the content will remain as the '/about' page until a hard refresh is performed.

## Solution

The issue is resolved by using the `replace()` method of the `router` object instead of `push()`.  This prevents the previous page from being cached, which can cause the UI to stay unchanged after navigation.