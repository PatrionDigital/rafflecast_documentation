# Farcaster - SIWF

## Signing into App with Farcaster

* [Farcast Documentation](https://docs.farcaster.xyz/auth-kit/installation)

## Things to Be Careful Of

Using Vite (which Farcaster recommends in their documentation) does have an issue.

Some dependencies from Node have been removed causing warnings in the browser console.

The main one seems to be "Buffer", and it will cause errors in the Farcaster login.

To fix this follow these steps:

1. Install buffer\
   `npm install buffer`
2.  Edit index.html (in the project root) to add the following javascript:

    ```xml
    <!-- node // buffer-->
    <script>window.global = window;</script>
    <script type="module">
        import { Buffer } from "buffer/";
       
        window.Buffer = Buffer;
    </script>
    ```

