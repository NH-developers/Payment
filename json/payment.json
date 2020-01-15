{
	"swagger": "2.0",
	"schemes" : ["https"],
	"host": "developers.nonghyup.com",
	"tags": [
		{
			"name": "2.간편결제"
		}
	],
	"paths": {
		"/InquireDepositorAccountNumber.nh": {
			"post": {
				"tags": [
					"2.간편결제"
				],
				"summary": "예금주조회",
				"description": "핀-어카운트 연결계좌에 대한 예금주명을 조회한다.",
				"consumes": [
					"application/json"
				],
				"produces": [
					"application/json"
				],
				"parameters": [
					{
						"in": "body",
						"name": "param",
						"description": "param",
						"required": true,
						"schema": {
							"$ref": "#/definitions/InquireDepositorFinAccountRequestData"
						}
					}
				],
				"responses": {
					
				},
				"deprecated": false
			}
		},
		"/InquireDepositorOtherBank.nh": {
			"post": {
				"tags": [
					"2.간편결제"
				],
				"summary": "타행예금주조회",
				"description": "계좌에 대한 예금주명을 조회한다.",
				"consumes": [
					"application/json"
				],
				"produces": [
					"application/json"
				],
				"parameters": [
					{
						"in": "body",
						"name": "param",
						"description": "param",
						"required": true,
						"schema": {
							"$ref": "#/definitions/InquireDepositorOtherBankRequestData"
						}
					}
				],
				"responses": {
					
				},
				"deprecated": false
			}
		},
		"/DrawingTransfer.nh": {
			"post": {
				"tags": [
					"2.간편결제"
				],
				"summary": "출금이체",
				"description": "핀-어카운트 연결계좌에서 출금하여 핀테크기업 약정계좌로 출금이체를 한다.",
				"consumes": [
					"application/json"
				],
				"produces": [
					"application/json"
				],
				"parameters": [
					{
						"in": "body",
						"name": "param",
						"description": "param",
						"required": true,
						"schema": {
							"$ref": "#/definitions/DrawingTransferRequestData"
						}
					}
				],
				"responses": {
					
				},
				"deprecated": false
			}
		},
		"/ReceivedTransferAccountNumber.nh": {
			"post": {
				"tags": [
					"2.간편결제"
				],
				"summary": "농협입금이체",
				"description": "핀테크기업 약정계좌에서 출금하여 핀-어카운트 연결계좌로 입금이체를 한다.",
				"consumes": [
					"application/json"
				],
				"produces": [
					"application/json"
				],
				"parameters": [
					{
						"in": "body",
						"name": "param",
						"description": "param",
						"required": true,
						"schema": {
							"$ref": "#/definitions/ReceivedTransferAccountNumberRequestData"
						}
					}
				],
				"responses": {
					
				},
				"deprecated": false
			}
		},
		"/ReceivedTransferOtherBank.nh": {
			"post": {
				"tags": [
					"2.간편결제"
				],
				"summary": "타행입금이체",
				"description": "핀테크기업 약정계좌에서 출금하여 타행계좌로 입금이체를 한다.",
				"consumes": [
					"application/json"
				],
				"produces": [
					"application/json"
				],
				"parameters": [
					{
						"in": "body",
						"name": "param",
						"description": "param",
						"required": true,
						"schema": {
							"$ref": "#/definitions/ReceivedTransferOtherBankRequestData"
						}
					}
				],
				"responses": {
					
				},
				"deprecated": false
			}
		},
		"/InquireTransactionHistory.nh": {
			"post": {
				"tags": [
					"2.간편결제"
				],
				"summary": "거래내역조회",
				"description": " 핀-어카운트 연결계좌에 대한 거래내역을 조회한다.",
				"consumes": [
					"application/json"
				],
				"produces": [
					"application/json"
				],
				"parameters": [
					{
						"in": "body",
						"name": "param",
						"description": "param",
						"required": true,
						"schema": {
							"$ref": "#/definitions/InquireTransactionHistoryRequestData"
						}
					}
				],
				"responses": {
					
				},
				"deprecated": false
			}
		}
	},
	"definitions": {
		"InquireDepositorFinAccountRequestData": {
			"type": "object",
			"required": [
				"Header",
				"Bncd",
				"Acno"
			],
			"properties": {
				"Header": {
					"$ref": "#/definitions/InquireDepositorAccountNumberHeader"
				},
				"Bncd": {
					"type": "string",
					"example": "은행코드를입력하세요",
					"description": "은행코드"
				},
				"Acno": {
					"type": "string",
					"example": "계좌번호를입력하세요",
					"description": "계좌번호"
				}
			},
			"title": "InquireDepositorFinAccountRequestData"
		},
		"InquireDepositorOtherBankRequestData": {
			"type": "object",
			"required": [
				"Header",
				"Bncd",
				"Acno"
			],
			"properties": {
				"Header": {
					"$ref": "#/definitions/InquireDepositorOtherBankHeader"
				},
				"Bncd": {
					"type": "string",
					"example": "은행코드를입력하세요",
					"description": "은행코드"
				},
				"Acno": {
					"type": "string",
					"example": "계좌번호를입력하세요",
					"description": "계좌번호"
				}
			},
			"title": "InquireDepositorOtherBankRequestData"
		},
		"DrawingTransferRequestData": {
			"type": "object",
			"required": [
				"Header",
				"FinAcno",
				"Tram",
				"DractOtlt"
			],
			"properties": {
				"Header": {
					"$ref": "#/definitions/DrawingTransferHeader"
				},
				"FinAcno": {
					"type": "string",
					"example": "핀어카운트",
					"description": "핀어카운트"
				},
				"Tram": {
					"type": "string",
					"example": "거래금액",
					"description": "거래금액"
				},
				"DractOtlt": {
					"type": "string",
					"example": "출금계좌인자내용",
					"description": "출금계좌인자내용"
				}
			},
			"title": "DrawingTransferRequestData"
		},
		"ReceivedTransferAccountNumberRequestData": {
			"type": "object",
			"required": [
				"Header",
				"Bncd",
				"Acno",
				"Tram",
				"DractOtlt",
				"Acno"
			],
			"properties": {
				"Header": {
					"$ref": "#/definitions/ReceivedTransferAccountNumberHeader"
				},
				"Bncd": {
					"type": "string",
					"example": "은행코드",
					"description": "은행코드"
				},
				"Acno": {
					"type": "string",
					"example": "계좌번호를입력하세요",
					"description": "계좌번호"
				},
				"Tram": {
					"type": "string",
					"example": "거래금액",
					"description": "거래금액"
				},
				"DractOtlt": {
					"type": "string",
					"example": "출금계좌인자내용",
					"description": "출금계좌인자내용"
				},
				"MractOtlt": {
					"type": "string",
					"example": "입금계좌인자내용",
					"description": "입금계좌인자내용"
				}
			},
			"title": "ReceivedTransferRequestData"
		},
		"ReceivedTransferOtherBankRequestData": {
			"type": "object",
			"required": [
				"Header",
				"Bncd",
				"Acno",
				"Tram",
				"DractOtlt",
				"Acno"
			],
			"properties": {
				"Header": {
					"$ref": "#/definitions/ReceivedTransferOtherBankHeader"
				},
				"Bncd": {
					"type": "string",
					"example": "은행코드",
					"description": "은행코드"
				},
				"Acno": {
					"type": "string",
					"example": "계좌번호를입력하세요",
					"description": "계좌번호"
				},
				"Tram": {
					"type": "string",
					"example": "거래금액",
					"description": "거래금액"
				},
				"DractOtlt": {
					"type": "string",
					"example": "출금계좌인자내용",
					"description": "출금계좌인자내용"
				},
				"MractOtlt": {
					"type": "string",
					"example": "입금계좌인자내용",
					"description": "입금계좌인자내용"
				}
			},
			"title": "ReceivedTransferOtherBankRequestData"
		},
		"InquireTransactionHistoryRequestData": {
			"type": "object",
			"required": [
				"Header",
				"Bncd",
				"Acno",
				"Insymd",
				"Ineymd",
				"TrnsDsnc",
				"Lnsq",
				"PageNo",
				"Dmcnt"
			],
			"properties": {
				"Header": {
					"$ref": "#/definitions/InquireTransactionHistoryHeader"
				},
				"Bncd": {
					"type": "string",
					"example": "은행코드",
					"description": "은행코드"
				},
				"Acno": {
					"type": "string",
					"example": "계좌번호",
					"description": "계좌번호"
				},
				"Insymd": {
					"type": "string",
					"example": "조회시작일자",
					"description": "조회시작일자"
				},
				"Ineymd": {
					"type": "string",
					"example": "조회종료일자",
					"description": "조회종료일자"
				},
				"TrnsDsnc": {
					"type": "string",
					"example": "A",
					"description": "거래구분"
				},
				"Lnsq": {
					"type": "string",
					"example": "DESC",
					"description": "정렬순서"
				},
				"PageNo": {
					"type": "string",
					"example": "1",
					"description": "페이지번호"
				},
				"Dmcnt": {
					"type": "string",
					"example": "100",
					"description": "요청건수"
				}
			},
			"title": "InquireTransactionHistoryRequestData"
		},
		"InquireDepositorAccountNumberHeader": {
			"type": "object",
			"required": [
				"AccessToken",
				"ApiNm",
				"ApiSvcCd",
				"FintechApsno",
				"IsTuno",
				"Iscd",
				"Trtm",
				"Tsymd"
			],
			"properties": {
				"ApiNm": {
					"type": "string",
					"example": "InquireDepositorAccountNumber",
					"description": "API명"
				},
				"Tsymd": {
					"type": "string",
					"example": "오늘날짜를입력하세요",
					"description": "전송일자"
				},
				"Trtm": {
					"type": "string",
					"example": "112428",
					"description": "전송시각"
				},
				"Iscd": {
					"type": "string",
					"example": "기관코드를입력하세요",
					"description": "기관코드"
				},
				"FintechApsno": {
					"type": "string",
					"example": "001",
					"description": "핀테크앱일련번호"
				},
				"ApiSvcCd": {
					"type": "string",
					"example": "DrawingTransferA",
					"description": "API서비스코드"
				},
				"IsTuno": {
					"type": "string",
					"example": "0000",
					"description": "기관 거래고유번호"
				},
				"AccessToken": {
					"type": "string",
					"example": "인증키를입력하세요",
					"description": "접근토큰"
				}
			},
			"title": "InquireDepositorAccountNumberHeader",
			"description": "공통부"
		},
		"InquireDepositorOtherBankHeader": {
			"type": "object",
			"required": [
				"AccessToken",
				"ApiNm",
				"ApiSvcCd",
				"FintechApsno",
				"IsTuno",
				"Iscd",
				"Trtm",
				"Tsymd"
			],
			"properties": {
				"ApiNm": {
					"type": "string",
					"example": "InquireDepositorOtherBank",
					"description": "API명"
				},
				"Tsymd": {
					"type": "string",
					"example": "오늘날짜를입력하세요",
					"description": "전송일자"
				},
				"Trtm": {
					"type": "string",
					"example": "112428",
					"description": "전송시각"
				},
				"Iscd": {
					"type": "string",
					"example": "기관코드를입력하세요",
					"description": "기관코드"
				},
				"FintechApsno": {
					"type": "string",
					"example": "001",
					"description": "핀테크앱일련번호"
				},
				"ApiSvcCd": {
					"type": "string",
					"example": "DrawingTransferA",
					"description": "API서비스코드"
				},
				"IsTuno": {
					"type": "string",
					"example": "0000",
					"description": "기관 거래고유번호"
				},
				"AccessToken": {
					"type": "string",
					"example": "인증키를입력하세요",
					"description": "접근토큰"
				}
			},
			"title": "InquireDepositorOtherBankHeader",
			"description": "공통부"
		},
		"DrawingTransferHeader": {
			"type": "object",
			"required": [
				"AccessToken",
				"ApiNm",
				"ApiSvcCd",
				"FintechApsno",
				"IsTuno",
				"Iscd",
				"Trtm",
				"Tsymd"
			],
			"properties": {
				"ApiNm": {
					"type": "string",
					"example": "DrawingTransfer",
					"description": "API명"
				},
				"Tsymd": {
					"type": "string",
					"example": "오늘날짜를입력하세요",
					"description": "전송일자"
				},
				"Trtm": {
					"type": "string",
					"example": "112428",
					"description": "전송시각"
				},
				"Iscd": {
					"type": "string",
					"example": "기관코드를입력하세요",
					"description": "기관코드"
				},
				"FintechApsno": {
					"type": "string",
					"example": "001",
					"description": "핀테크앱일련번호"
				},
				"ApiSvcCd": {
					"type": "string",
					"example": "DrawingTransferA",
					"description": "API서비스코드"
				},
				"IsTuno": {
					"type": "string",
					"example": "0000",
					"description": "기관 거래고유번호"
				},
				"AccessToken": {
					"type": "string",
					"example": "인증키를입력하세요",
					"description": "접근토큰"
				}
			},
			"title": "DrawingTransferHeader",
			"description": "공통부"
		},
		"ReceivedTransferAccountNumberHeader": {
			"type": "object",
			"required": [
				"AccessToken",
				"ApiNm",
				"ApiSvcCd",
				"FintechApsno",
				"IsTuno",
				"Iscd",
				"Trtm",
				"Tsymd"
			],
			"properties": {
				"ApiNm": {
					"type": "string",
					"example": "ReceivedTransferAccountNumber",
					"description": "API명"
				},
				"Tsymd": {
					"type": "string",
					"example": "오늘날짜를입력하세요",
					"description": "전송일자"
				},
				"Trtm": {
					"type": "string",
					"example": "112428",
					"description": "전송시각"
				},
				"Iscd": {
					"type": "string",
					"example": "기관코드를입력하세요",
					"description": "기관코드"
				},
				"FintechApsno": {
					"type": "string",
					"example": "001",
					"description": "핀테크앱일련번호"
				},
				"ApiSvcCd": {
					"type": "string",
					"example": "ReceivedTransferA",
					"description": "API서비스코드"
				},
				"IsTuno": {
					"type": "string",
					"example": "0000",
					"description": "기관 거래고유번호"
				},
				"AccessToken": {
					"type": "string",
					"example": "인증키를입력하세요",
					"description": "접근토큰"
				}
			},
			"title": "ReceivedTransferAccountNumberHeader",
			"description": "공통부"
		},
		"ReceivedTransferOtherBankHeader": {
			"type": "object",
			"required": [
				"AccessToken",
				"ApiNm",
				"ApiSvcCd",
				"FintechApsno",
				"IsTuno",
				"Iscd",
				"Trtm",
				"Tsymd"
			],
			"properties": {
				"ApiNm": {
					"type": "string",
					"example": "ReceivedTransferOtherBank",
					"description": "API명"
				},
				"Tsymd": {
					"type": "string",
					"example": "오늘날짜를입력하세요",
					"description": "전송일자"
				},
				"Trtm": {
					"type": "string",
					"example": "112428",
					"description": "전송시각"
				},
				"Iscd": {
					"type": "string",
					"example": "기관코드를입력하세요",
					"description": "기관코드"
				},
				"FintechApsno": {
					"type": "string",
					"example": "001",
					"description": "핀테크앱일련번호"
				},
				"ApiSvcCd": {
					"type": "string",
					"example": "ReceivedTransferA",
					"description": "API서비스코드"
				},
				"IsTuno": {
					"type": "string",
					"example": "0000",
					"description": "기관 거래고유번호"
				},
				"AccessToken": {
					"type": "string",
					"example": "인증키를입력하세요",
					"description": "접근토큰"
				}
			},
			"title": "ReceivedTransferOtherBankHeader",
			"description": "공통부"
		},
		"InquireTransactionHistoryHeader": {
			"type": "object",
			"required": [
				"AccessToken",
				"ApiNm",
				"ApiSvcCd",
				"FintechApsno",
				"IsTuno",
				"Iscd",
				"Trtm",
				"Tsymd"
			],
			"properties": {
				"ApiNm": {
					"type": "string",
					"example": "InquireTransactionHistory",
					"description": "API명"
				},
				"Tsymd": {
					"type": "string",
					"example": "오늘날짜를입력하세요",
					"description": "전송일자"
				},
				"Trtm": {
					"type": "string",
					"example": "112428",
					"description": "전송시각"
				},
				"Iscd": {
					"type": "string",
					"example": "기관코드를입력하세요",
					"description": "기관코드"
				},
				"FintechApsno": {
					"type": "string",
					"example": "001",
					"description": "핀테크앱일련번호"
				},
				"ApiSvcCd": {
					"type": "string",
					"example": "ReceivedTransferA",
					"description": "API서비스코드"
				},
				"IsTuno": {
					"type": "string",
					"example": "0000",
					"description": "기관 거래고유번호"
				},
				"AccessToken": {
					"type": "string",
					"example": "인증키를입력하세요",
					"description": "접근토큰"
				}
			},
			"title": "InquireTransactionHistoryHeader",
			"description": "공통부"
		}
	}
}