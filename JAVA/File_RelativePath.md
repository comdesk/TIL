<h3>File 클래스의 상대경로</h3>
<hr>

<p>
  ~/src/main/java 에 있는 클래스에서 ~/src/main/resources/html에 있는 파일을 File 클래스로 상대경로를 이용해서 불러오려고 했는데 FileNotFoundException이 났다.<br>
  상대경로를 ../resources/html 이라고 지정했다. 상위 폴더의 resources/html 폴더이므로.<br>
  그런데 파일을 찾지 못했다.
</p>
<p>
  자바의 File 에서 사용되는 상대 경로의 기준은 해당 클래스 파일이 있는 위치가 아니라, 클래스 파일이 포함되어 있는 <strong>프로젝트 폴더</strong>이다.
  그래서 ~/src/main/java에 있는 클래스에서
</p>

```java
File file = new File(".");
System.out.println(file.getAbsolutePath());
```
<p>
  이렇게 찍어봤더니 src의 상위까지의 경로가 나왔다.<br>
  그래서 경로를 "./src/main/resources/html” 이렇게 지정해줬더니 파일을 제대로 찾았다.<br>
  <br>
  출처: https://ohgyun.com/169
</p>
