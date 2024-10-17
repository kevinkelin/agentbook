# 简介

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.


## python code 

```python
@router.post("/query")
async def query(
        query: graphrag.GraphQueryModel,
        graphragService: GraphragService = Depends(GraphragService)
):
    user = "yangyanxing@360.cn"
    result = await graphragService.query(query.query, query.dataset_ids, user, prompt=query.prompt)
    return ResponseModel(data=result)
```
