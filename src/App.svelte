<script>
  import Navbar from "./components/Navbar.svelte";
  import Hero from "./components/Hero.svelte";
  import Destacados from "./components/Destacados.svelte";
  import Footer from "./components/Footer.svelte";
  import Colaborators from "./components/Colaborators.svelte";

  const navbarLinks = [
    { name: "Inicio", href: "/" },
    { name: "Nosotros", href: "/" },
    { name: "Proyectos", href: "/" },
    { name: "Contacto", href: "/" },
    { name: "Únete a nosotros", href: "/" },
  ];

  const destacados = [
    {
      title: `Acabamos de reunirnos los dos Comites Trabajemos Por Lorica y Comite Resistencia Ciudadana, en Pro de unir esfuerzo para lograr los objetivos trasados.`,
      description: "Reunión de los dos comites de Lorica",
      image:
        "https://scontent.feoh11-1.fna.fbcdn.net/v/t39.30808-6/460432538_522821157170680_586499730607974979_n.jpg?stp=dst-jpg_s600x600&_nc_cat=111&ccb=1-7&_nc_sid=833d8c&_nc_ohc=MZWyVNitf9YQ7kNvgEZthsp&_nc_ht=scontent.feoh11-1.fna&_nc_gid=AEtwE8Q9jFoio-VNY4qPL8K&oh=00_AYD3J0_SrG7-eyGN41T4Ft6B99sX-dvNDedOutdtTlGfKg&oe=66F65BB7",
      link: "https://www.facebook.com/photo?fbid=122111048540504523&set=a.122109503330504523",
      date: "Martes 17 de Septiembre de 2024",
      source: "Facebook - Comite Resistencia Ciudadana ",
    },
    {
      title:
        "“Estamos dispuestos a ayudar a avanzar para que se haga la variante de Lorica”: Zuleta",
      description: `“Estamos dispuestos a ayudar a avanzar para que se haga la variante de Lorica”: Zuleta
Erasmo Zuleta convoca reunión con Ruta al Mar tras declaraciones sobre inviabilidad del proyecto.
Tema del día
 5 días atrás

El gobernador de Córdoba, Erasmo Zuleta Bechara, participará este martes en una mesa de trabajo crucial con los directivos de la Concesión Ruta al Mar. El objetivo principal es abordar la polémica situación de la variante de Lorica, un proyecto que fue excluido del contrato de concesión y que, según Manuel Raigozo Rubio, gerente de Ruta al Mar, es “un proyecto a todas luces inviable financieramente”.`,
      image: "https://larazon.co/wp-content/uploads/2024/09/Erasmo-Zuleta.jpg",
      link: "https://larazon.co/temas-del-dia/estamos-dispuestos-a-ayudar-a-avanzar-para-que-se-haga-la-variante-de-lorica-zuleta/",
      date: "Martes 17 de Septiembre de 2024",
      source: "La razon",
    },
    {
      title: "Comunicado a la opinión pública.",
      description:
        "Comite resistencia ciudadana logro legalizar la organización.",
      image: "/assets/img/noticia2.jpg",
      link: "https://www.facebook.com/photo?fbid=122111048540504523&set=a.122109503330504523",
      date: "Martes 17 de Septiembre de 2024",
      source: "Facebook - Comite Resistencia Ciudadana ",
    },
  ];
  export let colaboradores = [
    {
      name: "Mendoza Ingenieria",
      logo: "/assets/img/empresa1.jpg",
      link: "https://example.com",
    },
    {
      name: "Diseños Modernos S.A.S",
      logo: "/assets/img/empresa2.jpg",
      link: "https://example.com",
    },
    {
      name: "TecnoSinú",
      logo: "/assets/img/empresa3.jpg",
      link: "https://example.com",
    },
  ];
</script>

<Navbar links={navbarLinks} />
<Hero />
<Destacados {destacados} />
<Colaborators {colaboradores} />
<Footer />
