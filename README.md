# pdfToText
Python code, PDF file to Text file

파이썬프로그램.
PyMuPDF 모듈을 이용하여 영문 PDF 파일에서 문자를 추출하여 영문 텍스트파일로 저장한다음
이 파일을 한 문장 단위로 읽어 네이버 파파고 API를 사용하여 번역한다음 한글 텍스트파일로 저장하는 코드.

네이버 파파고 API 번역 함수
def papagoAPI(id, secret, sentence)

Pdf 파일에서 영어 문자를 추출하나 모든 단어에 개행문자 "\n"이 포함되어 있어서
"\n"을 제거한다음 단어에 "." 마침표가 포함된 단어를 정규표현식으로 찾아서 "\n"을 포함,
하나의 문장을 만들고 영어텍스트 파일로 저장하는 함수
def pdfToText(inputFile)

Papago API 함수 결과값을 받아서 한글파일로 저장하는 함수
def trans(id, secret, inputfile, line=10)
