def get_google_client():
    """Авторизация БЕЗ БРАУЗЕРА через сервисный аккаунт"""
    try:
        # Бот просто берет ключ из файла service_key.json
        gc = gspread.service_account(filename='service_key.json')
        return gc
    except Exception as e:
        print(f"!!! ОШИБКА АВТОРИЗАЦИИ: {e}")
        return None
