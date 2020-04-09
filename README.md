# odata2openapi


## How to use it (from MAC):

- To generate an Openapi 3.0 JSON file starting from a metadata.xml file (in our example it's named *CatalogService.xml*), staying in the same folder where this file is located, run this command:
    `docker run --rm -v ${PWD}:/local sferriero/odata2openapi odata-openapi -dp /local/CatalogService.xml`
 
- To generate an Express NodeJS server in the folder named "output", starting from an Openapi 3.0 JSON file, remaining in the same folder where we have generated the previous file, run this command:

    `docker run --rm -v ${PWD}:/local sferriero /odata2openapi openapi-generator generate -i /local/CatalogService.openapi.json -g nodejs-express-server -o /local/output`
 