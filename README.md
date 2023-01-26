# COS PRO Java 1급 - 모의고사4
1
### 4차) 문제1 - 사전에서 단어찾기
```Java
import java.util.*;

public class Main {
		//코드 한줄 수정
    String[] vowels = {"A", "E", "I", "O", "U"};
    ArrayList<String> words;
    public void create_words(int lev, String str) {
        words.add(str); //빈문자열 추가
				// vowels의 인덱스 번호
        for (int i = 0; i < 5; i++) {
            if (lev < 5) {
								//A를 먼저 A, AA, AAA, AAAA, AAAAA 를 추가해줘야함
								//lev는 단어의 길이
								// System.out.println("i: " + i + "lev: " + lev+ "단어: "+str+vowels[i]);
                create_words(lev+1, str.concat(vowels[i])); 
            }
        }
    }
    
    public int solution(String word) { // word = "AAAAE"
        int answer = 0;
        words  = new ArrayList<String>();
        create_words(0, "");
        for (int i = 0; i < words.size(); i++) {
						//사전의 i번째 있는 값을 비교해서 두개가 같으면 answer에 i번 인덱스를 넣어준다.
            if (word.equals(words.get(i))) {
                answer = i;
                break;
            }
        }
        return answer;
    }

    public static void main(String[] args) {
        Main sol = new Main();
        String word1 = new String("AAAAE");
        int ret1 = sol.solution(word1);

        // [실행] 버튼을 누르면 출력 값을 볼 수 있습니다.
        System.out.println("solution 메소드의 반환 값은 " + ret1 + " 입니다.");

        String word2 = new String("AAAE");
        int ret2 = sol.solution(word2);

        // [실행] 버튼을 누르면 출력 값을 볼 수 있습니다.
        System.out.println("solution 메소드의 반환 값은 " + ret2 + " 입니다.");
    }
}
```

### 4차) 문제2 - 
```Java
```

### 4차) 문제3 - 
```Java
```

### 4차) 문제4 - 
```Java
```

### 4차) 문제5 - 
```Java
```

### 4차) 문제6 - 
```Java
```

### 4차) 문제7 - 
```Java
```

### 4차) 문제8 - 
```Java
```

### 4차) 문제9 - 
```Java
```

### 4차) 문제10 - 
```Java
```
