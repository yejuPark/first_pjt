# django

1. 프로젝트 생성
```zsh
django-admin startproject <pjtname> .
```

2. 가상환경 설정
```zsh
python -m venv venv
```

3. 가상환경 활성화/비활성화
```zsh
source venv/bin/activate
deactivate
```

4. 가상환경 내부에 django 설치
```zsh
pip install django
```

5. 서버 실행 확인 (종료 : 'ctrl + c')
```zsh
python manage.py runserver
```

6. 앱 생성
```zsh
django-admin startapp <appname>
```

7. 앱 등록
- `settings.py`의 `INSTALLED_APPS`에 등록
    - `<appname>`을 등록


8. 'urls.py'
```python
from first_app import views

urlpatterns = [
    ...
    path('index/', views.index),
]
```

9. 'views.py'
```python
def index(request):
    return render(request, 'index.html')
```

10. templates 폴더 생성 => index.html 생성


## MTV
: client의 request > urls.py > views.py > models.py > template(html) > views.py > response to client (html 문서 한장)

* MVC 패턴 (model - view - controller)
 - model : database
 - view : display (UI), html
 - controller : 둘 사이 
 (MTV > model , template(html) , view : MVC와 같은 순서)
