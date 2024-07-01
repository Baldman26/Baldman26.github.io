# Baldman26.github.io

poopie bum bum

[fraggle rock](https://www.youtube.com/watch?v=fxMMte0ya9w&list=PLLhOnau-tupSx7f-dlRzc0Q0OoEqpv9WV&index=2)


![don't press this](https://i.pinimg.com/originals/33/5d/9d/335d9d7725652e40ba8018f0730d96bf.gif)


[fish webpage](https://baldman26.github.io/noFishhere.html)






<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>AI Meme Generator</title>
</head>
<body>
    <h1>AI Meme Generator</h1>
    <div id="meme-container">
        <img id="meme-img" src="" alt="Meme Image">
        <p id="ai-quote"></p>
        <button id="generate-btn">Generate Meme</button>
    </div>

    <script src="script.js"></script>
</body>
</html>
const generateMeme = async () => {
    // 1. Fetch random image URL from Google (replace with actual API call)
    const imageUrl = await getRandomImageUrl();

    // 2. Fetch AI-generated quote (replace with your AI quote generation logic)
    const aiQuote = generateAIQuote();

    // 3. Update HTML elements
    const memeImg = document.getElementById('meme-img');
    const aiQuoteElem = document.getElementById('ai-quote');

    memeImg.src = imageUrl;
    aiQuoteElem.textContent = aiQuote;
};

// Example function to fetch random image URL (replace with actual implementation)
const getRandomImageUrl = async () => {
    // Implement logic to fetch random image URL from Google or another source
    // For example, you could use Google Custom Search API
    // Make sure to handle API key and request properly
    return 'https://example.com/random-image.jpg';
};

// Example function to generate AI quote (replace with actual implementation)
const generateAIQuote = () => {
    // Implement logic to generate AI quotes
    // This could involve calling an AI language model API or using pre-generated quotes
    return "AI-generated quote goes here.";
};

// Event listener for the Generate Meme button
document.getElementById('generate-btn').addEventListener('click', generateMeme);

// Initial meme generation on page load
generateMeme();


