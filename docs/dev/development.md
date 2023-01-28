<h1 class=title>Development</h1>

<blockquote id="attention">
    <span>Attention!</span>
    <p>Only follow these instructions if you want to modify the app.<br>Otherwise, please <a href="https://github.com/ProjectBlackPearl/project_black_pearl/releases/latest">download the app from GitHub.</a></p>
</blockquote>

## Prerequisites

The following software is required in order to build the app:

-   [Node.js](https://nodejs.org/en/download/)
-   [Rustup](https://rustup.rs/)
-   [Cargo](https://crates.io)
-   [Yarn](https://yarnpkg.com/)

## Setup

1. Install `yarn`

```
npm install yarn -g
```

2. Clone the repo

```
git clone https://github.com/ProjectBlackPearl/project_black_pearl.git ./PBP
```

3. Enter into the created directory

```
cd PBP
```

4. Install the packages

```
yarn install
```

5. Run the project

```
yarn tauri dev
```