CSI2532 Playground

Arild Yonkeu Tchana
300123590

```bash
# psql -c "DROP DATABASE university"
psql -c "CREATE DATABASE university"
psql university -f ./db/schema.sql
psql university -f ./db/seed.sql
psql university -f ./db/test.sql
```

# Systêmes universitaire

## Diagramme ER

### Situation 1

![Diagram 1](images/Situation1.PNG)

```sql
CREATE TABLE professors (
    ssn int,
    PRIMARY KEY (ssn)
);

CREATE TABLE courses (
    courseid int,
    PRIMARY KEY (courseid)
);

CREATE TABLE teaches (
    ssn int,
    courseid int,
    semesterid int,
    PRIMARY KEY (ssn, courseid),
    FOREIGN KEY (ssn) REFERENCES professors,
    FOREIGN KEY (courseid) REFERENCES courses
);
```

### Situation 2

![Diagram 2](images/Situation2.PNG)

```sql
CREATE TABLE professors (
    ssn int,
    PRIMARY KEY (ssn)
);

CREATE TABLE courses (
    courseid int,
    PRIMARY KEY (courseid)
);

CREATE TABLE teaches (
    ssn int,
    courseid int,
    semesterid int,
    PRIMARY KEY (ssn, courseid),
    FOREIGN KEY (ssn) REFERENCES professors,
    FOREIGN KEY (courseid) REFERENCES courses
);
```

### Situation 3

![Diagram 3](images/Situation3.PNG)

```sql
CREATE TABLE professors (
    ssn int,
    PRIMARY KEY (ssn)
);

CREATE TABLE courses (
    courseid int,
    PRIMARY KEY (courseid)
);

CREATE TABLE teaches (
    ssn int,
    courseid int,
    semesterid int,
    PRIMARY KEY (ssn, courseid),
    FOREIGN KEY (ssn) REFERENCES professors,
    FOREIGN KEY (courseid) REFERENCES courses
);
```

### Situation 4

![Diagram 4](images/Situation4.PNG)

```sql
CREATE TABLE professors (
    ssn int,
    PRIMARY KEY (ssn)
);

CREATE TABLE courses (
    courseid int,
    PRIMARY KEY (courseid)
);

CREATE TABLE teaches (
    ssn int,
    courseid int,
    semesterid int,
    PRIMARY KEY (ssn, courseid),
    FOREIGN KEY (ssn) REFERENCES professors,
    FOREIGN KEY (courseid) REFERENCES courses
);
```
