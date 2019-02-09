# gson-javatime-serialisers

## Што это такое?


Набор GSON сериализаторов для использования java 8 java.time entities. Когда можно, ISO 8601 string representations исползованы. 

## Добывать его

'''
<dependency>
  <groupId>com.fatboyindustrial.gson-javatime-serialisers</groupId>
  <artifactId>gson-javatime-serialisers</artifactId>
  <version>1.1.1</version>
</dependency>
````

## Пользовать его

````
final Gson gson = Converters.registerOffsetDateTime(new GsonBuilder()).create();
final OffsetDateTime original = OffsetDateTime.now();

final String json = gson.toJson(original);
final OffsetDateTime reconstituted = gson.fromJson(json, OffsetDateTime.class);
````

## Тестировать

Не связяно с gson-javatime-serializers само, но если вы работаете с Java 8 time, вы можете выть заинтересованы в [`spencerwi/hamcrest-jdk8-time`][3]


[1]: https://code.google.com/p/google-gson/
[2]: http://docs.oracle.com/javase/8/docs/api/java/time/package-summary.html
[3]: https://github.com/spencerwi/hamcrest-jdk8-time







