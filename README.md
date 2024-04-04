## 📝 Python OpenCV - 사람 얼굴과 해골 합성

## Abouy
이번 포스팅에서는 여러 가지 실습을 해보겠습니다. 이번 포스팅 역시 '파이썬으로 만드는 OpenCV 프로젝트(이세우 저)'를 정리한 것임을 밝힙니다.

## 🙋‍♀️ 사람 얼굴과 해골 합성 실습
연습용으로 아래 사람 얼굴과 해골 얼굴을 반반씩 합성해보겠습니다. 
![title](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FddMQKj%2FbtqGdtW0usk%2FnTLwcSYP6uQlKeKX26btfK%2Fimg.png)   

아래와 같이 그냥 반반씩 합치면 경계선이 뚜렷해 어색합니다. 알파 값을 조절하며 자연스럽게 이미지 합성을 해보겠습니다.

![title](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FUuYE6%2FbtqGh4A9tD8%2FW8kQZuYKLJc3ulsi6h8bbk%2Fimg.png)   

## 🛠 기능 엿보기   

자연스럽게 반반씩 합성이 되었습니다. 

이 예제에서 핵심 코드는 img_comp[:, start+i] = img_face[:, start+i] * alpha + img_skull[:, start+i] * beta 부분입니다. 

사람 얼굴 이미지의 반쪽과 해골 이미지의 반쪽을 알파 값을 조정하며 합성하는 부분이기 때문입니다.
