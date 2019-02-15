# Caliper Tracking

## Description

Caliper Tracking can be used to transform the edx tradition events into Caliper Standard format. Then those events can be used with any analytics application that is compatible with Caliper Standard events.

## Installation

To install **`caliper-tracking`** run the following command inside your virtual environment:

```sh
pip install git+https://github.com/ucsd-etc/caliper_tracking.git@master#egg=caliper-tracking
```

If you are using dockerized containers, then run the following command in devstack directory:

```sh
docker-compose exec lms bash -c 'source /edx/app/edxapp/edxapp_env && cd /edx/app/edxapp/edx-platform && pip install -e git+https://github.com/ucsd-ets/caliper_tracking.git@master#egg=caliper-tracking
```

## Usage

To enable and use `caliper-tracking`,

1. Add/Enable the `ENABLE_EVENT_CALIPERIZATION` flag in `FEATURES` in the `/edx/app/edxapp/lms.env.json` and `/edx/app/edxapp/cms.env.json` files which are located one level above the `edx-platform` directory.

```json
    "ENABLE_EVENT_CALIPERIZATION": true,
```

in `/edx/app/edxapp/lms.env.json` and `/edx/app/edxapp/cms.env.json` files of edx installation.

2. Restart your build/ devserver.
