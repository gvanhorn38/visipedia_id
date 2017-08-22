# Visipedia ID Dataset Tools

## Format

```
{
  "info" : info,
  "images" : [image],
  "categories" : [category],
  "annotations" : [annotation],
  "licenses" : [license]
}

info{
  "year" : int,
  "version" : str,
  "description" : str,
  "contributor" : str,
  "url" : str,
  "date_created" : datetime,
  "schema_version" : str
}

image{
  "id" : str,
  "width" : int,
  "height" : int,
  "file_name" : str,
  "license" : int,
  "url" : str,
  "rights_holder" : str,
  "user_id" : str
}

category{
  "id" : int,
  "name" : str, 
  "rank" : str,
  "supercategory" : str,
  "keypoints" : [str],
  "keypoints_style" : [str],
  "skeleton" : [edge],
  
  "gbif_key" : int,
  "kingdom" : str,
}

annotation{
  "id" : int,
  "image_id" : str,
  "category_id" : int,
  "segmentation" : RLE or [polygon],  // normalized?
  "area" : float,                     // normalized?
  "bbox" : [x1,y1,x2,y2],             // normalized?
  "iscrowd" : 0 or 1,
  "keypoints" : [x1,y1,v1,...],       // normalized?
  "num_keypoints" : int,
  "annotator_id" : int                //?
}

# Group multiple images together? 
observation{
  "id" : str,
  "image_ids": [image_id]
}
```
