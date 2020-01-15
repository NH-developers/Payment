# Payment
간편결제 API
## 1 소개  
### 1.1 출금이체
고객계좌에서 이용기관의 계좌로 자금을 인출하는 실시간 출금 서비스입니다.
#### 1.1.1 출금이체 오픈API 목록
| 전문명 | API |
|:---:|:---:|
| 출금이체 | DrawingTransfer |

#### 1.1.2 출금이체 흐름도
##### step 1
![image](https://user-images.githubusercontent.com/51725751/71962491-e46d0d00-323c-11ea-9f69-9421795792e2.png)
##### step 2
![image](https://user-images.githubusercontent.com/51725751/71962601-2302c780-323d-11ea-8d29-48b63ec02cd7.png)
##### step 3
![image](https://user-images.githubusercontent.com/51725751/71962626-2f872000-323d-11ea-9616-d3009efa6522.png)
#### 1.1.3 출금이체 Time Out 및 무응답
![image](https://user-images.githubusercontent.com/51725751/71962654-3ca40f00-323d-11ea-8fe7-0f6a3e9f7877.png)
#### 1.1.4 출금이체 재처리
![image](https://user-images.githubusercontent.com/51725751/71962665-47f73a80-323d-11ea-9624-0f339297a2c4.png)

### 1.2 입금이체
이용기관의 지급계좌에서 자금을 인출하여 수취인 계좌로 실시간 입금하는 서비스입니다.
#### 1.2.1 입금이체 오픈API 목록
| 전문명 | API |
|:---:|:---:|
| 농협입금이체(계좌번호) |	ReceivedTransferAccountNumber |	
| 타행입금이체(계좌번호) |	ReceivedTransferOtherBank	 |

#### 1.2.2 입금이체 흐름도
##### step 1
![image](https://user-images.githubusercontent.com/51725751/71962941-eedbd680-323d-11ea-8f4b-8d41d6ad15c8.png)
##### step 2
![image](https://user-images.githubusercontent.com/51725751/71962960-fb602f00-323d-11ea-919c-7bfca1d7ac59.png)
##### step 3
![image](https://user-images.githubusercontent.com/51725751/71963015-159a0d00-323e-11ea-962a-28f8add2b10e.png)
#### 1.2.3 입금이체 Time Out 및 무응답
![image](https://user-images.githubusercontent.com/51725751/71963044-22b6fc00-323e-11ea-9d72-57724a337b44.png)
#### 1.2.4 입금이체 재처리
![image](https://user-images.githubusercontent.com/51725751/71963066-32364500-323e-11ea-8c9b-75c3147f7af4.png)

### 1.3 거래내역조회
인터넷뱅킹이나 펌뱅킹 등을 통하지 않고 금융API를 통해 계좌거래내역을 간편하게 조회할 수 있는 서비스입니다.
#### 1.3.1 거래내역조회 오픈API 목록
| 전문명 | API |
|:---:|:---:|
| 거래내역조회(계좌번호) |	InquireTransactionHistory |	
		
#### 1.3.2 거래내역조회 흐름도
![image](https://user-images.githubusercontent.com/51725751/71963216-87725680-323e-11ea-8ddc-5badc2e45c0d.png)

## 2 resource url
#### 2.1 출금이체
https://developers.nonghyup.com/DrawingTransfer.nh
#### 2.2 농협입금이체
https://developers.nonghyup.com/ReceivedTransferAccountNumber.nh
#### 2.3 타행입금이체
https://developers.nonghyup.com/ReceivedTransferOtherBank.nhh
#### 2.4 거래내역조회
https://developers.nonghyup.com/InquireTransactionHistory.nh

## 3 example
### 3.1.1 출금이체 Request example
```json
{	
    "Header":{
        "ApiNm":"DrawingTransfer",
        "Tsymd":"20191129",
        "Trtm":"125237",
        "Iscd":"900001",
        "FintechApsno":"001",
        "ApiSvcCd":"DrawingTransferA",
        "IsTuno":"201911290000000001", 
        "AccessToken": "6500e3a81fe2deafd996ea437b6a4b7cfbd04a3ab7e26480b431fdf3ccf3b39b"
    },
  "FinAcno":"00820109000010001413",
  "Tram":"1000000",
  "DractOtlt":"테스트",
  "MractOtlt":"테스트"
}
```
### 3.1.2 출금이체 Request Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---:|:---:|:---:|:---:|:---:|:---:|  
| Header || 공통부 |||||	 
| FinAcno |	핀-어카운트 |	필드 |	30 |	필수 |	 
| Tram |	거래금액 |	필드 |	15 |	필수 |	 
| DractOtlt |	출금계좌인자내용 |	필드 |	25 |	선택 |	출금고객계좌 통장적용 인자내용 ex) 핀테크기업명 or 핀테크서비스명or 송금수취인 |
| MractOtlt |	입금계좌인자내용 |	필드 |	25 |	미사용 |	출금이체시에는 출금계좌인자 내용만사용 |
### 3.1.3 출금이체 Response example
```json
{	
    "Header": {
        "Trtm": "125237",
        "Rsms": "정상처리 되었습니다.",
        "ApiNm": "DrawingTransfer",
        "IsTuno": "201911290000000001",
        "Tsymd": "20191129",
        "FintechApsno": "001",
        "Iscd": "900001",
        "Rpcd": "00000",
        "ApiSvcCd": "DrawingTransferA"
    },
    "FinAcno": "00820100000190001639",
    "RgsnYmd": "20191124"
}
```
### 3.1.4 출금이체 Response Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---:|:---:|:---:|:---:|:---:|:---:|  
| Header || 공통부 |||||	 
| FinAcno |	핀-어카운트 |	필드 |	30 |	필수 |	 
| RgsnYmd |	등록일자 |	필드 |	8 |	필수 |	

### 3.2.1 농협입금이체 Request example
```json
{
  "Header":{
      "ApiNm":"ReceivedTransferAccountNumber",
      "Tsymd":"20191129",
      "Trtm":"003544",
      "Iscd":"000019",
      "FintechApsno":"001",
      "ApiSvcCd":"ReceivedTransferA",
      "IsTuno":"201911290000000001",
      "AccessToken":
      "791c18f7377be31c8b30b27eba8573de0aac529890c7b18ac722f6120adc5054"},
  "Bncd":"011",
  "Acno":"3020000000109",
  "Tram":"200000",
  "DractOtlt":"테스트",
  "MractOtlt":"테스트" 
}
```
### 3.2.2 농협입금이체 Request Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	 
| Bncd |	은행코드 |	필드 |	3 |	필수 |	농협은행:011, 상호금융:012 |
| Acno |	계좌번호 |	필드 |	20 |	필수 |	 
| Tram |	거래금액 |	필드 |	15 |	필수 |	 
| DractOtlt |	출금계좌인자내용 |	필드 |	25 |	선택 |	출금계좌(입금이체 약정모계좌) 통장인자내용 or 고객명 |
| MractOtlt |	입금계좌인자내용 |	필드 |	25 |	선택 |	입금고객계좌 통장적용 인자내용 ex) 핀테크기업명 or 핀테크서비스명 |
### 3.2.3 농협입금이체 Response example
```json
{	
    "Header": {
        "Trtm": "003544",
        "Rsms": "정상처리 되었습니다.",
        "ApiNm": "ReceivedTransferAccountNumber",
        "IsTuno": "201911290000000001",
        "Tsymd": "20191129",
        "FintechApsno": "001",
        "Iscd": "000019",
        "Rpcd": "00000",
        "ApiSvcCd": "ReceivedTransferA"
    }
}
```
### 3.2.4 농협입금이체 Response Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---:|:---:|:---:|:---:|:---:|:---:|  
| Header || 공통부 |||||	 

### 3.3.1 타행입금이체 Request example
```json
{	
  "Header":{
      "ApiNm":"ReceivedTransferOtherBank",
      "Tsymd":"20191129",
      "Trtm":"003544",
      "Iscd":"000019",
      "FintechApsno":"001",
      "ApiSvcCd":"ReceivedTransferA",
      "IsTuno":"201911290000000001",
      "AccessToken":
      "791c18f7377be31c8b30b27eba8573de0aac529890c7b18ac722f6120adc5054"},
    "Bncd":"002",
    "Acno":"1000000028002",
    "Tram":"200000",
    "DractOtlt":"테스트",
    "MractOtlt":"테스트"   
}
```
### 3.3.2 타행입금이체 Request Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	 
| Bncd |	은행코드 |	필드 |	3 |	필수 |	농협은행:011, 상호금융:012 |
| Acno |	계좌번호 |	필드 |	20 |	필수 |	 
| Tram |	거래금액 |	필드 |	15 |	필수 |	 
| DractOtlt |	출금계좌인자내용 |	필드 |	25 |	선택 |	출금계좌(입금이체 약정모계좌) 통장인자내용 or 고객명 |
| MractOtlt |	입금계좌인자내용 |	필드 |	25 |	선택 |	입금고객계좌 통장적용 인자내용 ex) 핀테크기업명 or 핀테크서비스명 |
### 3.3.3 타행입금이체 Response example
```json
{	
    "Header": {
        "Trtm": "003544",
        "Rsms": "정상처리 되었습니다.",
        "ApiNm": "ReceivedTransferOtherBank",
        "IsTuno": "201911290000000001",
        "Tsymd": "20191129",
        "FintechApsno": "001",
        "Iscd": "000019",
        "Rpcd": "00000",
        "ApiSvcCd": "ReceivedTransferA"
    }
}
```
### 3.3.4 타행입금이체 Response Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---:|:---:|:---:|:---:|:---:|:---:|  
| Header || 공통부 |||||	 

### 3.4.1 거래내역조회 Request example
```json
{
  "Header":{
      "ApiNm":"InquireTransactionHistory",
      "Tsymd":"20191129",
      "Trtm":"003544",
      "Iscd":"000019",
      "FintechApsno":"001",
      "ApiSvcCd":"ReceivedTransferA",
      "IsTuno":"201911290000000001",
      "AccessToken":
      "791c18f7377be31c8b30b27eba8573de0aac529890c7b18ac722f6120adc5054"},
    "Bncd":"011",
    "Acno":"3020000000109",
    "Insymd":"20191101",
    "Ineymd":"20191124",
    "TrnsDsnc":"A",
    "Lnsq":"ASC",
    "PageNo":"1",
    "Dmcnt":"5"
}
```
### 3.4.2 거래내역조회 Request Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---|:---:|:---:|:---:|:---|  
| Header || 공통부 |||||	 
| Bncd |	은행코드 |	필드 |	3 |	필수 |	농협은행:011, 상호금융:012 |
| Acno |	계좌번호 |	필드 |	20 |	필수 |	 
| Insymd |	조회시작일자 |	필드 |	8 |	필수 |	최고 1년 |
| Ineymd |	조회종료일자 |	필드 |	8 |	필수 |	조회기간: 최대 3개월 |
| TrnsDsnc |	거래구분 |	필드 |	1 |	- |	A:전체 M:입금 D:출금, default : A |
| Lnsq |	정렬순서 |	필드 |	10 |	- |	ASC:오름차순, DESC:내림차순, default:ASC |
| PageNo |	페이지번호 |	필드 |	4 |	- |	default : 1 조회건수 100건 초과하는 경우 (페이지번호 + 1)하여 연속거래 수행 |
| Dmcnt |	요청건수 |	필드 |	10 |	필수 |	최대 요청건수 100건 - 페이지당 건수 |
### 3.4.3 거래내역조회 Response example
```json
{
    "Header": {
        "Trtm": "003544",
        "Rsms": "정상처리 되었습니다.",
        "ApiNm": "InquireTransactionHistory",
        "IsTuno": "201911290000000001",
        "Tsymd": "20191129",
        "FintechApsno": "001",
        "Iscd": "000019",
        "Rpcd": "00000",
        "ApiSvcCd": "ReceivedTransferA"
    },
    "CtntDataYn": "N",
    "TotCnt": "1",
    "Iqtcnt": "1"
        "REC": [
        {
        	"Trdd": "20191124",
        	"Txtm": "222637",
        	"MnrcDrotDsnc": "3",
        	"Tram": "1004",
            "AftrBlnc": "1100097648",
            "TrnsAfAcntBlncSmblCd": "+",
            "Smr": null,
            "HnisCd": "000",
            "HnbrCd": "0000000",
            "Ccyn": "0",
            "Tuno": "700",
            "BnprCntn": "테스트"
        }
		]
}
```
### 3.4.4 거래내역조회 Response Element
| Element |	한글명 | Type |	Length |	optional |	Description |  
|:---|:---|:---:|:---:|:---:|:---:|  
| Header || 공통부 |||||	 
| CtntDataYn |	연속데이터여부 |	필드 |	1 |	필수 |	Y:이후데이터있음 |
| TotCnt |	총건수 |	필드 |	10 |	필수 |	미사용 |
| Iqtcnt |	조회총건수 |	필드 |	10 |	필수 |	 
| REC | 거래내역목록 |	반복부 |	 필수 |	최대 100건 |
| Trdd |	거래일자 |	필드 |	8 |	필수 |	 
| Txtm |	거래시각 |	필드 |	6 |	필수 |	 
| MnrcDrotDsnc |	입금출금구분 |	필드 |	1 |	필수 |	1:신규(입금) 2:입금 3:출금 4:해지(출금) |
| Tram |	거래금액 |	필드 |	15 |	필수 |	 
| AftrBlnc |	거래후잔액 |	필드 |	15 |	필수 |	 
| TrnsAfAcntBlncSmblCd | 	거래후계좌잔액부호코드 |	필드 |	1 |	필수 |	 
| Smr |	적요 |	필드 |	50 |	필수 |	 
| HnisCd |	최급기관코드 |	필드 |	3 |	필수 |	 
| HnbrCd |	취급지점코드 |	필드 |	7 | 필수 |	 
| Ccyn |	취소여부 |	필드 |	1 |	필수 |	정상:0, 취소:1 |
| Tuno |	거래고유번호 |	필드 |	50 |	필수 |	 
| BnprCntn |	통장인자내용 |	필드 |	20 |	필수 |	 
