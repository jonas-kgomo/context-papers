## Papers Dataset

This dataset contains information about various papers including their titles, authors, publication dates, abstracts, and more. It is a valuable resource for researchers, scholars, and anyone interested in exploring academic publications.

### Dataset Overview

- **Total Records:** [Insert total number of papers here]
- **Fields Included:** Title, Authors, Publication Date, Abstract, Keywords, DOI, etc.
- **Source:** [Mention the source of the dataset if available](https://docs.ieb.co.za/)

Credentials
- https://docs.ieb.co.za/ 
Username: guest@ieb.co.za   |   Password: guest

### Potential Uses

1. Analyzing trends in research topics
2. Identifying influential authors in a specific field
3. Conducting text mining and sentiment analysis on paper abstracts
4. Building recommendation systems for related papers

Feel free to explore and analyze this dataset to extract valuable insights and knowledge from the world of academic papers.


More 

- Listening Comprehension [short audio files]
- International Benchmark 

``` javascript
const fetch = require('node-fetch');
const fs = require('fs');

const url = "http://localhost:8000/convert";
const pdfFilePath = "example.pdf";

fs.readFile(pdfFilePath, (err, pdfContent) => {
    if (err) {
        console.error(err);
        return;
    }

    const formData = new FormData();
    formData.append('pdf_file', new Blob([pdfContent], { type: 'application/pdf' }), pdfFilePath);
    formData.append('extract_images', true); // Optional parameter

    fetch(url, {
        method: 'POST',
        body: formData
    })
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
});
``` 
