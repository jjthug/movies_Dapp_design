# movies_Dapp_design

Movie dApp

Each movie will have a unique moveid_id token with its name and symbol based on **ERC20 standard**

Investors can buy and trade with the Movie_id token

**##Storage:**
movie_id_tracker : increments each time a movie is created and will be assigned as the movieId on this dApp
mapping (address => bool) to store if advertiser has paid for advertising their content on the movie (of movieId).
Movie struct with movie name, movie token_name, owner, movieId 

**##Functions:**

* create_movie: the msg.sender can create a unique token with (name, symbol) and the total supply will be assigned to him (the movie token can be created on a separate contract nheriting from ERC20 and its constructor will be called with the name , symbol, withdrawal limit, withdrawal time period limit )

* invest : stakeholders can buy/ trade movie tokens ( either through exchange or token swap protocols)
 
* buy_tickets : spectators will buy a specified amount of tokens to access the movie contents, and this will lead to a rally in the token price (by requiring a higher value or higher number of other tokens to purchase the movie token)
				
* advertiserPayment:similarly the advertisers will have to buy the tokens at a specified rate to take part in advertising in the movie

* assign tokens: The movie owner can assign a percentage or fixed amount of tokens to actors, producers and directors
				
				
**##Usage specification:**
Producers, directors, actors can be provided the movie tokens upfront of after release, could be a specified amount or a percentage of tokens, as defined by the movie owner

Spectatots will have to pay a fees (in movie tokens) to access/download the movie.
In the newly created ERC20 movie token, a daily/weekly/monthly/as defined by owner withdrawal limit can be placed, to prevent market crashes.

Gas optimization : In the above approach minimal storage use(access, load) will be needed as the entire transfer and trade of ownership will be done using the tokens. 
					There is no need for storing any records as the tokens themselves will represent as the records.
					Minimal storage (mapping (address => bool)) can be added in the dApp to know if a advertiser has done the one time payment/ rent fees to access the movie, and hence wont require to purchase further tokens.