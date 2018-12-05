# Open Edition Driver
[![Build Status](https://travis-ci.org/hirmeos/open_edition_driver.svg?branch=master)](https://travis-ci.org/hirmeos/open_edition_driver)

This driver assumes that your instance of the [Identifier Translation Service](https://github.com/hirmeos/identifier_translation_service) contains mappings of works and Open Edition URLs. These can be obtained beforehand from [OE's OAI implementation](https://oai.openedition.org) - which you can harvest using [hirmeos/oai_uri_import](https://github.com/hirmeos/oai_uri_import).


## Run via crontab
```
0 0 * * 0 docker run --rm --name "open_edition_driver" --env-file /path/to/config.env -v /somewhere/to/store/preprocessing:/usr/src/app/cache -v /somewhere/to/store/output:/usr/src/app/output openbookpublishers/open_edition_driver
```
