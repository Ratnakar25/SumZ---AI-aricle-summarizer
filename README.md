
<h1>Demo Photo</h1>
<img src="demo-photo.png" width='50%' />

<h1>Article Summarizer Application</h1>
This project is a web application that allows you to summarize any article using OpenAI’s GPT model. You can enter the URL of an article or paste the text in the input area and get a concise summary in seconds. You can also copy the summary to your clipboard or save it to your local storage for later use.

<h2>How to run this project</h2>
To run this project, you need to have Node.js and npm installed on your machine. You also need an OpenAI API key, which you can get from here.

<ul>
<li>Clone this repository to your local machine.</li>
<li>Navigate to the project directory and run npm install to install the dependencies.</li>
<li>Create a .env file in the root directory and add your OpenAI API key as VITE_RAPID_API_ARTICLE_KEY=sk-....</li>
<li>Run npm run dev to start the development server.</li>
<li>Open your browser and go to http://localhost:3000 to see the application.</li>
</ul>

<h2>How this project works</h2>
This project uses React as the front-end framework, Vite as the build tool, and Tailwind CSS as the styling library. It also uses RTK Query as the data fetching library and OpenAI as the AI service provider.
The main component of this project is App.js, which renders the input area, the summary area, and the history area. The input area allows you to enter the URL or text of an article and submit it to the API. The summary area displays the generated summary and provides options to copy or save it. The history area shows the list of previous summaries and allows you to delete them.

The logic for fetching data from the OpenAI API is handled by openaiApi.js, which uses RTK Query to create an API service with endpoints for creating chat completions and summarizing texts. The endpoints use the openai.Completion.create method from the openai package to send requests to the OpenAI API with different parameters.

The logic for saving data to the local storage is handled by storage.js, which uses the localStorage object to store and retrieve data as JSON strings. The data is stored as an array of objects, each containing a unique id, a timestamp, a source, and a summary.

The logic for handling form events and catching errors is handled by useForm.js, which is a custom hook that takes an initial state and a callback function as arguments and returns an object with values, errors, handleChange, handleSubmit, and resetForm properties. The values property holds the current state of the form inputs, the errors property holds any validation errors, the handleChange property is a function that updates the values and errors on input change, the handleSubmit property is a function that calls the callback function on form submit, and the resetForm property is a function that resets the values and errors to their initial state.

The logic for implementing copy to clipboard is handled by useClipboard.js, which is another custom hook that takes a text value as an argument and returns an object with copied and copyText properties. The copied property is a boolean that indicates whether the text has been copied or not, and the copyText property is a function that copies the text to the clipboard using the navigator.clipboard.writeText method.

The UI design of this project follows a glass morphism style, which creates a frosted glass effect using CSS filters and backdrop filters. The main colors used are blue, white, and gray, creating a contrast between the background and the foreground elements.

## Technologies Used

### Fronend

- React
- JavaScript
- Tailwind CSS (for styling)

### State Management

- Redux (for managing application state)

### Build Tools

- Vite (for faster build times)

### APIs

- OpenAI API (for GPT-4 integration)
- RapidAPI (for additional functionalities)

## Features

- URL Log: Maintains a history of previously entered URLs, which users can copy or revisit for past summaries
- Database Integration: Stores past URLs and summaries, allowing users to easily access previous entries
- Aesthetic Design: Features a minimalistic design with gradient fonts
- Responsiveness: Designed to be mobile-friendly and adaptable to various screen sizes

## Background

With the rise of generative AI, I saw an opportunity to improve upon the existing UI of AI tools. I began by brainstorming what I used ChatGPT the most for. As a student, I use ChatGPT for its capabilities in summarizing content but found its UI lacking. This led to my creation of Sumz.ai, combining the robust capabilities of GPT-4 with a user-friendly and visually appealing interface.

## Notes

This project marks my first integration of OpenAI's API into a web app. Furthermore, it marks the foundation for some of my future projects that I plan on using generative AI to enhance user productivity.

