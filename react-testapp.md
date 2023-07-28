# Your first application with React.js

As a product team, we want to be sure about knowledge level of new developer

So that we are asking to build test application

## Acceptance criteria

1. Project should contains react project and testapp.html
2. testapp.html consist of
      1. Base HTML tags: head, body etc.
      2. Title "My first app"
      3. Paragraph about you: name, age, university name or job name
      4. Your favourite picture(your photo, photo of your pet, memes)
      5. Text field A
          1. User can enter only numbers
          2. Default value is 0
      6. Text field B
          1. User can enter only numbers
          2. Default value is 0
      7. The "Result:" text is placed after fields
           1. When user changes text field A or text field B, this text should be changed to "Result: X" where X - sum of A and B
3. React app based on Next.js and Chakra UI
4. React app consists of
      1. Card component from Chakra UI
      2. Has a title: A plus B
      3. Button "Click to add B"
      4. Result field with number
      5. When the user clicks on button, the result number should be increased 

## Mockup

### testapp.html
![image](https://github.com/takttusur/onboarding/assets/15832039/59d834c9-ea67-4456-9248-8765c1a6c64e)
### React app
![image](https://github.com/takttusur/onboarding/assets/15832039/0693e07c-84a3-49d0-81d4-fa2130c3de70)


## Out of scope
Some differences between results and mockup will not be a problem.
Commnications with backend, webpack config, extended css. 

## Technical details


### For React app

Start from template [https://nextjs.org/learn/basics/create-nextjs-app/setup](https://nextjs.org/learn/basics/create-nextjs-app/setup).
After this step you'll have `pages/index.js` file. Please, install Chakra UI (link below).

Add Chakra UI [https://chakra-ui.com/getting-started/nextjs-guide](https://chakra-ui.com/getting-started/nextjs-guide)

From ^^ you need only Installation and Provider Setup. After installing, open `pages/index.js`, find `<main>` and remove all content inside `<main> ... </main>`. Next, wrap ` <div className={styles.container}>` section in `<ChakraProvider>`. You'll get something like this:
```js
export default function Home() {
  return (
      <ChakraProvider>
          <div className={styles.container}>
            //.........
          </div>
      </ChakraProvider>
  )
}
```

Create you first component. Create new file `AplusB.js` in pages folder. Put in the file:
```js
export default function AplusB() {
    
    return <p>123</p>
}
```

Next, open `pages/index.js` add `import AplusB from "./AplusB";` to the top of file. Find `<main>... </main>` section and put `<AplusB></AplusB>` inside.
Start your app in terminal `npm run dev`.
You'll see this in browser:
![image](https://github.com/takttusur/onboarding/assets/15832039/3902d186-cc31-4191-9ba7-5b5df40082ac)

Now, you can continue doing the task at `AplusB.js`. Use links below:
1. [https://chakra-ui.com/docs/components/card/usage](https://chakra-ui.com/docs/components/card/usage)
2. [https://react.dev/reference/react/useState](https://react.dev/reference/react/useState)
