# CS361 Instructions

To programmatically request data from the microservice, you need to make a POST request to the /make_request endpoint with the item information you want to add. Here's an example using JavaScript's Fetch API:

fetch('/make_request', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json',
    },
    body: JSON.stringify(locations),
})
    .then(response => response.json())
    .then(data => {
        console.log('Response from microservice:', data['result']);
    })
    .catch(error => {
        console.error('Error:', error);
    });

To programmatically receive data from the microservice, you need to check the response from the /make_request endpoint.
