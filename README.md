# omikuji-go



```
vgrun -new-from-example=simple omikuji
```

--------------
```
go install github.com/vugu/vgrun@latest
vgrun -install-tools

go get github.com/vugu/vugu
go get github.com/vugu/vugu/cmd/vugufmt
```

## Tailwind CSS
### Install
```
npm init -y
npm install tailwindcss@latest postcss@latest autoprefixer@latest
```

### Generate Tailwind CSS setting file
```
npx tailwindcss init -p
```

### Create CSS file

```src/styles/main.css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### Add build script

```package.json
"scripts": {
"build:css": "tailwindcss -i ./src/styles/main.css -o ./dist/styles/tailwind.css --minify"
"watch:css": "tailwindcss -i ./dist/styles/main.css -o ./dist/styles/tailwind.css --watch"
}
```

### Build Tailwind CSS

```
npm run build:css
```

Watch Mode

```
npm run watch:css
```

## Create Makefile

```makefile
.PHONY: build

build:
	npm run build:css
	go build
```

## Go Build and Execution

```
go build
./omikuji-go 
```

