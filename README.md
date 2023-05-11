# Full VideoPlayer
 
<div>
This is a full option videoplayer made with js.This player will fullfill
everything that you need from a web videoplayer.Such as: Subtitles,Multile Audio,
using different episodes of a series,Different video qualitiy.
The code is simple and adjustable.

## Installation
-[Intializing Player](#intializing-the-player)
-[Usage](#usage)
-[Arguments and Options](#arguments-and-options)

## Intializing the Player
Usage in html file:
```html
<script type="module">
    import { Player } from 'player/player.js';
    let options;
    const player = new Player('player', options);
</script>
```

## Usage
This player wont work with video source as usual.You have to set the video source through the options. So here is the most simple option list.You can know more about optional options in options section.

##### Single Video:

```json
{
    "src" : "Video Source",
    "audios" : [
        {   
            "src" : "Audio source",
            "label" : "Audio Language Label"
        }
    ], 
    "subtitles":[
        {
            "src" : "Subtilte Source",
            "src" : "Subtitle Label",
        }
    ]
}
```

##### Multiple Video:
```json
{
    "collections" : [
        {
            "src" : "Video Source",
            "audios" : [
                {   
                    "src" : "Audio source",
                    "label" : "Audio Language Label"
                }
            ], 
            "subtitles":[
                {
                    "src" : "Subtilte Source",
                    "src" : "Subtitle Label",
                }
            ]
        }
    ]
}
```


## Arguments and Options 
Here are the arguments that you can pass on to the class.

##### Arguments
| Key              | Description                                          | Value Type  | optional |
|:---------------- | :----------------------------------------------------|:------------|:---------|
| element_id       | The id of the video element that you want initialize | `String`    | False    |
| options          | The options that you declared already                | `Dict`      | False    |

##### Options
You can use the options below for a single video and multiple videos. If you want to use multiple videos,
just put the options for all of them in a list named `Collections`;

| Key              | Description                                          | Value Type     | optional |
|:---------------- | :----------------------------------------------------|:---------------|:---------|
| src              | The video path                                       | `String`       | False    |
| audios           | The audios that you wanna use on video               | `List<Audio>`  | True     |
| Subtitles        | The subtitles that you wanna use on video            | `List<Subtile>`| True     |

Note: Subtiltes should be in vtt structure.

###### Subtilte options
| Key              | Description                                          | Value Type  | optional |
|:---------------- | :----------------------------------------------------|:------------|:---------|
| src              | The path of subtitle                                 | `String`    | False    |
| label            | The label that you wanna appear on item              | `String`    | False    |

###### Audio options
| Key              | Description                                          | Value Type  | optional |
|:---------------- | :----------------------------------------------------|:------------|:---------|
| src              | The path of subtitle                                 | `String`    | False    |
| label            | The label that you wanna appear on item              | `String`    | False    |
