                    HTTP Запрос
                         ↓
                  Проверка метода
                   /          \
             Совпадает?     Нет → 405 Method Not Allowed
                 Да
                 ↓
            ServeMux match
            /      |      \
           /       |       \
    GET /healthz  GET /metrics  POST /reset  /app/*
         ↓           ↓            ↓           ↓
        OK        Hits: X      Store(0)   FileServer
