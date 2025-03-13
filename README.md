```Java
...
import java.util.ArrayList;
import java.util.List;

@Getter
class Hugo<T extends Job> extends Developer<T> {
  
  protected String location;
  protected String title;
  protected String[] frontendTechs;
  protected String[] backendTechs;
  protected String[] interests;
  protected T job;
  protected List<T> desiredJobs;

  public Hugo() {
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
      "SQL",
      ".NET Core"
    };
    this.desiredJobs = new ArrayList<Job>() {{
      add(new T("Godot Developer"));
      add(new T("Backend Developer"));
      add(new T("DevOps"));
    }};
    this.job = new T("Developer at Buenos Aires City Government");
  }

  public String employ(T newJob) {
    for(T desiredJob : this.desiredJobs) {
      if (newJob.equals(desiredJob)) {
        this.job = newJob;
        return "Thank you so much! You'll have such a great person and professional";
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

If you want to contact me, please send me a DM or email me from my webpage https://hugoitu.com.ar (UPDATE: DOWN)
