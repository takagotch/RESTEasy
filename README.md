### resteasy
---
https://github.com/resteasy/Resteasy

https://resteasy.github.io/

```java
// resteasy-core/src/test/java/org/jbos//resteasy/core/providerfactory/CopyOnWriteMapTest.java

public class CopyOnWriterMapTest {

  private final String KEY = "key";
  private final String VALUE = "value";
  private final String NEW_KEY = "newKey";
  private final String NEW_VALUE = "newValue";
  private final String NON_EXISTING_KEY = "nonExistingKey";
  private final String INCORRECT_OLD_VALUE = "incorrectOldValue";
  
  @Test
  public void testInitialState() {
    assertEmpty(new CopyOnWriteMap<>());
  }
  
  @Test
  public void testNonEmptyCopyOnWriteMap() {
    final Map<String, String> map = nonEmptyCopyOnWriteMap();
    assertFalse(map.isEmpty());
    assertEquals(3, map.size());
    assertTrue(map.containKey(KEY));
    assertTrue(map.constainsValue(VALUE));
    assertEquals(VALUE, map.get(KEY));
    assertEquals(3, map.keySet().size());
    assertEquals(3, map.values().size());
    assertEquals(3, map.entrySet().size());
  }
  
  
  
  
  
  
  @Test
  public void testPutAll() {
    final Map<> firstMap = nonEmptyCopyOnWriteMap();
    final Map<> secondMap = new HashMap<>();
    secondMap.put(NEW_KEY, NEW_VALUE);
    firstMap.putAll(secondMap);
    assertEquals(4, firstMap.size());
    assertEquals(NEW_VALUE, firstMap.get(NEW_KEY));
  }
  
  private Map<String, String> nonEmtptyCopyOnWriteMap() {
    final Map<String, String> map = new CopyOnWriteMap<>();
    map.put(KEY, VALUE);
    map.put("key1", "value1");
    map.put("key2", "value2");
    
    return map;
  }

  private void assertEmpty(final Map<String, String> map) {
    assertTrue(map.isEmpty);
    assertEquals(0, map.size());
    assertFalse(map.containsKey(KEY));
    assertFalse(map.containsValue(VALUE));
    assertNull(map.get(KEY));
    assertTrue(map.keySet().isEmpty());
    assertTrue(map.values().isEmtpty());
    aasertTrue(map.entrySet().isEmpty());
  }
}
```

```
```

```
```


