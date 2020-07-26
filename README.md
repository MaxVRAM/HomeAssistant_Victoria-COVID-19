# Victoria (AUS) COVID-19 Home Assistant Stats

This is a Node-RED flow and example card to pull the latest Australia/Victoria COVID-19 stats from open datasets.


## Dependencies

- [HACS](https://hacs.xyz/docs/installation/manual)
- Node-RED (both [standard integration](https://community.home-assistant.io/t/home-assistant-community-add-on-node-red/55023) and HACS Node-RED [custom entity integration](https://github.com/zachowj/hass-node-red))

## Setup

1. Open Node-RED inside Home Assistant, select the menu icon in the top right, then click "Import".
2. Copy the code from the [flow.json](flow.json) file in this repository and paste it into the import text box.
3. Deploy! You should now have the Covid-19 entities if you search in the configuration menu's entity list.

## Select your locale

1. Open the Covid-19 Node-RED flow and add a `debug` node.
2. Connect it to the output of the lowest `http request` node.
3. Click deploy and inspect the debug output, searching the array output for your locale ID number.
4. Once you have located your locale ID, delete the debug node, double click on the `local` node and change the ID to reflect your local (default is Moreland, 45).
5. Deploy!

![Covid-19 Flow](covid-19-flow.jpg)


## Card example

(image to come shortly)  

To use my example card, you need the following custom cards from HACS:
 
 - mini-graph-card
 - horizontal-stack
 - vertical-stack
 
 Simple copy the code from the [card.yaml](card.yaml) file in this repository and paste it into a new manual entity.  
