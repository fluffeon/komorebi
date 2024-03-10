
# Configure __init__.py
conf = configuration_data()
conf.set_quoted('PACKAGE_NAME', meson.project_name())
conf.set_quoted('PACKAGE_VERSION', meson.project_version())
conf.set_quoted('PKGDATADIR', pkgdatadir)
conf.set_quoted('DATADIR', join_paths(prefix, datadir))

initpy = configure_file(
    input: '__init__.in',
    output: '__init__.py',
    configuration: conf,
    install: false,
)

py.install_sources(
    [
        'preferences_window.py',
        'screen.py',
        'settings.py',
        'utilities.py',
        initpy,
    ],
    subdir: 'komorebi',
)

py.install_sources(
    [
        'bubblemenu/item.py',
        'bubblemenu/menu.py',

    ],
    subdir: 'komorebi/bubblemenu',
)

py.install_sources(
    [
        'overlays/asset.py',
        'overlays/base.py',
        'overlays/clock.py',
        'overlays/desktop.py',
    ],
    subdir: 'komorebi/overlays',
)

py.install_sources(
    [
        'wallpaper_creator/pages.py',
        'wallpaper_creator/utilities.py',
        'wallpaper_creator/window.py',
    ],
    subdir: 'komorebi/wallpaper_creator',
)

py.install_sources(
    [
        'wallpapers/base.py',
        'wallpapers/image.py',
        'wallpapers/video.py',
        'wallpapers/web.py',
    ],
    subdir: 'komorebi/wallpapers',
)
