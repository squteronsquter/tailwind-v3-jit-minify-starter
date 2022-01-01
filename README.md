# tailwindcss JIT (just-in-time)

```
mkdir tailwind

cd tailwind

npm init -y
npm install -D tailwindcss@latest postcss@latest autoprefixer@latest

npx tailwindcss init

```

## package.json

```
{

...
  "scripts": {
    "dev": "npx tailwindcss -o style.css --watch",
    "prod": "npx tailwindcss -o style.css --minify"
  },

...

}

```

## tailwind.config.js (tailwind V3)

```
module.exports = {
  mode: 'jit',
  content: [
    './*.html',
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}

```

## generate your tailwind.css file

```
npx tailwindcss -o style.css --watch

```

## create an index.html file in the root directory

```
touch index.html

html:5

link:css style.css

```

## open the preview window and add some tailwind classes in your html

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Tailwind JIT</title>
</head>
<body class="bg-gray-900">
    <main class="max-w-sm m-auto">
    <h1 class="text-4xl font-semibold text-center mt-5 text-cyan-500">Hello Tailwind</h1>
    <div class="mt-10 ">
            <img src="img/logo.svg" alt="Logo">
    </div>
    <p class="mt-10 text-cyan-500 text-left">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Dignissimos sunt quam consectetur ipsum quas omnis sed. Facilis debitis labore, hic iste earum quidem eveniet autem in distinctio itaque possimus voluptates!</p>
    </main>
</body>
</html>

```

| You can check the tailwind colors straight from VS Code (Shift+Cmd+P)

While you are coding with --watch flag all classes you are using are kept in memory (JIT) when you stop and relaunch only those classes are kept in memory which ae in the code now, those you swapped from time to time trying eg. different colors are gone

## minify your tailwind.css file

```
npx tailwindcss -o style.css --minify

```

## use package.json scripts to run your development or production builds

```
npm run dev

npm run prod

```

## that's all for now
