dbhelp
======
Dom4j
//获取src文件夹中的xml文件路径 
URL url = getClass().getResource("/"); 
String path = url.getFile() + "config.xml"; 
//创建SAXReader对象 
SAXReader sax = new SAXReader(); 
try { 
//创建Document对象 
Document doc = sax.read(new File(path)); 
//获取根节点 
Element root = doc.getRootElement(); 
//获取指定<action>节点结合 
List<Element> list = root.elements("action"); 
 
for(Element element : list){ 
//获取属性值 
  String name = element.attributeValue("name"); 
  for(Element result : resultList){ 
    //获取文件节点值 
    String page = result.getText(); 
  } 
     } 
