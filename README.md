## Hello! I’m Howard, and here is some background on me… 👋🏻 👋

● 📚 Data Analytics bootcamp graduate (April 2022, Juno College)  
● 💾 Skilled in Excel / Sheets, SQL, Tableau, Python, Adobe (Lightroom/Photoshop/Premiere)  
● ⛺️ Google Data Analytics Certificate  
● 💎 4+ years of Data Analytics & Account Management experience gained in Tech Industry  
● 👔 Strengths: communication, Teamwork, attention to detail, mentorship  
● 👍 I’m a people-person! I enjoy relationship building and team collaboration  
● 📄 My resume can be found [here](https://drive.google.com/file/d/1ic52fY_1GA07X86AvN0AM5KzHHAu6pbW/view?usp=sharing)

● ⚡ Quick fact: I'm an avid PC enthusiast and gamer. I mostly play FPS and MMORPG games.

## Connect with me
### LinkedIn - https://www.linkedin.com/in/howardlin118/



name: Latest blog post workflow
on:
  schedule: # Run workflow automatically
    - cron: '0 * * * *' # Runs every hour, on the hour
  workflow_dispatch: # Run workflow manually (without waiting for the cron to be called), through the Github Actions Workflow page directly

jobs:
  update-readme-with-blog:
    name: Update this repo's README with latest blog posts
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v2
      - name: Pull in dev.to posts
        uses: gautamkrishnar/blog-post-workflow@master
        with:
          feed_list: "https://dev.to/feed/gautamkrishnar,https://www.gautamkrishnar.com/feed/"
