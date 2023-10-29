# Тестирование с JUnit и Allure

Примеры из [https://github.com/mkyong/junit5-examples](https://github.com/mkyong/junit5-examples)

САМЫЕ различные тесты с allure, params, conditional, display и чего только нет.

Проведение тестов: 

Maven:

````shell
mvn test
````

Gradle:

````shell
./gradlew test
````

Прогон конкретного теста:

````shell
./gradlew test --tests '*AssumptionsTest'
./gradlew test --tests com.mkyong.AssumptionsTest
./gradlew test --tests 'com.mkyong.assertions*'
./gradlew test --tests '*Assumptions*'
````

Разные варианты тестирования:

````shell
gradle test --tests '*SomeTest.someSpecificFeature'
gradle test --tests '*SomeSpecificTest'

gradle test --tests '*IntegTest'
gradle test --tests '*IntegTest*ui*'
gradle test --tests '*IntegTest.singleMethod'
````

Просмотр отчетов:

````shell
allure serve allure-results/
````

![Результаты](doc/result.png)

Пример использования: [https://github.com/cherepakhin/companies](https://github.com/cherepakhin/companies). В этом же репозитории (companies) применение для интеграционного тестирования.

Перед использованием в **codespace github** установить программу allure:

````shell
apt install allure
````

После этого выполнить:

````shell
./node_modules/allure-commandline/bin/allure serve allure-results/
````
