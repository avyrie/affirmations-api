# Positive Affirmations

I created this fetchable api to be used by whoever needs it to provide several positive affirmations in hopes that it may be used to remind others of their inherent worth. We all need more positivity in our lives and I hope this will help provide the mean to remind others of that.

## Fetch Random Affirmation
The below code can be added to fetch a random affirmation from this api:

const fetch = require('node-fetch');
const url = 'https://avyrie.github.io/affirmations-api/affirmations.json';
const randomNum = (arrLength) => {
    return Math.floor(Math.random() * arrLength)
}
const fetchData = () => {
    fetch(url)
    .then(response => response.json())
    .then(data => console.log(data.affirmations[(randomNum(data.affirmations.length))]))
    .catch(err => {
        console.log(err)
    })
}


## Contributing
Additional contributions are welcome. If you know of a positive affirmation that would be useful to add, please contribute to this open-source project.