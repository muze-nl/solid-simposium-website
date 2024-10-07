# Solid Symposium Website

This is the repository for the Solid Symposium website.

## Installation

No installation is required. Visit it at https://sosy25.eu/.

## Usage

It's a static website. Just visit it.

## Contributing

Please open an issue to provide feedback or suggestions.

Merge requests are welcome.

### Development

The website has been developed using [SimplyCode][1]

For development, the website can be run locally using [SimplyCode Electron][2] or [SimplyCode Docker][3].

Content can be edited using [SimplyEdit][4]. Visit https://sosys25.eu/#simply-edit to edit the content.

The live version of the repository is deployed with [SimplyEdit Backend][5] to save edits.

### Deployment

For the live version of the website, the following are required:

```tree
.
├── assets/
├── data/
├── html
│   ├── assets        -> ../assets/
│   ├── data          -> ../data/
│   ├── simply-edit/  -> ../vendor/simplyedit/simplyedit-backend/www/simply-edit/
│   ├── .htaccess     -> ../vendor/simplyedit/simplyedit-backend/www/.htaccess
│   └── index.html    -> ../generated.html
├── vendor/
│   └── simplyedit/
└── generated.html
```

these can be created using the following commands:
```sh
composer install
mkdir www
cd www
ln -s ../assets/ .
ln -s ../data/ .
ln -s ../generated.html index.html
ln -s ../vendor/simplyedit/simplyedit-backend/www/.htaccess .
ln -s ../vendor/simplyedit/simplyedit-backend/www/simply-edit/ .
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

[1]: https://github.com/SimplyEdit/simplycode
[2]: https://github.com/SimplyEdit/simplycode-electron
[3]: https://github.com/SimplyEdit/simplycode-docker
[4]: https://simplyedit.io/
[5]: https://github.com/SimplyEdit/simplyedit-backend
