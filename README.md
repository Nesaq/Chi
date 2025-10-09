                    HTTP Запрос
                         ↓
                    ServeMux
                   /        \
                  /          \
            /api/*         /app/*
                |              |
        API эндпоинты    Статические файлы
        /healthz         index.html
        /metrics         assets/logo.png
        /reset           style.css
                |
        middlewareMetricsInc
                |
        fileserverHits++
