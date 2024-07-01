# Baldman26.github.io

poopie bum bum

[fraggle rock](https://www.youtube.com/watch?v=fxMMte0ya9w&list=PLLhOnau-tupSx7f-dlRzc0Q0OoEqpv9WV&index=2)


![don't press this](https://i.pinimg.com/originals/33/5d/9d/335d9d7725652e40ba8018f0730d96bf.gif)


[fish webpage](https://baldman26.github.io/noFishhere.html)






// Function to fetch a random image URL using Google Custom Search API
const fetchRandomImage = async () => {
    const apiKey = 'YOUR_API_KEY'; // Replace with your Google API key
    const searchEngineId = 'YOUR_SEARCH_ENGINE_ID'; // Replace with your Google Custom Search Engine ID
    const query = 'random image'; // You can adjust the query as needed

    const url = `https://www.googleapis.com/customsearch/v1?key=${apiKey}&cx=${searchEngineId}&q=${encodeURIComponent(query)}&searchType=image`;

    try {
        const response = await fetch(url);
        if (!response.ok) {
            throw new Error('Network response was not ok');
        }
        const data = await response.json();
        if (data.items && data.items.length > 0) {
            const randomImage = data.items[Math.floor(Math.random() * data.items.length)];
            return randomImage.link; // Return the direct link to the image
        } else {
            throw new Error('No image results found');
        }
    } catch (error) {
        console.error('Error fetching random image:', error);
        return null;
    }
};
const generateMeme = async () => {
    try {
        // 1. Fetch random image URL from Google Custom Search API
        const imageUrl = await fetchRandomImage();

        // 2. Fetch AI-generated quote (replace with your AI quote generation logic)
        const aiQuote = generateAIQuote();

        // 3. Update HTML elements
        const memeImg = document.getElementById('meme-img');
        const aiQuoteElem = document.getElementById('ai-quote');

        memeImg.src = imageUrl;
        aiQuoteElem.textContent = aiQuote;
    } catch (error) {
        console.error('Error generating meme:', error);
    }
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


