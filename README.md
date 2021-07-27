# Dark Matter
A Mapbox GL basemap style useful for data visualizations. The cartography is based on the
[CartoDB Dark Matter Basemap](https://github.com/CartoDB/CartoDB-basemaps) and it is using the vector tile
schema of [OpenMapTiles](https://github.com/openmaptiles/openmaptiles).

## Edit the Style

Use the [Maputnik CLI](http://openmaptiles.org/docs/style/maputnik/) to edit and develop the style.
After you've started Maputnik open the editor on `localhost:8000`.

```
maputnik --watch --file style.json
```

## Sprites Generation

The `dolomate/spritezero` docker image was used for sprite generation:
as described in [https://github.com/macteo/spritezero-docker](https://github.com/macteo/spritezero-docker)

```
mkdir -p data/sprites
cp -r icons data/sprites
docker run -it -e FOLDER=_svg -e THEME=sprite -v ${PWD}/data:/data dolomate/spritezero
```

Sprites are then moved toplevel.

## License

- [ ] Clarify license
