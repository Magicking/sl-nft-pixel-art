# NFT Street Ware NFT


## Attributes

      UI Editor                   UI Editor
    .#############              #############
    .#           #              #   _/ \_   #
    .#    ###    #    canvas    #    ###    #
    .#   #   #   #  /        \  #   #   #   #
    .#  # x x #  # /          \ #  # x x #  #
    .#  #  _ >=8 # Attribute    #  #  _  #  # Attribute    
    .#   #   #   # popularities #   #   #   # popularities 
    .#    ###    # [ 42 ] [PAY] #    ###    # [ 100 ] [PAY] 
    .#           #  6 copies    #           # 100 copies    
    .#############              #############
     scissor attribute          hat attribute

Attribute definition:
 - Name
 - Royalties (0x42 / 10%)
 - Graphic:
   - X (relative to pos ref)
   - Y (relative to pos ref)
   - PosRef (Eye{R;L} / Ear{R;L} / ...)
   - Compressed (DEFLATE) bitmap 

Attribute price x Popularity share

    ################
    # 100-------+  #
    #  .       /|  #
    #  .      / |  #
    #  .     /  |  #
    # 42----+   |  #
    #  .   /|   |  #
    #  .  / |   |  #
    #  . /  |   |  #
    #  1/   |   |  #
    #  #1...6...10 #
    ################

## Minting

The mint operation combines multiple attributes and creates a new NFT

    #############
    #   _/ \_   #
    #    ###    #
    #   #   #   #
    #  # x o #  #
    #  #  _ >=8 #
    #   #   #   #
    #    ###    #
    #    (x,y,z)#
    #############
      scissor+hat
      attributes
          w/
     x.o background

Mint:
 - Random background selected or depending the season
 - Choose attributes (or randomly using popularities share)
 - Pay fees
Display:
 - Render on-chain (BMP/GIF/PNG)

Fees on:
 - Mint
 - Transfer
 - Attribute creation
