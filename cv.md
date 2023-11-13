# Alexander Gamezo

## Personal Information
* Email:	[alexandergamezo@gmail.com](mailto:alexandergamezo@gmail.com)
* Phone:	+995595002687, +375297710766
* Location:	Georgia(Batumi), Belarus(Minsk)
* Discord nickname: @alexandergamezo
* LinkedIn:	[https://www.linkedin.com/in/alexandergamezo](https://www.linkedin.com/in/alexandergamezo)

## Summary
Strong foundation in .NET framework, C#, and ASP.NET. I have been actively involved in hands-on coding,
troubleshooting, and collaborating with experienced developers. I am a fast learner, detail-oriented, and
thrive in a team environment. Completed .NET development courses from EPAM in Belarus and Georgia.
Strong understanding of ASP.NET Web API, ASP.NET MVC, Entity Framework, AutoMapper, .NET Core,
Microsoft SQL Server, Postman API, and Git.

## Skills
* ASP.NET Web API
* ASP.NET MVC
* Entity Framework
* AutoMapper
* .NET Core
* Microsoft SQL Server
* Postman API
* Swagger
* Git

## Code Example
```
public AutomapperProfile()
{
  CreateMap<Game, GameModel>()
                .ForMember(gm => gm.Genres, g => g.MapFrom(x => x.GameGenres.Select(gr => new GenreModel { Id = gr.Genre.Id, Name = gr.Genre.Name })))
                .ReverseMap()
                .ForMember(g => g.Id, opt => opt.MapFrom<GameModelToGameConverter>())
                .ForMember(g => g.GameGenres, opt => opt.MapFrom((gm, g, _, context) =>
                {
                    return gm.Genres.Select(genre => new GameGenre
                    {
                        GameId = g.Id,
                        GenreId = genre.Id
                    }).ToList();
                }))
                .AfterMap((g, gm) =>
                {
                    gm.Id = g.Id;
                });
}
```
        
## Education
* Epam
    + EPAM CRE .NET - .NET Engineers Program (Georgia). [Project: GameStore](https://gitlab.com/alexandergamezo/gamestoreproject)
    + EPAM .Net Development (Georgia). [Project: ToDoApplication](https://gitlab.com/alexandergamezo/todo-application)   
    + EPAM .Net Development(Belarus). [Project: FileCabinetApplication](https://github.com/alexandergamezo/file-cabinet-task)
* Belarusian National Technical University, Minsk, Faculty of Transport Communications, Automobile Roads
* Belarusian National Technical University, Minsk, Institute of Qualification Advancement, Economics and Management on an Industrial Enterprise
* Belarusian State University of Physical Culture, Minsk, Institute of Qualification Advancement, Coaching Work (Wushu)

## Languages
* Belarusian
* Russian
* English: B1(CEFR, [EPAM English test result](https://telescope.epam.com/who/Aliaksandr_Hameza))
