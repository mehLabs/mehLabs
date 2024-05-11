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
  protected String[] interests;
  protected Job job;
  protected List<Job> desiredJobs;

  FullStack(){
    this.name = "Hugo Iturrieta";
    this.location = "Bahía Blanca, Argentina";
    this.title = "FullStack Developer";
    this.interests = [
      "Guitar",
      "Videogames",
      "Travel",
      "Cats",
      "Economics",
      "Philosophy"
    ]
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
    ];
    this.desiredJobs = new ArrayList<Job>() {
      {
        add(new Job("Frontend developer"));
        add(new Job("Backend developer"));
        add(new Job("FullStack developer"));
      }
    this.job = new Job("Stretcher Bearer in a Hospital");
  }

  employ(Job newJob){
    for(int i=0; i < this.desiredJobs.size(); i++){
      Job desiredJob = this.desiredJobs.get(i);
      if (newJob.equals(desiredJob)){
        this.job = newJob;
        System.out.println("Thank you so much! You'll have such a great person and professional");
        break;
      }
    }
  }
  
}
```

If you want to contact me, please send me a DM or email me from my webpage https://hugoitu.com.ar
