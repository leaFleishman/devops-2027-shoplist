1.ירוצו 2 קונטיינרים וייבנה image אחד
2.http://localhost:9001/hello/Rivka — יחזיר Shalom Rivka.
http://localhost:9002/hello/Rivka — יחזיר Hello Rivka.
3.כי הפורט כבר תפוס על ידי הראשון,לכל קונטיינר סביבה שונה (VM)   
4. greeter-fr:
    build:
      context: ../../02-docker-basics/homework/greeter
    ports:
      - "9003:9000"
    environment:
      GREETING: Bonjour
      5.כי הוא לא שומר נתונים רק אומר שלום
