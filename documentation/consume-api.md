# API

1. Post message

   ```shell
   curl -s -k -d "@people.json" -H "Content-Type: application/json" -X POST https://localhost:8443/api/people
   ```

   A saída deve ser parecida com isso:

   ```json
   {
     "id": "1234567890",
     "name": "Marcos Vallim",
     "height": 186,
     "mass": 80,
     "hair_color": "branco",
     "skin_color": "branco",
     "eye_color": "marron",
     "birth_year": "1980",
     "gender": "masculino",
     "created": "2019-07-28T00:00:00.000+0000",
     "edited": "2019-07-28T00:00:00.000+0000"
   }
   ```

2. Spring console application

   ```text
      .   ____          _            __ _ _
     /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
    ( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
     \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
      '  |____| .__|_| |_|_| |_\__, | / / / /
     =========|_|==============|___/=/_/_/_/
     :: Spring Boot ::        (v2.1.2.RELEASE)

    20:52:15.961 [main] INFO  com.ciandt.SpringKafkaApplication - Starting SpringKafkaApplication on cooler with PID 19251 (/home/mvallim/Projects/workspace/spring-kafka-schema-registry-ssl/target/classes started by mvallim in /home/mvallim/Projects/workspace/spring-kafka-schema-registry-ssl)
    20:52:15.963 [main] INFO  com.ciandt.SpringKafkaApplication - No active profile set, falling back to default profiles: default
    20:52:18.882 [main] INFO  com.ciandt.SpringKafkaApplication - Started SpringKafkaApplication in 3.136 seconds (JVM running for 3.469)
    20:52:43.173 [https-jsse-nio-8443-exec-5] INFO  c.c.application.PeopleApplication - sending payload='com.ciandt.model.People@94718fb'
    20:52:43.512 [https-jsse-nio-8443-exec-5] WARN  o.a.k.c.producer.ProducerConfig - The configuration 'auto.register.schemas' was supplied but isn't a known config.
    20:52:43.512 [https-jsse-nio-8443-exec-5] WARN  o.a.k.c.producer.ProducerConfig - The configuration 'specific.avro.reader' was supplied but isn't a known config.
    20:52:43.512 [https-jsse-nio-8443-exec-5] WARN  o.a.k.c.producer.ProducerConfig - The configuration 'value.subject.name.strategy' was supplied but isn't a known config.
    20:52:44.535 [org.springframework.kafka.KafkaListenerEndpointContainer#0-0-C-1] INFO  c.c.application.PeopleApplication - received payload='{"id": "1234567890", "name": "Marcos Vallim", "height": 186, "mass": 80, "hair_color": "branco", "skin_color": "branco", "eye_color": "marron", "birth_year": "1980", "gender": "masculino", "created": 1564272000000, "edited": 1564272000000}'
   ```
