gnome = import('gnome')

pithos_resources = gnome.compile_resources('pithos',
  'io.github.Pithos.gresource.xml',
  gresource_bundle: true,
  install: true,
  install_dir: pkgdatadir
)

install_data('io.github.Pithos.gschema.xml',
  install_dir: join_paths(get_option('datadir'), 'glib-2.0/schemas')
)

i18n.merge_file(
  input: 'io.github.Pithos.desktop.in',
  output: 'io.github.Pithos.desktop',
  type: 'desktop',
  po_dir: '../po',
  install: true,
  install_dir: join_paths(get_option('datadir'), 'applications')
)

i18n.merge_file(
  input: 'io.github.Pithos.appdata.xml.in',
  output: 'io.github.Pithos.appdata.xml',
  po_dir: '../po',
  install: true,
  install_dir: join_paths(get_option('datadir'), 'appdata')
)

pithos_settings = gnome.compile_schemas()

subdir('icons')
