
library(tidyverse)
library(lubridate)

infracciones_muy_graves <- multas %>% filter(Calificacion == "Muy Grave",
                                   !is.na(LONGITUD),
                                   !is.na(LATITUD))

# Ejemplo marcador
library(leaflet)
m <- leaflet(data = infracciones_muy_graves)  %>%
              addTiles() %>%  # Añade por defecto los Tiles de  OpenStreetMap
              addCircleMarkers(lng = ~LONGITUD, lat = ~LATITUD, 
                         fill = TRUE, 
                         color = 'red',
                         stroke = FALSE,
                         radius = 10,
                         fillOpacity = 0.5)
m  # Imprime el mapa


