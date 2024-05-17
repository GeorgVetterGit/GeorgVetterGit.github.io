# Judge a Book by its Color

![Thumbnail](/assets/book_visualisation/pictures/title.png)<br>

__Introduction__<br>
In this project, I investigated how the main colors of bestsellers have appeared over the past decades, whether there are visibly dominant main colors among bestsellers, and how these main colors can be visualized. This question is of great importance as it provides insights into the visual design of book covers and reveals potential trends over the years. By visualizing the main colors, one can draw conclusions about the book market and gain valuable insights into how book covers should be designed to be successful.

__Data Scraping__<br>
For the investigation, I used data on book titles, authors, and the periods in which the books were ranked first on the bestseller list. This data was sourced from Wikipedia. The book covers were scraped from various online sources. The data was obtained through web scraping, extracting all relevant information about the bestsellers from the respective sources.

__Data Wrangling__<br>
The scraped data had to be first converted into a structured form. It turned out that the data was partially inconsistent and needed manual cleaning. Periods were corrected, and missing image data was supplemented from additional sources.

__Visualization__<br>
For visualizing the main colors of the bestsellers, I opted for an appealing and simple representation. The visualization was designed in the form of a bookshelf, with each shelf representing a year and each book in the shelf representing a week. The color of each book corresponds to the main color of the respective bestseller for that week. To make the visualization more interesting, the heights and widths of the book spines were randomly varied.

__What I learned__<br>
Through this project, I learned how to create appealing visualizations using simple methods in Matplotlib. Additionally, I scraped and processed image data for the first time, which is valuable experience for future projects.

__Further Work__<br>
While the current visualization answers some basic questions and meets aesthetic requirements, it provides room for further analysis. Future steps could include investigating the influence of colors on the success of bestsellers, analyzing color trends in different genres, and examining changes in the average duration that a book holds the top position.