
#has_inttypes = meson.get_compiler('cpp').has_header('inttypes.h')

defines = ['-DVERSION="@0@"'.format(meson.project_version())]
defines	+= ['-DPKGDATADIR="@0@"'.format(join_paths(get_option('prefix'), get_option('datadir')))]

dep = dependency('X11', required : true)
#dep += declare_dependency()

#img = ['../images/buttons.gif', '../images/digits.gif']
#run_command('../liblcdf/giftoc', '-extern', '-makename', img, check: true)

executable('xmahjongg',
  ['alarm.cc', 'button.cc', 'game.cc', 'hint.cc', 'kmjts.cc', 'matches.cc', 'panel.cc',
  'solution.cc', 'swgeneral.cc', 'tile.cc', 'traverse.cc', 'board.cc', 'counter.cc',
  'gmjts.cc', 'kdets.cc', 'main.cc', 'moment.cc', 'random.cc', 'solvable.cc', 'swwidget.cc',
  'tileset.cc', 'xmj3ts.cc'],
  cpp_args: defines,
  include_directories: '../include',
  link_with: liblcdf_static,
  dependencies: dep,
  install: true)

