# Instagram_caption_and_image_generator
Creates Captions and Images
Inputs
• Data Gathering:
• {Topic URL}: Provide a valid URL of a tweet or webpage containing the main theme for the reel.
• {Details}: Optionally, include additional context, opinions, or personal experiences related to the topic.
Use variables to store the inputs
topic_url = input("Provide a valid URL of a tweet or webpage containing the main theme for the reel: ") details = input("Optionally, include additional context, opinions, or personal experiences related to the topic: ")
Process
• URL Validation: The system will confirm the validity of the {Topic URL}. If the URL is invalid, the system will request a valid input. Once validated, the system will open the URL in a separate tab for analysis.
Use indexing to access specific portions of the inputs
keywords = topic_url.split(“/”)[-1] # get the last part of the URL as keywords context = details.split(“.”) # split the details by sentences
• Data Extraction: The system will extract information from {Details} if provided. If not available, the system may request additional input or proceed without it.
Use search queries to get up to date information from various sources
news_source = “#search_query " + keywords + " news” # get a news source related to the keywords social_media_source = “#search_query " + keywords + " social media” # get a social media source related to the keywords other_source = "#search_query " + keywords # get another source related to the keywords
• Instagram Analytics: Bing AI will analyze your Instagram account at https://www.instagram.com/nojaydenx/ and compare it with top accounts in your niche to identify the most engaging content types and incorporate these insights into the caption creation process. The goal is to make your Instagram Reel post informative and credible and improve the quality of the caption, engagement, viewership, accuracy, and content.
Use Web Pilot plugin to automate the process of opening and analyzing your Instagram account and other accounts in your niche
web_pilot.open(“https://www.instagram.com/nojaydenx/”) # open your account web_pilot.analyze(“engagement”, “content_type”, “hashtags”) # analyze your account metrics web_pilot.compare(“https://www.instagram.com/explore/tags/ukraine/”) # compare your account with top accounts in Ukraine niche
 
Process
• Caption Generation: Using Bing AI, a caption will be generated that respects the provided guidelines. Each element will be checked for compliance with the constraints.
Use a function to generate a caption based on the inputs and the guidelines
def generate_caption(topic_url, details, guidelines):
code for generating a caption that respects the guidelines
return caption
Use Bing News Search plugin to get the latest news topics related to your niche and use them as the inputs for the caption
bing_news_search.search(“ukraine”) # search for news topics related to Ukraine topic_url = bing_news_search.get_url() # get the URL of the first news topic details = bing_news_search.get_snippet() # get the snippet of the first news topic caption = generate_caption(topic_url, details, guidelines) # call the function with the inputs and the guidelines Guidelines
• Caption Guidelines: The generated caption will adhere to the following criteria:
• Language and Region: The caption will be in en-US.
• Character Limit: The caption will not exceed 2200 characters.
• Sources: The caption will reference up to 3 sources, including at least 1 news source and 1 social media source. Keywords from {Topic URL} and {Details} will be used to sort sources by date, relevance, and popularity. The information will be cross-referenced with {Topic URL} and {Details}.
• Caption Elements: The caption will include a title, emoji, description, question, quote, and call to action. Additional optional elements may include location, flag, question mark, quotation mark, arrow, tagging, hand, support, heart emoji, and hashtags, prioritized by importance. You can also include your Patreon link (https://www.patreon.com/nojaydenx) or ask your viewers to show support via your link in your bio as an optional element.
• Style and Tone: The style and tone of the caption will be factual, professional, and authoritative. It will use clear and concise language and avoid jargon and slang. It will also use active voice and positive words whenever possible.
• Caption Editing: The caption will be edited and formatted using Grammarly and Hemingway Editor to check for errors and ensure compliance with Instagram’s guidelines.


- Cover Photo Creation: Using Bing AI, a cover photo will be created that matches the caption topic and has a Use Grammarly and Hemingway Editor plugins to edit and format your caption
grammarly.edit(caption) # edit your caption with Grammarly hemingway.format(caption) # format your caption with Hemingway Editor
• Markdown Usage: Emphasis, hyperlinks, and emojis as separators will be applied using markdown formatting while respecting the character limit.
Use markdown formatting to add emphasis, hyperlinks, and emojis to your caption
This is a title
😎 This is an emoji This is a link This is emphasis Output
• Caption Formatting: The final caption will be formatted with double line breaks between sections and enclosed within a code block using three backticks (`) at the start and end, yielding a ready-to-use Instagram Reel caption.
Use a code block to enclose your caption with three backticks (`) at the start and end
• Cover Photo Creation: Using Bing AI, a cover photo will be created that matches the caption topic and has a title of the topic. The cover photo will use realistic imagery that will use the same lettering and structure and format each time.
Use a function to create a cover photo based on the caption topic and title
def create_cover_photo(caption_topic, caption_title):
code for creating a cover photo that matches the caption topic and has a title of the topic
return cover_photo
cover_photo = create_cover_photo(caption_topic, caption_title) # call the function with the caption topic and title
Use Bing Image Creator plugin to generate realistic imagery for the cover photo
try: bing_image_creator.generate(caption_topic) # generate realistic imagery for the cover photo except:
Use Bing Image Search plugin to search for an image related to the caption topic and use it as the cover photo
bing_image_search.search(caption_topic) # search for an image related to the caption topic cover_photo = bing_image_search.get_image() # get the first image from the search results
Use Bing Image Resizer plugin to resize the image to fit the Instagram cover photo format
bing_image_resizer.resize(cover_photo, 1080, 1920) # resize the image to 1080 pixels wide and 1920 pixels high
Use Bing Image Editor plugin to add bold dynamic lettering on the front of the image
bing_image_editor.add_text(cover_photo, caption_title, “Arial”, “Bold”, “White”, “Centered”) # add text with Arial font, bold style, white color, and centered position
Use Bing Video Downloader plugin to download the video from Twitter
bing_video_downloader.download(topic_url) # download the video from Twitter video = bing_video_downloader.get_video() # get the downloaded video
Use Bing File Sharing plugin to upload the cover photo and the video to a cloud storage service and generate download links
bing_file_sharing.upload(cover_photo, “instagram_reel_cover.png”) # upload the cover photo as a PNG file cover_photo_link = bing_file_sharing.get_link() # get the download link for the cover photo
bing_file_sharing.upload(video, “instagram_reel_video.mp4”) # upload the video as a MP4 file video_link = bing_file_sharing.get_link() # get the download link for the video
Use Bing Image Viewer plugin to display the cover photo in the conversation
bing_image_viewer.display(cover_photo) # display the cover photo in the conversation
Use Bing Video Player plugin to play the video in the conversation
bing_video_player.play(video) # play the video in the conversation




