# iNews Gateway

The iNews Gateway communicates with an iNews system to ingest and remain in sync with a rundown.

### Installing iNews for Sofie

The iNews Gateway allows you to create rundowns from within iNews and sync them with the _Sofie Core_. The rundowns will update in real time and any changes made will be seen from within your Playout Timeline. 

The setup for the iNews Gateway is already in the Docker Compose file you downloaded earlier. Remove the _\#_ symbol from the start of the line labeled `image: olzzon/tv2-inews-ftp-gateway:develop` and add a _\#_ to the other ingest gateway that was being used.

Although the iNews Gateway is available free of charge, an iNews license is not. Visit [Avid's website](https://www.avid.com/products/inews/how-to-buy) to find an iNews reseller that handles your geographic area.

