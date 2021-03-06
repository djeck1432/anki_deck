# Create anki cards and export it in .apkg

## How to install

```bash
pip3 install ankideck
```


## How it works
The first step is to create a new deck:

`deck` - is a deck of cards.

If you want to create new deck :
```python
deck = getEmptyCol()
```
 Add a new card:

`front` - it's the front side of the card

`back` - it's a backside of card. 

`answer` - it's an extra field for input type card.

`css` - it's a style of card.


```python
add_new_card(deck, front, back,
                css=None, explination=None)
```
If you want to add an image, you need to:

`image` - it's a binary format of the image

`name_deck` - it's a name of deck it will use for the name of the image.

`extension_image` - it's an extension for image.

```python
add_image(deck,image,name_deck='example',extension_image='.jpeg')
```

Export in .apkg extension:

`export_path` - it's the path where you will upload the file.

```python
export_ankipkg(deck,export_path)
```

# Examples
```python
def create_anki_cards():
    #create new deck
    deck = getEmptyCol()
    
    #add new baicCard to deck
    add_new_card(deck,front,back)
    
    #add new inputCard to deck with new css 
    add_new_card(deck,front,back,css=css, explination=explination)
    
    #upload image to media deck
    add_image(deck,image,image_name='expame',extension_image='.jpeg')
    
    #export deck in .apkg
    export_ankipkg(deck,export_path)
        
      
```