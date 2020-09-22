### 1. Django-REST Framework

1. DRF : `Django` 안에서 `RESTful API` 서버를 쉽게 구축할 수 있도록 도와주는 오픈소스 라이브러리.`

2. 기본설정
    - (가상환경)
    - `DRF` 라이브러리 설치 : `pip install djangorestframework`
    - `API` 자동 문서화 라이브러리 설치 : `pip install django-rest-swagger`
    
    > `setting.py`의 `INSTALLED_APPS`에 `rest_framework`, `rest_framework_swagger` 추가

3. Serialize
    - 직렬화의 필요성
        1. 다른환경과 데이터를 주고 받으려면 동일한 데이터 구조를 가져야함.
        2. serialize : `통일된 데이터를 전송가능한 형태로(데이터 스트림) 만드는 것`
        3. 파이썬에서 직렬화를 담당하는 클래스 = `Serializer` : serializers.py
        
    - `serializer`는 쿼리셋과 모델 인스턴스와 같은 복잡한 데이터를 `JSON, XML` 등의 유형으로 쉽게 변환 할 수 있도록 해줌.
        - `Django`에서 `Client`로 복잡한 데이터를 보내려면 `'string'`으로 변환해야함. 이 변환을 `serializer`라고 함. 
       
    - `serializer`의 첫번째 인자에는 문자열의 형태를 변환시킬 데이터를 넣음.
        - 여러개의 객체가 저장되어 있는 경우 `many=True`

<br>
<br>

- 함수 기반 뷰를 사용
    - `@api_view()` : `from rest_framework.decorators import api_view`
        - 어떠한 `HTTP Methods`를 허용할건지에 대한 설정을 하는 데코레이터

- 클래스 기반 뷰
    - 데코레이터가 없는 대신, `APIView`를 상속받음

- 제네릭 클래스 기반 뷰
    - 짱짱맨

- `import serializer`
    - `from rest_framework import serializers`

- `view.py` 함수에서는 최종적으로 `response`라는 객체를 반환해야함. (`render`나 `redirect`도 `response`클래스를 상속받은 메소드임.)
    - `from rest_framework.response import Response`







