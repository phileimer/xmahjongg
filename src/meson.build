defines = ['-DVERSION="@0@"'.format( meson.project_version() )]
defines	+= ['-DPKGDATADIR="@0@"'.format( join_paths( get_option('prefix'), appdatadir ) )]

dep = dependency('X11', required : true)

configheader = 'config.h'

config = custom_target(configheader,
  output: configheader,
  command: ['touch', '@OUTPUT@'],
  install: false)

img = ['../images/buttons.gif', '../images/digits.gif']
imgsrc = 'images.c'

images = custom_target(imgsrc,
  output: imgsrc,
  input: img,
  command: [giftoc_exec, '-extern', '-makename', '@INPUT@'],
  capture: true,
  install: false)

executable('xmahjongg',
  ['alarm.cc', 'button.cc', 'game.cc', 'hint.cc', 'kmjts.cc', 'matches.cc', 'panel.cc',
  'solution.cc', 'swgeneral.cc', 'tile.cc', 'traverse.cc', 'board.cc', 'counter.cc',
  'gmjts.cc', 'kdets.cc', 'main.cc', 'moment.cc', 'random.cc', 'solvable.cc', 'swwidget.cc',
  'tileset.cc', 'xmj3ts.cc'],
  cpp_args: defines,
  include_directories: '../include',
  link_with: [liblcdf_static],
  sources: [images, config],
  dependencies: [dep],
  install: true)

