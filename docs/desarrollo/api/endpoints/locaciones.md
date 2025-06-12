## ARCHIVO ENDPOINT locations.py

### Endpoints
#### {platform_id}/paises/{country_id}/estados/{state_id}/localidades
Valida las credenciales de acceso, ejecuta la función <a href="../../../../../desarrollo/api/funciones/locaciones/#get_locations_by_country_state"> 
    <strong>get_locations_by_country_state</strong>
  </a> y retorna los resultados.
#### {platform_id}/paises/{country_id}/estados/{state_id}/municipios
Valida las credenciales de acceso, ejecuta la función <a href="../../../../../desarrollo/api/funciones/ciudades/#get_cities_by_country_state"> 
    <strong>get_cities_by_country_state</strong>
  </a> y retorna los resultados.
#### {platform_id}/paises/{country_id}/estados
Valida las credenciales de acceso, ejecuta la función <a href="../../../../../desarrollo/api/funciones/estados/#get_states_by_country"> 
    <strong>get_states_by_country</strong>
  </a> y retorna los resultados.
#### {platform_id}/paises
Valida las credenciales de acceso, ejecuta la función <a href="../../../../../desarrollo/api/funciones/paises/#get_countries"> 
    <strong>get_countries</strong>
  </a> y retorna los resultados.