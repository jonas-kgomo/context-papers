## High School Exams Dataset

This dataset provides information about high school exams, including exam names, subjects, scores, student information, and more. It serves as a valuable resource for educators, students, and researchers interested in analyzing academic performance at the high school level.
Exams span between 
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


For Conversion use https://github.com/adithya-s-k/marker-api 


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
