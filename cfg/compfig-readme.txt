// ---------------------------
// '~~~ mastercomfig exec ~~~'
// ---------------------------

// This ZIP installation method is not recommended. Use it only if you know what you're doing!!!

// You can find more info at the bottom of the
// file for things like maximum performance, high
// quality and more!

// If local servers are not working, like broken shooting and moving,
// enter host_thread_mode 0 in console and when you are done, enter host_thread_mode 1

// DXLevel Launch Options:
// These launch options should be added to first launch, and then removed.
//
// DXLevel Launch options are very system dependent so you will only find the best one by testing it yourself.
// However, -dxlevel 98 is your best bet and works for most people.
//
// Windows (recommended dxlevel):
// -dxlevel 98 : DirectX 9Ex
//
// Windows (alternative dxlevels):
// -dxlevel 90 : Shader Model 2 (recommended for weak GPUs)
// -dxlevel 95 : Shader Model 3
// -dxlevel 100 : DirectX 9Ex (max settings allowed, no GPU feature support checking)
//
// OpenGL (Linux and macOS) (recommended dxlevel):
// -dxlevel 92 : OpenGL partial Shader Model 3
//
// OpenGL (Linux and macOS) (alternative dxlevel):
// -dxlevel 90 : OpenGL Shader Model 2 (recommended for weak GPUs)

// Launch Options:
// -novid -nojoy -nosteamcontroller -noff -softparticlesdefaultoff -reuse
//
// -novid : disables Valve startup logo, saves time
// -nojoy : stops Joystick system from starting up, faster startup and less memory usage
// -nosteamcontroller : disable Steam controller system, faster startup and less memory usage
// -noff : disables controller rumble (vibration) system, faster startup and less memory usage
// -softparticlesdefaultoff : disable scene depth blending for particles and sprites, more FPS
// -reuse :  allow network sockets to be reused when busy (sets SO_REUSEADDR), better network performance

// Extra Launch Options:
// -console : displays console on startup
// -r_emulate_gl : emulates OpenGL on Windows, FPS boost on most GPUs, does not work with
//                 the ESEA client, so remove it when you want to play in ESEA matches
// -nohltv : disables SourceTV, faster startup and less memory usage but can't spectate through SourceTV
// -nostartupsound : disable game music on main menu
// -primarysound : always use a direct hardware sound buffer (only works on stereo or headphones), may cause sounds to not play
// -snoforceformat : do not set the hardware sound buffer format, may cause sounds to not play
// -limitvsconst : limits the hardware vertex shader constants to 256, FPS boost on weak GPUs
// -NoQueuedPacketThread : disable the net queued packet thread, use with net_queued_packet_thread 0, use only on Linux
// -threads X : ONLY USE THIS IF YOU HAVE 8 OR MORE THREADS
//              how many extra worker threads are allowed. set X to thread count minus four.
//              if your value for threads is less than 4, there is no point to using -threads.

// OpenGL Launch Options (Linux and macOS only):
// -gl_enablesamplerobjects : use OpenGL Sampler Objects for better texture preloading (Linux only)
// -gl_texclientstorage : reduce memory usage by relying on GPU memory instead of a host copy (macOS only)
// -gl_nv_bindless_texturing : use GL_NV_bindless_texture for optimized texture objects in shaders (Nvidia only)
// -gl_amd_pinned_memory : use GL_AMD_pinned_memory for optimized buffer allocation (AMD only)

// Niche Launch Options:
// -nouserclip : uses software clipping instead of hardware user clip planes, FPS increase or decrease depends on your CPU+GPU
// -disable_d3d9_hacks : Disables a few Source Engine hacks, FPS increase or decrease depends on system
// -high : runs TF2 with High priority, which depending on your CPU may decrease or increase performance
// -nosound : disables sound, no performance boost unless your drivers are slow
// -small : allow for resolutions smaller than 640x480

// Experimental Launch Options:
// None at this time.

// ==============
// '--- Main ---'
// ==============

exec comfig // Main config file

// =================
// '--- Presets ---'
// =================
// Presets are overrides that set alternative values for easy customization.
// You can uncomment (remove the // before exec) to make a preset selected on load.
// Or, you can enter "exec presetname" (without the quotes) in console to customize the config in game.
// It is recommended to use "exec" on the main menu, as changing settings while in a match
// may cause stability and performance issues.

// You should only be using one preset at a time.

//exec presets/maxquality // Maximum quality preset -  Absolute maximum quality without caring about performance
                          // Remove any 01-mastercomfig folders from tf/custom
                          // Then copy the 01-mastercomfig_maxquality folder into tf/custom
//exec presets/midquality // Mid quality preset - Enables graphical features missing from default without making them higher quality
//exec presets/compquality // Competitive quality preset - The maximum performance you can get while enabling features that may give you
                           // an information advantage and disabling optimizations that may reduce accuracy
//exec presets/comp // Competitive performance preset - The maximum performance you can get without making the game too hard to play
                    // because of awful visual quality and glitches
//exec presets/maxperformance // Maximum performance preset - Maximum performance without caring much about visibility or possible bugs
                              // Remove any existing 01-mastercomfig folders from tf/custom
                              // Then copy the 01-mastercomfig_maxperformance folder into tf/custom
//exec presets/stripped // Stripped performance preset - Negatively affects playability by a lot and disables very essential features in desperation for performance
                        // Remove any existing 01-mastercomfig folders from tf/custom
                        // Then copy the 01-mastercomfig_maxperformance folder into tf/custom

// ================
// '--- Addons ---'
// ================
// Addons are additional configs that adjust the config and presets to suit more specific or niche use cases.
// You can uncomment (remove the // before exec) to make a addon applied on load.
// Or, you can run "exec addonname" (without the quotes) in console to customize the config in game.
// It is recommended to use "exec" on the main menu, as changing settings while in a match
// may cause stability and performance issues.

// Any number of addons can be used together, unlike presets.

//exec addons/badcpu // Bad CPU addon - Optimizations that generally do not affect quality for bad CPUs with two or less cores
                     // WARNING: can potentially REDUCE performance on other CPUs!!!
                     // stripped, maxperformance or comp presets recommended
//exec addons/badgpu // Bad GPU addon - Optimizations that generally do not affect quality for weak integrated graphics chips
                     // (Intel graphics) or weak/old GPUs (lower end made before 2007)
                     // WARNING: can potentially REDUCE performance on other graphics cards!!!
                     // maxperformance or comp presets recommended
//exec addons/ssd // SSD addon - Memory and loading optimizations for when your TF2 installation is on a SSD
//exec addons/transparent_viewmodels // Enables support for transparent viewmodels. Note that this does not enable transparent viewmodels,
                                     // your HUD must enable them. This only allows transparent viewmodels to work.
                                     // the transparent viewmodel materials require dxlevel90 or higher

// ================
// '--- Custom ---'
// ================

//exec custom // Personal extra addon - For changing values in config without update pains
