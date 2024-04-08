# Django-static-media-settings

**In Settings.py : -**

import os

**In Templates Section :**

"DIRS": [
            BASE_DIR/'templates'
        ],


**In the bottom :**

STATIC_FILES = [
    BASE_DIR/"static"
]



STATIC_URL = '/static/'

STATIC_ROOT =os.path.join(BASE_DIR,'static')

MEDIA_URL = '/media/'

MEDIA_ROOT = os.path.join(BASE_DIR,'media')

**In Project urls.py :**
from django.conf import settings
from django.conf.urls.static import static

+ static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)\
+ static(settings.STATIC_URL, document_root=settings.STATIC_ROOT)
