---
Domain: AI
Type: Concept
folder_ready: 1
---
### Idea
**Bloques de construcción fundamentales en la arquitectura de agentes modernos**
### Concept 
Para que una skill sea accionable por un agente a traves de los diferentes frameworks, debe constar de tres partes:

**Schema:** Nombre de la Skill, Descripción, Argumentos de Entrada 
**Lógica de Ejecución:** El codigo a ejecutar cuando se ejecuta una skill puede ser: Llamada API , Consulta a BDD, Script del sistema 
**Canal de Retorno:** El resultado estructurado que devuelve la skill, el modelo toma el output y lo reinyecta a su contexto, para dar una respuesta final
### Principios de diseño 
Considera estos principios para el diseño de tus skills:
- **Modularidad y Aislamiento:** Un skill debe hacer una cosa, preferible tener dos skills atómicas
- **Seguridad y Control de Accesos:** Las skills deben implementar validación estricta de inputs, para correr los menores riesgos
- **[[Idempotencia]]**

## 📂 Subthemes 

<!-- FOLDER_LINKS_START -->
- 📄 [[02-Resources/Prompts/Skills/Agents.md.md|Agents.md]]
- 📄 [[02-Resources/Prompts/Skills/low-token.md|low-token]]
- 📄 [[02-Resources/Prompts/Skills/planner.md|planner]]
- 📄 [[02-Resources/Prompts/Skills/README.md|README]]
- 📁 [[02-Resources/Prompts/Skills/Skills-Documentation/Skills-Documentation|Skills-Documentation]]
<!-- FOLDER_LINKS_END -->

```dataviewjs  
const START = "<!-- FOLDER_LINKS_START -->";
const END = "<!-- FOLDER_LINKS_END -->";

const activeFile = app.workspace.getActiveFile();
if (!activeFile) return;

const current = dv.current();

// 🔹 Gate: no ejecutar hasta que Templater marque listo
if (!current.folder_ready) {
  dv.paragraph("Waiting for template...");
  return;
}

const folderPath = activeFile.parent.path;
const folder = app.vault.getAbstractFileByPath(folderPath);

let items = folder.children
  .filter(f => f.path !== activeFile.path)
  .sort((a, b) => a.name.localeCompare(b.name));

const generated = items
  .map(f => {
    if (f.children) {
      return `- 📁 [[${f.path}/${f.name}|${f.name}]]`;
    } else {
      return `- 📄 [[${f.path}|${f.basename}]]`;
    }
  })
  .join("\n");

let content = await app.vault.read(activeFile);

const escape = s => s.replace(/[.*+?^${}()|[\]\\]/g, "\\$&");
const pattern = new RegExp(
  escape(START) + "[\\s\\S]*?" + escape(END)
);

const replacement = `${START}\n${generated}\n${END}`;

// 🔹 Idempotencia
if (content.includes(replacement)) {
  dv.paragraph("Already synced.");
  return;
}

if (content.includes(START) && content.includes(END)) {
  content = content.replace(pattern, replacement);
} else {
  content += `\n\n${replacement}\n`;
}

await app.vault.modify(activeFile, content);

dv.paragraph("Folder structure synced.");
```
### State:
#Note 
