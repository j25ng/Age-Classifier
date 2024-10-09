![header](https://capsule-render.vercel.app/api?type=venom&color=auto&height=300&section=header&text=Age%20Classifier&desc=DE32%203rd%20project%20TEAM2&animation=twinkling&fontSize=60&descSize=30&fontColor=000000&fontAlignY=40)

## 프로젝트 개요
얼굴 사진을 업로드하면 [age-classifier 모델](https://huggingface.co/nateraw/vit-age-classifier)로 **나이**를 **예측**하는 **프로그램**


## 스택
<img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=Streamlit&logoColor=white"/> 사용자 인터페이스

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat&logo=FastAPI&logoColor=white"/> API 서버 

<img src="https://img.shields.io/badge/Apache_Airflow-017CEE?style=flat&logo=Apache-Airflow&logoColor=white"/>  작업 스케쥴

<img src="https://img.shields.io/badge/PySpark-E25A1C?style=flat&logo=Apache-Spark&logoColor=white"/> 데이터 처리 및 분석

<img src="https://img.shields.io/badge/MariaDB-003545?style=flat&logo=mariadb&logoColor=white"/> 데이터베이스 

## 아키텍쳐 구상도
![image](https://github.com/user-attachments/assets/07992c4b-d047-4c41-9234-c64e1aac1afd)


## 주요 기능
1. **업로드한 이미지로 나이 예측**
   - 사용자는 **Streamlit** 인터페이스를 통해 얼굴 이미지 업로드
   - 업로드된 이미지는 **FastAPI**로 전송하여 DB 저장
   - **Airflow**를 사용하여 머신러닝 모델 실행

2. **이미지 전처리**
   - **FastAPI**를 사용하여 잘못된 이미지 데이터 삭제 가능
   - 실제 나이 라벨링

3. **데이터 집계 및 분석**
   - **PySpark**를 활용하여 나이대별 예측 정확도 분석

## 기본 설정
```
$ docker pull 어쩌고
```

## 이용
### 사용자
1. [Streamlit](http://54.180.238.29:8032/) 접속
2. Upload Image 접속
3. 이미지 업로드
   
<details>
  <summary><strong>업로드 화면</strong></summary>

  ![image](https://github.com/user-attachments/assets/017564f9-ecf9-49c9-83e7-1abcf9b8b66b)



</details>   

4. [Streamlit](http://54.180.238.29:8032/all) 접속
5. 이미지 예상 나이 확인
<details>
  <summary><strong>나이 예측 화면</strong></summary>

 ![image](https://github.com/user-attachments/assets/1a487d18-234a-422b-b4f5-8c1c0f499b0a)



</details> 



### 관리자
1. [Streamlit](http://54.180.238.29:8032/admin) 접속
2. Manage 접속
3. 비밀번호 입력
4. 얼굴이 아닌 이미지 삭제 및 정답 결과 라벨링
   
<details>
  <summary><strong>데이터 전처리 화면</strong></summary>

![image](https://github.com/user-attachments/assets/fdc68695-9c77-48d9-80be-92f65c0b36b4)



</details> 
 


### 시각화
1. [Streamlit](http://54.180.238.29:8032/age_acc#d18cd05) 접속
2. 나이대별 예측 정확도 그래프

<details>
   <summary><strong>그래프 화면</strong></summary>

   ![image](https://github.com/user-attachments/assets/8371d49d-31f3-47dd-b844-7b60f3664346)

</details>
