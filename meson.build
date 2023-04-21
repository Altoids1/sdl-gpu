project('SDL_gpu', 'c')
SDL_gpu_dir = include_directories(
  'include',
  'src',
  '/usr/include/SDL2',
  'src/externals/glew',
  'src/externals/glew/GL',
  'src/externals/stb_image',
  'src/externals/stb_image_write',
  '__CMake_build',
  '.'
)
SDL_gpu_sys = include_directories(is_system : true)
SDL_gpu_inc = [SDL_gpu_dir, SDL_gpu_sys]
SDL_gpu_src = files(
  'src/externals/glew/glew.c',
  'src/SDL_gpu.c',
  'src/SDL_gpu_matrix.c',
  'src/SDL_gpu_renderer.c',
  'src/SDL_gpu_shapes.c',
  'src/renderer_OpenGL_1_BASE.c',
  'src/renderer_OpenGL_1.c',
  'src/renderer_OpenGL_2.c',
  'src/renderer_OpenGL_3.c',
  'src/renderer_OpenGL_4.c',
  'src/renderer_GLES_1.c',
  'src/renderer_GLES_2.c',
  'src/renderer_GLES_3.c',
  'src/externals/stb_image/stb_image.c',
  'src/externals/stb_image_write/stb_image_write.c',
  'src/externals/glew/GL/glew.h',
  'src/externals/glew/GL/glxew.h',
  'src/externals/glew/GL/wglew.h',
  'include/SDL_gpu.h',
  'include/SDL_gpu_version.h',
  'include/SDL_gpu_RendererImpl.h',
  'include/SDL_gpu_OpenGL_1_BASE.h',
  'include/SDL_gpu_OpenGL_1.h',
  'include/SDL_gpu_OpenGL_2.h',
  'include/SDL_gpu_OpenGL_3.h',
  'include/SDL_gpu_OpenGL_4.h',
  'include/SDL_gpu_GLES_1.h',
  'include/SDL_gpu_GLES_2.h',
  'include/SDL_gpu_GLES_3.h',
  'src/externals/stb_image/stb_image.h',
  'src/externals/stb_image_write/stb_image_write.h'
)
SDL_gpu = static_library(
  'SDL_gpu',
  SDL_gpu_src,
  build_by_default : true,
  link_args : [],
  link_with : [],
  include_directories : SDL_gpu_inc,
  install : true,
  override_options : ['c_std=gnu99'],
  objects : [],
  install_dir : 'lib',
  c_args : ['-DGLEW_STATIC', '-DSDL_GPU_DISABLE_GLES', '-DSDL_GPU_USE_BUFFER_RESET', '-DSTBI_FAILURE_USERMSG'],
  pic : false
)
SDL_gpu_dep = declare_dependency(
  link_args : [],
  link_with : SDL_gpu,
  compile_args : [],
  include_directories : SDL_gpu_inc
)
_3d_demo_dir = include_directories(
  'include',
  'src',
  '/usr/include/SDL2',
  'src/externals/glew',
  'src/externals/glew/GL',
  'src/externals/stb_image',
  'src/externals/stb_image_write',
  '.',
  '__CMake_build'
)
_3d_demo_sys = include_directories(is_system : true)
_3d_demo_inc = [_3d_demo_dir, _3d_demo_sys]
_3d_demo_src = files('demos/3d/main.c', 'src/externals/glew/glew.c')
_3d_demo = executable(
  '3d_demo',
  _3d_demo_src,
  build_by_default : false,
  link_args : [
    '-rdynamic',
    '-L-L/home/amelie/git/ServeTwo/subprojects/sdl-gpu-0.12.0/src',
    '-lSDL2',
    '-lm',
    '-lGL',
    '-lGLU',
    '-lSDL2',
    '-lm'
  ],
  link_with : [SDL_gpu],
  include_directories : _3d_demo_inc,
  install : false,
  override_options : ['c_std=gnu99'],
  objects : [],
  c_args : ['-DGLEW_STATIC', '-DSDL_GPU_DISABLE_GLES', '-DSDL_GPU_USE_BUFFER_RESET', '-DSTBI_FAILURE_USERMSG'],
  pie : false
)
SDL_gpu_shared_dir = include_directories(
  'include',
  'src',
  '/usr/include/SDL2',
  'src/externals/glew',
  'src/externals/glew/GL',
  'src/externals/stb_image',
  'src/externals/stb_image_write',
  '__CMake_build',
  '.'
)
SDL_gpu_shared_sys = include_directories(is_system : true)
SDL_gpu_shared_inc = [SDL_gpu_shared_dir, SDL_gpu_shared_sys]
SDL_gpu_shared_src = files(
  'src/externals/glew/glew.c',
  'src/SDL_gpu.c',
  'src/SDL_gpu_matrix.c',
  'src/SDL_gpu_renderer.c',
  'src/SDL_gpu_shapes.c',
  'src/renderer_OpenGL_1_BASE.c',
  'src/renderer_OpenGL_1.c',
  'src/renderer_OpenGL_2.c',
  'src/renderer_OpenGL_3.c',
  'src/renderer_OpenGL_4.c',
  'src/renderer_GLES_1.c',
  'src/renderer_GLES_2.c',
  'src/renderer_GLES_3.c',
  'src/externals/stb_image/stb_image.c',
  'src/externals/stb_image_write/stb_image_write.c',
  'src/externals/glew/GL/glew.h',
  'src/externals/glew/GL/glxew.h',
  'src/externals/glew/GL/wglew.h',
  'include/SDL_gpu.h',
  'include/SDL_gpu_version.h',
  'include/SDL_gpu_RendererImpl.h',
  'include/SDL_gpu_OpenGL_1_BASE.h',
  'include/SDL_gpu_OpenGL_1.h',
  'include/SDL_gpu_OpenGL_2.h',
  'include/SDL_gpu_OpenGL_3.h',
  'include/SDL_gpu_OpenGL_4.h',
  'include/SDL_gpu_GLES_1.h',
  'include/SDL_gpu_GLES_2.h',
  'include/SDL_gpu_GLES_3.h',
  'src/externals/stb_image/stb_image.h',
  'src/externals/stb_image_write/stb_image_write.h'
)
SDL_gpu_shared = shared_library(
  'SDL_gpu_shared',
  SDL_gpu_shared_src,
  build_by_default : true,
  link_args : [
    '-lSDL2',
    '-lm',
    '-lGL',
    '-lGLU',
    '/usr/lib/x86_64-linux-gnu/libGL.so',
    '/usr/lib/x86_64-linux-gnu/libGLU.so'
  ],
  link_with : [],
  include_directories : SDL_gpu_shared_inc,
  install : true,
  override_options : ['c_std=gnu99'],
  objects : [],
  install_dir : 'lib',
  c_args : ['-DGLEW_STATIC', '-DSDL_GPU_DISABLE_GLES', '-DSDL_GPU_USE_BUFFER_RESET', '-DSDL_gpu_shared_EXPORTS', '-DSTBI_FAILURE_USERMSG']
)
SDL_gpu_shared_dep = declare_dependency(
  link_args : [
    '-lSDL2',
    '-lm',
    '-lGL',
    '-lGLU',
    '/usr/lib/x86_64-linux-gnu/libGL.so',
    '/usr/lib/x86_64-linux-gnu/libGLU.so'
  ],
  link_with : SDL_gpu_shared,
  compile_args : [],
  include_directories : SDL_gpu_shared_inc
)
camera_demo_dir = include_directories(
  'include',
  'src',
  '/usr/include/SDL2',
  'src/externals/glew',
  'src/externals/glew/GL',
  'src/externals/stb_image',
  'src/externals/stb_image_write',
  '.',
  '__CMake_build'
)
camera_demo_sys = include_directories(is_system : true)
camera_demo_inc = [camera_demo_dir, camera_demo_sys]
camera_demo_src = files('demos/camera/main.c')
camera_demo = executable(
  'camera_demo',
  camera_demo_src,
  build_by_default : false,
  link_args : [
    '-rdynamic',
    '-L-L/home/amelie/git/ServeTwo/subprojects/sdl-gpu-0.12.0/src',
    '-lSDL2',
    '-lm',
    '-lGL',
    '-lGLU',
    '-lSDL2',
    '-lm'
  ],
  link_with : [SDL_gpu],
  include_directories : camera_demo_inc,
  install : false,
  override_options : ['c_std=gnu99'],
  objects : [],
  c_args : ['-DGLEW_STATIC', '-DSDL_GPU_DISABLE_GLES', '-DSDL_GPU_USE_BUFFER_RESET', '-DSTBI_FAILURE_USERMSG'],
  pie : false
)
init_demo_dir = include_directories(
  'include',
  'src',
  '/usr/include/SDL2',
  'src/externals/glew',
  'src/externals/glew/GL',
  'src/externals/stb_image',
  'src/externals/stb_image_write',
  '.',
  '__CMake_build'
)
init_demo_sys = include_directories(is_system : true)
init_demo_inc = [init_demo_dir, init_demo_sys]
init_demo_src = files('demos/init/main.c')
init_demo = executable(
  'init_demo',
  init_demo_src,
  build_by_default : false,
  link_args : [
    '-rdynamic',
    '-L-L/home/amelie/git/ServeTwo/subprojects/sdl-gpu-0.12.0/src',
    '-lSDL2',
    '-lm',
    '-lGL',
    '-lGLU',
    '-lSDL2',
    '-lm'
  ],
  link_with : [SDL_gpu],
  include_directories : init_demo_inc,
  install : false,
  override_options : ['c_std=gnu99'],
  objects : [],
  c_args : ['-DGLEW_STATIC', '-DSDL_GPU_DISABLE_GLES', '-DSDL_GPU_USE_BUFFER_RESET', '-DSTBI_FAILURE_USERMSG'],
  pie : false
)
simple_shader_demo_dir = include_directories(
  'include',
  'src',
  '/usr/include/SDL2',
  'src/externals/glew',
  'src/externals/glew/GL',
  'src/externals/stb_image',
  'src/externals/stb_image_write',
  '.',
  '__CMake_build'
)
simple_shader_demo_sys = include_directories(is_system : true)
simple_shader_demo_inc = [simple_shader_demo_dir, simple_shader_demo_sys]
simple_shader_demo_src = files('demos/simple-shader/main.c')
simple_shader_demo = executable(
  'simple_shader_demo',
  simple_shader_demo_src,
  build_by_default : false,
  link_args : [
    '-rdynamic',
    '-L-L/home/amelie/git/ServeTwo/subprojects/sdl-gpu-0.12.0/src',
    '-lSDL2',
    '-lm',
    '-lGL',
    '-lGLU',
    '-lSDL2',
    '-lm'
  ],
  link_with : [SDL_gpu],
  include_directories : simple_shader_demo_inc,
  install : false,
  override_options : ['c_std=gnu99'],
  objects : [],
  c_args : ['-DGLEW_STATIC', '-DSDL_GPU_DISABLE_GLES', '-DSDL_GPU_USE_BUFFER_RESET', '-DSTBI_FAILURE_USERMSG'],
  pie : false
)
test_common_dir = include_directories(
  'include',
  'src',
  '/usr/include/SDL2',
  'src/externals/glew',
  'src/externals/glew/GL',
  'src/externals/stb_image',
  'src/externals/stb_image_write',
  '__CMake_build',
  '.'
)
test_common_sys = include_directories(is_system : true)
test_common_inc = [test_common_dir, test_common_sys]
test_common_src = files('common/common.c', 'common/demo-font.c')
test_common = static_library(
  'test_common',
  test_common_src,
  build_by_default : false,
  link_args : [],
  link_with : [],
  include_directories : test_common_inc,
  install : false,
  override_options : ['c_std=gnu99'],
  objects : [],
  c_args : ['-DGLEW_STATIC', '-DSDL_GPU_DISABLE_GLES', '-DSDL_GPU_USE_BUFFER_RESET', '-DSTBI_FAILURE_USERMSG'],
  pic : false
)
test_common_dep = declare_dependency(
  link_args : [],
  link_with : test_common,
  compile_args : [],
  include_directories : test_common_inc
)
tutorial_space_demo_dir = include_directories(
  'include',
  'src',
  '/usr/include/SDL2',
  'src/externals/glew',
  'src/externals/glew/GL',
  'src/externals/stb_image',
  'src/externals/stb_image_write',
  '.',
  '__CMake_build'
)
tutorial_space_demo_sys = include_directories(is_system : true)
tutorial_space_demo_inc = [tutorial_space_demo_dir, tutorial_space_demo_sys]
tutorial_space_demo_src = files('demos/tutorial-space/main.c')
tutorial_space_demo = executable(
  'tutorial_space_demo',
  tutorial_space_demo_src,
  build_by_default : false,
  link_args : [
    '-rdynamic',
    '-L-L/home/amelie/git/ServeTwo/subprojects/sdl-gpu-0.12.0/src',
    '-lSDL2',
    '-lm',
    '-lGL',
    '-lGLU',
    '-lSDL2',
    '-lm'
  ],
  link_with : [SDL_gpu],
  include_directories : tutorial_space_demo_inc,
  install : false,
  override_options : ['c_std=gnu99'],
  objects : [],
  c_args : ['-DGLEW_STATIC', '-DSDL_GPU_DISABLE_GLES', '-DSDL_GPU_USE_BUFFER_RESET', '-DSTBI_FAILURE_USERMSG'],
  pie : false
)
