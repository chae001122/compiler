# C language compiler

# 사용환경 : nix

# 사용법

yacc -d kim.y  
lex kim.l  
cc y.tab.c lex.yy.c support.c semantic.c print.c print_seman.c generator.c  
-> a.out 실행파일 생성됨    
  
test할 c파일로 어셈블리 코드 생성  
ex) ./a.out test.c  
-> a.asm 파일 생성됨  
  
yacc -d int.y  
lex int.l  
cc -o inter y.tab.c lex.yy.c int.c lib.c  
-> inter 실행파일 생성됨  
  
./inter a.asm  
-> 어셈블리 코드 실행 과정과 프로그램 결과 출력  
