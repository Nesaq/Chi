                    HTTP Запрос
                         ↓
                    ServeMux
                   /    |    \
                  /     |     \
            /api/    /admin/   /app/
                |        |        |
        Health Check  Admin UI  Website
        (JSON)        (HTML)    (Files)
                |        |        |
                |        |   middlewareMetricsInc
                |        |        ↓
                |        |   fileserverHits++
                |        |
                |    handleAdminMetrics
                |        ↓
                |    HTML с счетчиком
