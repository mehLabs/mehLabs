```Java
...
import java.util.ArrayList;
import java.util.List;

@Getter
class Hugo extends Developer {
  
  protected String location;
  protected String title;
  protected String[] frontendTechs;
  protected String[] backendTechs;
  protected String[] interests;
  protected Job job;
  protected List<Job> desiredJobs;

  Hugo() {
    super("Hugo Iturrieta");
    this.location = "Bahía Blanca, Argentina";
    this.title = "FullStack Developer";
    this.interests = new String[] {
      "Guitar",
      "Videogames",
      "Travel",
      "Cats",
      "Economics",
      "Philosophy"
    };
    this.frontendTechs = new String[] { 
      "Angular", 
      "Reactjs", 
      "Bootstrap", 
      "TailwindCSS"
    };
    this.backendTechs = new String[] {
      "Java",
      "Spring Boot",
      "NodeJS",
      "NestJS",
      "SQL"
    };
    this.desiredJobs = new ArrayList<Job>() {{
      add(new Job("Godot Developer"));
      add(new Job("Backend Developer"));
      add(new Job("DevOps"));
    }};
    this.job = new Job("Developer at Buenos Aires City Government");
  }

  public void employ(Job newJob) {
    for(Job desiredJob : this.desiredJobs) {
      if (newJob.equals(desiredJob)) {
        this.job = newJob;
        System.out.println("Thank you so much! You'll have such a great person and professional");
        return;
      }
    }
    throw new RuntimeException("Nice offer, thank you. I'll... contact you... some day...");
  }

  public void kill() {
    throw new RuntimeException("Impossible");
  }

  public void dm() {
    throw new RuntimeException("What? This is just a README. Message him!");
  }
}

```

If you want to contact me, please send me a DM or email me from my webpage https://hugoitu.com.ar
