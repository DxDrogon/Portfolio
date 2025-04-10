<script>
  let projektek = [
    {
      cim: "Bevásárlólista",
      leiras: "Ez a projekt egy egyszerű bevásárlólista amihez hozzá lehet adni és törölni lehet termékeket.",
      url: "https://dxdrogon.github.io/Bevasarlolista/"
    },
    {
      cim: "Lista",
      leiras: "Ez egy szimpla lista ami különböző gyümölcsöket listázik ki.",
      url: "https://dxdrogon.github.io/Lista/"
    },
    {
      cim: "Órai lista",
      leiras: "Ez egy szimpla lista ami különböző állatokat listázik ki.",
      url: "https://dxdrogon.github.io/OraiLista/"
    },
    {
      cim: "Labda",
      leiras: "Egy pattogó labda.",
      url: "https://dxdrogon.github.io/Ball/"
    },
    {
      cim: "Számológép",
      leiras: "Egy számológép ami a négy alapműveletet tudja elvégezni.",
      url: "https://dxdrogon.github.io/Szamologep/"
    },
    {
      cim: "Kő-papír-olló",
      leiras: "Ez egy egyszerű kő-papír-olló játék.",
      url: "https://dxdrogon.github.io/Rockpaperscissors/"
    },
    {
      cim: "Palindróm",
      leiras: "Ez a program megmondja, hogy egy adott szó palindróm-e.",
      url: "https://dxdrogon.github.io/Palindrome/"
    },
    {
      cim: "Óra",
      leiras: "Ez a program megjeleníti a pontos időt.",
      url: "https://dxdrogon.github.io/Clock/"
    },
    {
      cim: "BMI",
      leiras: "Év végi projekt, ami egy filmes weboldal.",
      url: "https://bibliothecamotusimaginibus.netlify.app"
    },
  {
      cim: "Naptár",
      leiras: "Ez a projekt egy szimpla naptár havi és heti nézettel",
      url: "https://calendarfeladat.netlify.app/"
    },
{
      cim: "GA",
      leiras: "Egy egyszserű weboldal.",
      url: "https://dxdrogon.github.io/GAFrontend/"
    },
{
      cim: "Térkép",
      leiras: "Egy kattintható térkép amin országokat lehet megtalálni.",
      url: "https://dxdrogon.github.io/Map/"
    }

  ];
</script>

<main>
  <section class="bemutatkozas">
    <h1>Üdvözöllek a portfóliómon!</h1>
    <p>Ezen a portfólión lehet megtekinteni elkészült projekteimet</p>
  </section>

  <section>
    <h2>Készségeim</h2>
    <div class="keszseg-grid">
      <div class="kartya nagy-kartya">
        <h3>Programozás</h3>
        <p>C#, JavaScript, HTML, CSS</p>
      </div>
      <div class="kartya nagy-kartya">
        <h3>Adatbázis</h3>
        <p>MySQL, SQLite</p>
      </div>
    </div>
  </section>

  <section>
    <h2>Projektek</h2>
    <div class="projekt-grid">
      {#each projektek as projekt}
        <div class="kartya">
          <h3>{projekt.cim}</h3>
          <p>{projekt.leiras}</p>
          <button on:click={() => window.open(projekt.url, '_blank')}>Megnyitás</button>
        </div>
      {/each}
    </div>
  </section>
</main>

<footer>
  <p>Elérhetőség: <a href="mailto:pelda@email.hu">szelpaldominik01@gmail.com</a></p>
  <p>&copy; 2025 Minden jog fenntartva.</p>
</footer>

<style>
  main {
    padding: 2rem;
    font-family: Arial, sans-serif;
    max-width: 1000px;
    margin: 0 auto;
    background-color: #f0f2f5;
    color: #000000;
  }

  section {
    margin-bottom: 3rem;
  }

  .bemutatkozas {
    background: linear-gradient(135deg, #dfffe2, #b3f2c9);
    padding: 2rem;
    border-radius: 16px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.15);
    transform: translateY(-10px);
    color: #000000;
  }

  .projekt-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
}

  .keszseg-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 1rem;
  }

  .kartya {
    background: #f5f5f5;
    padding: 1rem;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    display: flex;
    flex-direction: column;
    /*justify-content: space-between;*/
    color: #000000;
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  .kartya:hover {
    transform: translateY(-5px);
    box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2);
  }

  .nagy-kartya {
    min-height: 150px;
  }

  .kartya h3 {
    margin-top: 0;
  }

  .kartya ul {
    padding-left: 1.2rem;
    margin: 0;
  }

  .kartya li {
    margin-bottom: 0.4rem;
  }

  .kartya button {
    margin-top: auto;
    padding: 0.5rem;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }

  .kartya button:hover {
    background-color: #0056b3;
  }

  footer {
    text-align: center;
    padding: 2rem;
    background-color: #292828;
    color: #ffffff;
    font-size: 0.9rem;
    border-top: 1px solid #ccc;
  }

  footer a {
    color: #007bff;
    text-decoration: none;
  }

  footer a:hover {
    text-decoration: underline;
  }
</style>
