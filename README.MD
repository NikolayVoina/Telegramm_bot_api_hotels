# Telegram bot for hotel search

This bot allows you to find hotels according to your search criteria.

Link to the bot: https://t.me/niceee2meetbot.

## Bot functionality

With this bot, you can:

- Find hotels based on the lowest or highest price.
- Find hotels based on the best price-to-distance ratio from the city center.
- Request search history.

For each hotel, the bot displays the following data:

- Hotel name.
- Hotel website.
- Hotel address.
- Distance from the city center in kilometers.
- Stay period entered by the user.
- Accommodation cost for a specific period.
- Accommodation cost per night.

## Requirements

pyTelegramBotAPI==4.4.0
python-dotenv==0.19.2
pip~=21.1.2
certifi~=2022.6.15
requests~=2.28.1
loguru~=0.6.0

To install the above libraries, run the following command: `pip install -r requirements.txt`

## Bot commands

- /start - Launches the bot, automatically executed when connecting to the bot.
- /help - List of commands and their descriptions.
- /lowprice — Displays the cheapest hotels in the city.
- /highprice — Displays the most expensive hotels in the city.
- /bestdeal — Displays hotels that are the best deal in terms of price and distance from the center.
- /history — Displays search history.

### Telegram bot command descriptions

#### Search for the cheapest hotels (/lowprice)

1. Upon entering the /lowprice command, the bot asks for the city where you want to find hotels.
2. Next, the user enters the name of the locality. The bot will make a request to the hotels API and display a list of locations whose names are similar to the entered city. If the bot does not find any location, you need to enter the city name again; perhaps the user made a mistake when entering it.
3. Next, the number of hotels to display is requested.
4. Then the user selects the check-in and check-out dates.
5. After determining the check-in and check-out dates, the bot asks the user if they want to display hotel photos.
6. If the answer is positive, the bot sends the user an album (in case there is more than 1 photo) of photos with information (see above) for each hotel found.

#### Search for the most expensive hotels (/highprice)

1. Upon entering the /highprice command, the bot asks for the city where you want to find hotels.
2. Next, the user enters the name of the locality. The bot will make a request to the hotels API and display a list of locations whose names are similar to the entered city. If the bot does not find any location, you need to enter the city name again; perhaps the user made a mistake when entering it.
3. Next, the number of hotels to display is requested.
4. Then the user selects the check-in and check-out dates.
5. After determining the check-in and check-out dates, the bot asks the user if they want to display hotel photos.
6. If the answer is positive, the bot sends the user an album (in case there is more than 1 photo) of photos with information (see above) for each hotel found.

#### Search for the best deals (/bestdeal)

1. Upon entering the /bestdeal command, the bot asks for the city where you want to find hotels.
2. Next, the user enters the name of the locality. The bot will make a request to the hotels API and display a list of locations whose names are similar to the entered city. If the bot does not find any location, you need to enter the city name again; perhaps the user made a mistake when entering it.
3. Next, the number of hotels to display is requested.
4. Then the user sets the price range and the distance value from the city center in km.
5. Then the user selects the check-in and check-out dates.
6. After determining the check-in and check-out dates, the bot asks the user if they want to display hotel photos.
7. If the answer is positive, the bot sends the user an album (in case there is more than 1 photo) of photos with information (see above) for each hotel found.

#### Request search history (/history)

Upon entering the /history command, the user receives the history of ALL their queries.
