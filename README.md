# SEA8 - Spring Data JPA Quest 02 - One-to-Many

## Challenge: The magic of Spring Data JPA

_Fork_ the following repository: https://github.com/WCS-Java-Training-Bonn-2019/quest-spring-jpa-onetomany.

You are taking over the development of a Harry Potter fan site to add the following features:

- a wizard should be able to enroll in one (and only one) school.
- it should be possible to retrieve the list of students enrolled in a school.

The first step will be to create the database *spring_jpa_onetomany* from **this sql file**:

```
curl -s https://raw.githubusercontent.com/WildCodeSchool/quest-spring-jpa-onetomany/master/database/spring_jpa_onetomany.sql | mysql -u root -p
```

The user is the same as in the previous quests: *h4rryp0tt3r* with the password *Horcrux4life*.
It will be necessary to give him all the rights on the database *spring_jpa_onetomany*:

```SQL
GRANT ALL PRIVILEGES ON spring_jpa_onetomany.* TO 'h4rryp0tt3r'@'localhost';
```

1. Modify the entity *Wizard* to add the code necessary to create its relationship with a school: *School school*
2. Modify the entity *School* to add the code necessary to create their relationship with a list of wizards: *List<Wizard> wizards*
3. Restart the server: requests to create the foreign key of its constraint should appear in the *logs*
4. Without modifying other classes, it should be possible to add a student to a school and see the list of students enrolled, from the "registration" link

If it doesn't work, check the error messages in the *logs*:

- did you name the attributes correctly as requested?
- did you create the getters and setters?

## Validation criterias

- The project runs correctly on the required database and user.
- The class *Wizard* contains all the code necessary to link a school.
- The class *School* contains all the code necessary to link a list of students.
- It is possible to register a student at a school from the "registration" link.
- It is possible to see the list of students enrolled in a school from the "registration" link.
- The code is available on GitHub.
