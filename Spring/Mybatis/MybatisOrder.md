<h3>mybatis-config.xml 순서</h3>
<hr>

<p>
    mybatis-config.xml, 즉 마이바티스 설정파일에 Mapper 인터페이스와 Mapper.xml 파일을 동시에 등록해서 혼용해서 사용하려고 할 때, 
</p>
<fieldset>
    &lt;mappers&gt;
    	&lt;mapper class="org.zerock.myapp.mapper.BoardMapper" /&gt;
        &lt;!-- <package name="" />      --&gt;
    
        &ltmapper resource="mappers/BoardMapper.xml" /&gt;
        &lt;!-- <mapper url=""/> --&gt;        
    &lt;/mappers&gt;
</fieldset>
<p>
    이렇게 Mapper 인터페이스를 먼저 mappers 태그에 등록하고 xml 파일을 등록해야지, xml 파일을 먼저 등록하고 Mapper 인터페이스를 나중에 등록하면 
    <b>Type interface org.zerock.myapp.mapper.BoardMapper is already known to the MapperRegistry.</b> 
    오류가 난다.
</p>