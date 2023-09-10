# 데이터베이스 다중화

## DB 클러스터링을 시스템에서 적용하는 이유:
1. Write와 Read operation의 분리로 인해, 병렬로 처리될 수 있는 query의 수가 늘어나고, 성능을 더 좋게할 수 있다.
2. Reliability(안정성)
3. Availability(가용성)
   - 2와 3번의 장점은, 대표적으로 서버의 장애발생으로 인한 후속조치와 연관이 있다.

## 구현 시 생각해야할 점:
1. Write operation은 마스터 db에서만 지원한다.
2. 부 DB는 주 데이터베이스로부터 그 사본을 전달받고, read operation만을 지원한다.
3. DB를 변경하는 명령어들 (ex: insert, delete, update 등)은 주 데이터베이스로만 전달되어야한다.






  
