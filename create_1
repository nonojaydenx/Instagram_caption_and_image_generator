# Import NLTK library to use stopwords module  
import nltk  
nltk.download('stopwords')  
from nltk.corpus import stopwords  
  
# Import web_pilot plugin to enhance web search and query functionality  
import web_pilot  
  
# Import gpt_3 library to use OpenAI's GPT-3 natural language generation model  
import gpt_3  
  
# Import instagram_format library to use Instagram's formatting options for captions and cover photos  
import instagram_format  
  
# Import image_generator library to use different image generation models, such as StyleGAN, BigGAN, or CLIP  
import image_generator  
  
# Import image_editor library to use different image editing options, such as cropping, resizing, rotating, or adding filters or stickers  
import image_editor  
  
# Import image_previewer library to preview the generated image before sending it to the chat  
import image_previewer  
  
# Import image_saver library to save or share the generated image on social media platforms, such as Instagram, Facebook, or Twitter  
import image_saver  
  
# Import bing_image_viewer library to display images in the chat box  
import bing_image_viewer  
  
# Define a function to get user inputs  
def get_user_inputs():  
  # Prompt user to enter topic URL  
  topic_url = input("Enter the topic: ")  
  # Prompt user to enter any additional details  
  details = input("Enter any additional details: ")  
  # Prompt user to enter any keywords  
  keywords = input("Enter any keywords: ").split(",")  
  # Prompt user to enter the context or purpose  
  context = input("Enter the context: ")  
  # Prompt user to enter the tone  
  tone = input("Enter the tone: ")  
  # Prompt user to enter the style  
  style = input("Enter the style: ")  
  # Prompt user to enter the personality  
  personality = input("Enter the personality: ")  
  # Prompt user to enter the format  
  format = input("Enter the format: ").split(",") 
  # Prompt user to enter the resolution
  resolution = input("Enter the resolution: ")
  # Prompt user to enter the quality
  quality = input("Enter the quality: ")
  # Prompt user to enter the style
  style = input("Enter the style: ")
  # Prompt user to enter the textures
  textures = input("Enter the textures: ").split(",")
  # Prompt user to enter the feedback
  feedback = input("Enter the feedback: ")
  # Prompt user to enter Instagram account URL
  ig_account_url = input("Enter your Instagram account URL: ")
  # Prompt user to choose an image generation model
  image_model = input("Choose an image generation model from StyleGAN, BigGAN, or CLIP: ")
  # Prompt user to customize the image generation parameters
  image_params = input("Customize the image generation parameters (number of images, diversity, style transfer, color scheme): ").split(",")
  # Convert all inputs to lowercase
  topic_url = topic_url.lower()
  details = details.lower()
  keywords = [keyword.lower() for keyword in keywords]
  context = context.lower()
  tone = tone.lower()
  style = style.lower()
  personality = personality.lower()
  format = [item.lower() for item in format]
  resolution = resolution.lower()
  quality = quality.lower()
  style = style.lower()
  textures = [texture.lower() for texture in textures]
  feedback = feedback.lower()
  ig_account_url = ig_account_url.lower()
  image_model = image_model.lower()
  image_params = [param.lower() for param in image_params]
 Remove any stop words from the inputs 
stop_words = set(stopwords.words('english')) 
topic_url = ' '.join([word for word in topic_url.split() if word not in stop_words]) 
details = ' '.join([word for word in details.split() if word not in stop_words]) 
keywords = [word for word in keywords if word not in stop_words] 
context = ' '.join([word for word in context.split() if word not in stop_words]) 

Combine all inputs into one string 
input_string = f'{topic_url} {details} {" ".join(keywords)} {context}' 

Create a dictionary of user inputs 
user_inputs = { 
"topic_url": topic_url, 
"details": details, 
"keywords": keywords, 
"context": context, 
"tone": tone, 
"style": style, 
"personality": personality, 
"format": format, 
"resolution": resolution, 
"quality": quality, 
"style": style, 
"textures": textures,
"feedback": feedback,
"ig_account_url": ig_account_url,
"input_string": input_string,
"image_model": image_model,
"image_params": image_params
} 

# Define a function to generate the content type
def generate_content_type(user_inputs):
  # Use web_pilot to search for relevant information based on the user's inputs and sources
  web_pilot.search(user_inputs["input_string"], sources = [user_inputs["topic_url"]])
  # Use gpt_3 to generate the caption based on the user's inputs and sources, and the web search results
  caption = gpt_3.generate_caption(user_inputs, web_pilot.results)
  # Use image_generator to generate the image based on the user's inputs and sources, and the web search results
  image = image_generator.generate_image(user_inputs, web_pilot.results)
  # Use image_editor to edit or modify the image based on the user's preferences
  image = image_editor.edit_image(image, user_inputs)
  # Use image_previewer to preview the image before sending it to the chat
  image_previewer.preview_image(image)
  # Use bing_image_viewer to display the image in the chat box
  bing_image_viewer.display_image(image)
  # Use instagram_format to format the caption and the image according to Instagram's standards
  instagram_format.format_caption(caption)
  instagram_format.format_image(image)
  # Use image_saver to save or share the image on social media platforms, such as Instagram, Facebook, or Twitter
  image_saver.save_image(image, user_inputs["ig_account_url"])
  image_saver.share_image(image, user_inputs["ig_account_url"])
  # Return the caption and the image as the final output
  return caption, image

# Call the get_user_inputs function to get the user's inputs
user_inputs = get_user_inputs()

# Call the generate_content_type function to generate the content type based on the user's inputs
caption, image = generate_content_type(user_inputs)

# Print the caption and display the image in the chat box
print(caption)
bing_image_viewer.display_image(image)
