# 출처 : https://docs.djangoproject.com/ko/2.2/intro/tutorial01/
# django
git clone https://github.com/django/django.git
pip install -e django\
// Editable이래
django-admin startproject [folder 이름] // 하위 폴더 생성됨

# tip
과거의 PHP 를 작성해본 경험이 있다면(최근의 프레임워크 말고) 아마 코드 전체를 /var/www 같은 웹 서버의 DocumentRoot 에 넣으려고 하려고 할겁니다. Django 에서는 그러지 마십시요. 파이선 코드가 웹서버의 DocumentRoot 에 존재하는것은 좋은 생각이 아닙니다. 웹을 통해서 외부의 사람들이 Python 코드를 직접 열어볼 수 있는 위험이 있기 때문입니다. 그렇게 되면 보안에 별로 좋지 않습니다.

작성한 코드를 /home/mycode 와 같은 DocumentRoot 의 바깥에 두는것을 권합니다.


# 개발서버
$ python manage.py runserver
$ python manage.py runserver 0:8000

# 포트 변경하기
python manage.py runserver 8080

# app 추가 (투표)
python manage.py startapp polls