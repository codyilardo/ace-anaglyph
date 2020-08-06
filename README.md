# Notes

paulbourke.net/stereographics/anaglyphs

## Options

1. Write a python script for OBS that processes the two video feeds. Need to somehow seperate left and right footage. 

Scene API Reference (obs_scene_t)
Utilize the Scene API

Check out:
https://obsproject.com/docs/reference-core.html

obs_display_t *obs_display_create(const struct gs_init_data *graphics_data)
void obs_display_resize(obs_display_t *display, uint32_t cx, uint32_t cy)

https://obsproject.com/docs/reference-scenes.html?highlight=crop#c.obs_sceneitem_crop



2. Configure (within OBS) for the edits for the images, and export as a profile. 
    - Duplicate the stream
    - crop each
    - stack each on top of eachother
    - with Left:
        - turn off G and B
    - with Right:
        - turn off R
    - blending mode? 

Rfinal = Rleft
Gfinal = Gright
Bfinal = Bright