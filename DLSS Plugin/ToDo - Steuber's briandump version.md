- [ ] #todo Create a comprehensive list of everything the plugin needs to do and the order it has to do it in 📅 2023-08-18 




- Provide raw color buffer for each frame (in HDR or LDR/SDR space).
- Per pixel motion vector generation
- The depth buffer for the frame
- The exposure value (if processing in HDR space)

	
- Allow for sub-pixel viewport jitter and have good pixel coverage with at least 16 jitter phases (32 or more is preferred).
- Initialize NGX and DLSS using a valid ProjectID (See Section 5.2.1).
	- ProjectID is specific to third party engine i.e. in our case unity
- The ability to negatively bias the LOD for textures and geometry.



- query for DLSS support 
	- can happen before ngx object is initialized
	- see section 2.3
- Query for vulkan extensions
	- 2.3.1




### Def. of done type stuff

- Full production non-watermarked DLSS library (nvngx_dlss.dll) is packaged in the release build (see section 4.2)

- Game specific Application ID is used during initialization (see section 5.2.1) 

- Motion vectors for all scenes, materials and objects are accurate (see section 3.6) 

- Exposure value is properly sent each frame (or auto-exposure is enabled) (see section 3.9)

- Mip-map bias set when DLSS is enabled (see section 3.5)

- Static scenes resolve and compatible jitter confirmed (see section 3.7)

- DLSS modes are queried and user selectable in the UI (see section 3.2.1 and RTX UI Developer Guidelines) and/or dynamic resolution support is active and tested

