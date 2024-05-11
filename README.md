```Java
...
import Developer from 'bahia-blanca';

@Getter
Class Hugo extends Developer{
  
  protected String name;
  protected String location;
  protected String title;
  protected String[] frontendTechs;
  protected String[] backendTechs;
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
    ];
    this.frontendTechs = [ 
      "Angular", 
      "Reactjs", 
      "Bootstrap", 
      "TailwindCSS", 
    ];
    this.backendTechs = [
      "Java",
      "Spring Boot",
      "NodeJS",
      "NestJS",
      "SQL",
    ];
    this.desiredJobs = new ArrayList<Job>() {
      {
        add(new Job("Godot Developer"));
        add(new Job("Backend Developer"));
        add(new Job("DevOps"));
      }
    this.job = new Job("Developer at Buenos Aires City Gobernment");
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

  kill(){
    throw new Exception("Impossible");
  }

  dm(){
    throw new Exception("What? This is just a README. Message him!");
  }
}
```

If you want to contact me, please send me a DM or email me from my webpage https://hugoitu.com.ar
