
FROM demisto/python3:3.12.8.3720084

COPY requirements.txt .

RUN apk --update add --no-cache --virtual .build-dependencies python3-dev build-base wget git linux-headers \
  && apk --update add --no-cache libstdc++ \
  && pip install --no-cache-dir -r requirements.txt \
  && apk del .build-dependencies
