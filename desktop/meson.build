# replace @datadir@ and translate
metadata = 'cafe-desktop.xml'
i18n.merge_file(metadata,
  input: configure_file(
    input: metadata + '.in.in',
    output: metadata + '.in',
    configuration : conf
    ),
  output: metadata,
  po_dir: '../po',
  data_dirs: '..',
  install: true,
  install_dir: metadatadir
  )

backgrounds = [
  'Float-into-MATE.png',
  'GreenTraditional.jpg',
  'MATE-Stripes-Dark.png',
  'MATE-Stripes-Light.png',
  'Stripes.png',
  'Ubuntu-Cafe-Cold-no-logo.png',
  'Ubuntu-Cafe-Dark-no-logo.png',
  'Ubuntu-Cafe-Radioactive-no-logo.png',
  'Ubuntu-Cafe-Warm-no-logo.png',
]
install_data(backgrounds, install_dir: join_paths(backgrounddir, 'desktop'))
