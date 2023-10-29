import openai

# Set your OpenAI GPT-3 API key
api_key = 'YOUR_API_KEY'

# Function to generate a story based on the user's description
def generate_story(description):
    prompt = f"Create a funny story about {description}."
    response = openai.Completion.create(
        engine="text-davinci-002",
        prompt=prompt,
        max_tokens=150,
        api_key=api_key
    )
    return response.choices[0].text

# Function to play the Mad Libs game
def play_mad_libs(description):
    story = generate_story(description)
    blanks = []
    for i in range(1, 26):
        user_input = input(f"Fill in the blank #{i}: ")
        story = story.replace(f"___{i}___", user_input, 1)
    print("\nHere's your funny story:")
    print(story)

if __name__ == "__main__":
    print("Welcome to the Mad Libs game!")
    user_description = input("What will the short story be about? ")
    play_mad_libs(user_description)
