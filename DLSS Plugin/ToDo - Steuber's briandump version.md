- [ ] #todo Create a comprehensive list of everything the plugin needs to do and the order it has to do it in 📅 2023-08-18 


1. Initialize NGX - Thadd
2. Ensure correctly sized frame buffers - connor/thadd
	1. generate two sets - 
		1. full res (game res)
		2. sub game res(75% or whatever the scaling for dlss is)
3. Initialize memory for motion vectors - connor/thadd
	4. size of frame buffer determined by ngx and quality set by user and resolution
4. Initialize memory for scratch buffers
5. Set up render passes for motion vectors (Shader that outputs movement with respect to time for all pixels) - colin
6. Start frame things
7. Update cameras location so that it jitters (0 or almost 0 visible movement) (Us OR hijack jitter from TAA)
	1. random (research)
	2. does it need to repeat? (Research)
8. Begin rendering (unity)
	1. generate depth buffer (Unity)
	2. Run motion vector pass (Us)
	3. DLSS feature eval (Us)
	4. copy results into larger frame buffer (Us or NGX, research)
	5. throw it back into the URP (Us or automatic)
9. Proceed to next frame



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

