# Last modified: 2025-06-10T12:44:05.737970+00:00
FROM demisto/python3:3.12.8.3720084

COPY requirements.txt .

RUN apk --update add --no-cache --virtual .build-dependencies python3-dev build-base wget git \
  && pip install --no-cache-dir -r requirements.txt \
  && apk del .build-dependencies
