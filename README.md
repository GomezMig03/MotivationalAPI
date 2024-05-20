# What is this?

This is a public api using github pages for the Final Higher Education Project of Multiplatform Application Development. It consist of a series of motivational phrases to help the people using the app, [which is an addiction manager](https://addiction-helper.vercel.app/). 

# Can I contribute?

Absolutely! feel free to add your favourite phrases whether they are religoius or not. Use the religion camp on the json to clarify it. 1 = catholic, 0 = non religious.
You can also add new translations or fixing possible errors on the current ones.

We are not currently accepting web contributions. There are plans to migrate the documentation to Vue, which may affect the process in the future.

# Can I use this for my project?

Yes you can, you can also fork this and use it however you want.

# How can I use this API

Simply make a HTTP request to
```https://gomezmig03.github.io/MotivationalAPI/[language].json```

The current languages codes are the following:
 * English = en
 * Spanish = es
 * French = fr
 * Japanese = ja

## Example of an HTTP request to get a random phrase and author on javascript
```
fetch('https://gomezmig03.github.io/MotivationalAPI/en.json')
        .then(response => {
          if (!response.ok) {
            throw new Error('Unable to retrieve data from the server.');
          }
          return response.json();
        })
        .then(data => {
          const randomIndex = Math.floor(Math.random() * data.length);
          const phrase = data[randomIndex].phrase;
          const author = data[randomIndex].author
          console.log(('quote').textContent = `"${phrase}" - ${author}`);
        })
        .catch(error => {
          console.error('Error:', error);
        });
```
