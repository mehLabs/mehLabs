```Java
...
import Developer from 'bahia-blanca';

@Getter
Class FullStack extends Developer{
  
  protected String name;
  protected String location;
  protected String title;
  protected String[] frontend;
  protected String[] backend;
  protected Job job;

  FullStack(){
    this.name = "Hugo Iturrieta";
    this.location = "Bahía Blanca, Argentina";
    this.title = "FullStack Developer";
    this.frontend = [ 
      "JavaScript", 
      "Typescript", 
      "Angular", 
      "Reactjs", 
      "Redux", 
      "Bootstrap", 
      "TailwindCSS", 
      "CSSModules" 
    ];
    this.backend = [
      "Java",
      "Spring Boot",
      "NodeJS",
      "ExpressJS",
      "MySQL",
      "PostgreSQL"
    ]
    this.job = new Job("Stretcher Bearer in a Hospital");
  }

  darEmpleo(Empleo newEmpleo){
    this.empleo = newEmpleo;
    System.out.println("Thank you so much! You'll have such a great person and professional");
  }
  
}
```
