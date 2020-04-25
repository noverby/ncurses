project('ncurses', 'c',
  version : '6.2',
  default_options : ['warning_level=3', 'b_asneeded=false', 'b_lundef=false'])

subdir('ncurses')

#foreach src : sources
#  str = '@0@'.format(src)
#  message(str)
#  configure_file(input: str, output: str, copy: true)
#endforeach

inc_dirs = include_directories('ncurses', 'include')
#static_library('ncurses', sources, c_args: ['-DNCURSES_WIDECHAR', '-DUSE_WIDEC_SUPPORT', '-DHAVE_MBTOWC', '-DHAVE_MBLEN'],include_directories: inc_dirs)
libncurses = static_library('ncurses', sources, c_args: [],include_directories: inc_dirs)

libncurses_dep = declare_dependency(include_directories: inc_dirs,
                                   link_with: libncurses)
