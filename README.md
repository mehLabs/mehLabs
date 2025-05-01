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

  public Hugo() {
    super("Hugo Iturrieta");
    this.location = "Bahía Blanca, Argentina";
    this.title = "Software Developer";
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
      add(new Job("Godot Developer")); // yes please
      add(new Job("Backend Developer"));
      // add(new Job("DevOps")); // maybe in a future, but not for now
    }};
    this.job = new Job("Software Developer at Buenos Aires City Government");
  }

  public String employ(Job newJob) {
    throw new RuntimeException("Sorry but currently not available");
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
