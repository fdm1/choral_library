<script lang="ts">
  import Database from "better-sqlite3";
  import fs from "node:fs";

  // list all files in the directory
  // const files = fs.readdirSync('./db/Database');
  // console.log({files: files})
  // console.log({fs.Dir})
  const db = new Database(fs.readFileSync("./db/DatabaseName.db"));
  const stmt = db.prepare("select * from foo");
  const names = stmt.all();
  // const names = ['foo', 'bar', 'baz'];
  console.log({ names });
</script>

{#each names as name}
  <p>Name: {name.name}</p>
{/each}
