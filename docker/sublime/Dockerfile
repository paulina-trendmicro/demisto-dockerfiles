
FROM demisto/python3:3.12.8.3720084

# Upgrade all packages to latest
RUN apk --update --no-cache upgrade

COPY requirements.txt .

RUN apk --update add --no-cache --virtual .build-dependencies python3-dev build-base wget \
  && pip install --no-cache-dir -r requirements.txt \
  && apk del .build-dependencies

