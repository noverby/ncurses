project('ncurses', 'c',
  version : '6.2',
  default_options : ['warning_level=3'])

subdir('ncurses')

inc_dirs = include_directories('ncurses', 'include')
static_library('ncurses', sources, c_args: ['-DNCURSES_WIDECHAR', '-DUSE_WIDEC_SUPPORT', '-DHAVE_MBTOWC', '-DHAVE_MBLEN'],include_directories: inc_dirs)
#static_library('ncurses', sources, c_args: [],include_directories: inc_dirs)
