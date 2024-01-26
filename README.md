### [도서판매현황] ###

도서판매현황 압축파일을 해제 후 각 도서별 정보를 상, 하반기로 나누어 정리 후에 판매부수, 판매금액을

집계하여 결과파일에 정리해서 메일에 첨부하여 담당자에게 발송하는 과제


**[사전작업]**

1_요청, 2_작업,3_결과 폴더 생성

1_요청 폴더 : 도서판매정보압축파일, 작업파일과 결과파일의 템플릿, 연락처 파일

Input 폴더 : VBA 코드 파일

Config 파일에 필요정보 입력


**[개인작업파일 Mywork 폴더]**

   CheckFolder - 작업폴더와 결과 폴더 확인 후 생성
  
   ExtractFile -  압축해제된 폴더 확인 후 해제 후 파일들을 array 변수에 담기
   
   WriteWorkFile - 압축해제된 파일들을 대상으로 판매된 연월에 따라 해당년에 상, 하반기로 분류하여 작업파일에 해당 중분류별 

                   시트에 데이터를 작성후 작업파일을 생성
   
   SendEmail - 최종 결과 파일들을 압축 후 연락처 파일에서 담당자의 이메일을 확인해서 메일에 압축파일을 첨부하여 이메일 발송
   
  
### [작업과정] ###

1. **INITIALIZE PROCESS**
   
    작업, 결과 폴더 확인
    압축파일 해제 후 필요정보 추출하여 dictionary에 담아서 작업
    작업파일 4개 생성 - 2022년 상, 하반기  2023년 상, 하반기
   
2. **GET TRANSACTION DATA**

    TransactionItem : 작업파일 arrWorkFiles 
                         
    dt_TransactionData 사용 안함
   
4. **PROCESS TRANSACTION**

  작업파일의 판매현황, 분류별판매현황 시트 작성 (판매부수, 판매금액 집계) 
  
  결과파일 생성 - 작업파일의 판매현황 시트와 분류별 판매현황 시트의 데이터를 한 시트에 담기

    
5. **END PROCESS**
   
    결과파일들을 압축 후 담당자에게 메일에 첨부하여 발송
   
