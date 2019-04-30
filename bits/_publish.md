An item of type `electronMicroscope` would be published similar to:

```json
{
  "publisher": "FloAddress",
  "payment": "freeeee",
  "details": {
    "basic": {
      "name": "BigJoe",
      "description": "The biggest baddest microscope in the lab"
    },
    "electronMicroscope": {
      "electronCount": 9001
    },
    "microscope": {
     "maxMagnification": 9001
    },
    "hardware": {
      "serial": "123-456-7890",
      "manufacturer": ["acme"]
    }
  }
}
```


If one wants to obtain all microscopes it's now possible to search
 `details.microscope` and it will return all variants regardless of type
 
 
Similarly an `electronMicrograph` could be published as:

```json
{
  "publisher": "FloAddress",
  "payment": "freeeee",
  "details": {
    "electronMicrograph": {
      "magnification": 7,
      "takenBy": "DaviTxid"
    },
    "image": {
     "height_px": 1200,
     "width_px": 1200,
     "ppi": 1000000
    },
    "file": {
      "location": "hash",
      "network": "ipfs"
    }
  }
}
```

A wallpaper site that wishes to load all images can search
 `details.image` and now have all the information necessary
 to display a simple image while ignoring anything under
 `details.electronMicrograph`