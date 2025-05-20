# Smart FAQ Chatbot

A sophisticated chatbot that uses Natural Language Processing to match user questions with the most relevant answers from a predefined FAQ database. Built with TF-IDF vectorization and cosine similarity, this system can understand semantically similar questions even when they're phrased differently.

## Features

- **TF-IDF Vectorization** - Transforms text into numerical vectors
- **Cosine Similarity Matching** - Measures relevance between queries and FAQ questions
- **Comprehensive E-commerce FAQ Database** - 60+ pre-defined Q&As organized by category
- **Text Preprocessing** - Handles variations in query formatting
- **Configurable Similarity Threshold** - Adjustable matching strictness

## Requirements

- Python 3.6+
- NumPy
- scikit-learn

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/smart-faq-chatbot.git
cd smart-faq-chatbot

# Install required packages
pip install numpy scikit-learn
```

## Usage

### Basic Usage

```python
from faq_chatbot import FAQChatbot, faq_data, get_faq_answer

# To get an answer for a specific query
answer = get_faq_answer("How do I track my order?")
print(answer)
```

### Run Demo

```python
# Run the included demo with test cases
demo_chatbot()
```

### Custom FAQ Data

```python
# Define your own FAQ data
my_faq_data = {
    "What's your return policy?": "You can return items within 30 days.",
    "How do I contact support?": "Email us at support@example.com.",
    # Add more Q&A pairs
}

# Initialize a new chatbot with your data
from faq_chatbot import FAQChatbot
my_chatbot = FAQChatbot(my_faq_data)

# Get answers
def my_get_answer(query):
    return my_chatbot.get_answer(query)
```

## How It Works

1. **Preprocessing**: User queries are normalized (lowercase, punctuation removal)
2. **Vectorization**: TF-IDF converts questions into numerical vectors
3. **Similarity Calculation**: Cosine similarity determines the closest FAQ match
4. **Threshold Filtering**: Returns the best answer only if similarity exceeds threshold

## Categories in the Demo FAQ Database

- Delivery & Shipping
- Store Information
- Returns & Refunds
- Order Tracking & Management
- Payment & Pricing
- Customer Service
- Account Management
- Products & Services
- Loyalty Program & Promotions
- Technical Support

## Customization

- Adjust the similarity threshold in the `FAQChatbot` initialization
- Modify the TF-IDF parameters for different vectorization approaches
- Expand the FAQ data dictionary with your own questions and answers

## License

[MIT](LICENSE)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
