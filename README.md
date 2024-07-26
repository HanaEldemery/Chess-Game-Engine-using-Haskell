# Chess Game Engine using Haskell
I implemented part of the engine for a chess game using Haskell. This project required creating functions to initialize a chess board, visualize the board, move pieces according to their movement rules, and suggest possible legal moves for any piece on the board. The primary focus was on implementing the core functionalities while adhering to the rules of chess, with a few simplifications, such as no pawn promotions and allowing the king to move into threatened positions.
I started by defining the necessary types and data structures, including Location, Player, Piece, and Board. Location represented a cell on the chess board, indexed by a column letter and a row number. Player distinguished between the white and black players. Piece was represented by data constructors for each type of chess piece, along with their locations on the board. The Board type encapsulated the current player, the list of white pieces, and the list of black pieces.
The first function I implemented was setBoard, which initialized the chess board to its standard starting configuration. This function did not take any inputs and returned a Board with the white and black pieces in their initial positions. By ensuring that the first turn was always assigned to the white player, I established the foundation for simulating a chess game.
Next, I developed the visualizeBoard function to provide a visual representation of the board. This function took a Board as input and returned a string that displayed the board's state. Black pieces were suffixed with 'B' and white pieces with 'W'. The function formatted the board into an 8x8 grid, making it easy to understand the current positions of all pieces and indicating whose turn it was.
The isLegal function was then implemented to check the legality of a move. This function took a piece, a board, and a target location as inputs and returned True if the move was legal and False otherwise. It considered the specific movement rules of each piece and ensured that moves adhered to these rules.
Building on isLegal, I created the suggestMove function, which generated a list of all possible legal moves for a given piece on the board. This function helped in identifying potential moves a player could make, aiding in the development of game strategies.
Finally, I implemented the move function, which executed a move if it was legal. This function took a piece, a target location, and a board as inputs and returned an updated board after applying the move. If the move was illegal, it raised an appropriate error. This function was crucial for simulating the progression of the game and ensuring that each move followed the chess rules.
Through this project, I leveraged Haskell's functional programming features to create a robust and efficient chess game engine. The system I developed allowed for initializing, visualizing, and manipulating a chess board while enforcing the rules of chess and providing a foundation for further development of a complete chess game.
