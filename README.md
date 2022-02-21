# Positive Affirmations

I created this fetchable api to be used by whoever needs it to provide several positive affirmations in hopes that it may be used to remind others of their inherent worth. We all need more positivity in our lives and I hope this will help provide the mean to remind others of that.

## Fetch Random Affirmation
The below code can be used to fetch a random affirmation from this api using JS fetch:

const fetch = require('node-fetch');
<br />
const url = 'https://avyrie.github.io/affirmations-api/affirmations.json';
<br />
const randomNum = (arrLength) => {
<br />
    return Math.floor(Math.random() * arrLength)
<br />
}
<br />
const fetchData = () => {
<br />
    fetch(url)
<br />
    .then(response => response.json())
<br />
    .then(data => console.log(data.affirmations[(randomNum(data.affirmations.length))]))
<br />
    .catch(err => {
<br />
        console.log(err)
<br />
    })
<br />
}


## Contributing
Additional contributions are welcome. If you know of a positive affirmation that would be useful to add, please contribute to this open-source project.

Thank you to our current contributors:
<br />
<a href="https://github.com/avyrie/affirmations-api/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=avyrie/affirmations-api" />
</a>
