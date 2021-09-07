# movies_Dapp_design

Movie dApp

Each movie will have a unique moveid_id token with its name and symbol based on ERC20 standard

Investors can buy and trade with the Movie_id token

Functions: 

create_movie: the msg.sender can create a unique token with (name, symbol) and the total supply will be assigned to him

invest : stakeholders can buy/ trade movie tokens ( either through exchange or token swap protocols)
 
buy_tickets : spectators will buy a specified amount of tokens to access the movie contents, and this will lead to a rally in the token price (by requiring a higher value or higher number of other tokens to purchase the movie token)
				similarly the advertisers will have to buy the tokens at a specified rate to take part in advertising in the movie

Producers, directors, actors can be provided the movie tokens upfront of after release, could be a specified amount or a percentage of tokens, as defined by the movie owner

In the newly created ERC20 movie token, a daily/weekly/monthly/as defined by owner withdrawal limit can be placed, to prevent market crashes.

Gas optimization : In the above approach minimal storage use will be needed as the entire transfer and trade of ownership will be done using the tokens. 
					There is no need for storing any records as the tokens themselves will represent as the records.
					A minimal storage (mapping (address => bool)) can be added in the dApp to know if a spectator has done the one time payment/ rent fees to access the movie, and hence wont require to purchase further tokens.