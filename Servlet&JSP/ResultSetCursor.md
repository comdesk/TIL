ResultSet은 커서를 가진다.

IN JAVA 7 DOCS
public interface ResultSet
extends Wrapper, AutoCloseable
...
A ResultSet object maintains a cursor pointing to its current row of data. Initially the cursor is positioned before the first row.

맨 처음에 커서는 첫 번째 행이 아닌, 첫 번째 행 앞에 있다.
그래서 ResultSet을 가져올 때, 처음부터 rs.next()를 해야 첫 번째 행부터 가져올 수 있는 것이다.

if(rs.next())든, while(rs.next())든 커서를 한 칸 다음으로 움직이고, 로직을 시작한다.


<h3>rs.absolute(int row)</h3>
예: 맨 처음에 rs.absolute(5);면 커서는 5행에 존재한다.

그래서
rs.absolute(5);

while(rs.next()) {
  ;;
}
일때,
while에서는 6번째 행부터 커서가 시작한다.
