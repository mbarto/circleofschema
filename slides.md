---
theme: seriph

title: Promemoria - Archivio.com

class: text-center
drawings:
  persist: false
transition: slide-left
mdc: true
---

# Promemoria - Archivio.com

Some technical choices

---
layout: center
---

# JSON (smart) editor

<div class="flex flex-col items-center">

 * [json-editor](https://github.com/json-editor/json-editor?tab=readme-ov-file)
   * [example](https://json-editor.github.io/json-editor/form-submission.html)
 * [json-edit-react](https://carlosnz.github.io/json-edit-react/)
 * [monaco-editor](https://www.npmjs.com/package/@monaco-editor/react)
   * [example](https://microsoft.github.io/monaco-editor/playground.html?source=v0.52.2#example-creating-the-editor-hello-world)

</div>
---
layout: center
---

# JSON validation

<div class="flex flex-col items-center">

 * [Ajv](https://ajv.js.org/) + [json-schema-to-ts](https://github.com/ThomasAribart/json-schema-to-ts)
 * [Zod](https://zod.dev/) + [zod-to-json-schema](https://github.com/StefanTerdell/zod-to-json-schema)
 * [Valibot](https://valibot.dev/) + [@valibot/to-json-schema](https://github.com/fabian-hiller/valibot/tree/main/packages/to-json-schema)
 * [Typebox](https://github.com/sinclairzx81/typebox)
 * [Effect Schema](https://effect.website/docs/schema/introduction/)

</div>
---
layout: center
---

<div class="flex flex-col items-center">

# The Circle of Schema(s)

<Excalidraw
  drawFilePath="https://backend.excalidraw.com/api/scene/6f9OLpO77b6/1zSMv3UX8jB/contents"
  class="w-[600px] ml-30"
  frame="Frame1"
  :darkMode="false"
  :background="false"
/>

</div>
---
layout: center
---
<div class="flex flex-col items-center">

# A different Schema for a different purpose

<Excalidraw
  drawFilePath="https://backend.excalidraw.com/api/scene/6f9OLpO77b6/1zSMv3UX8jB/contents"
  class="w-[500px]"
  frame="Frame2"
  :darkMode="false"
  :background="false"
/>

</div>
---
layout: center
---
<div class="flex flex-col items-center">

# Application Configuration

<Excalidraw
  drawFilePath="https://backend.excalidraw.com/api/scene/6f9OLpO77b6/1zSMv3UX8jB/contents"
  class="w-[700px]"
  frame="Frame3"
  :darkMode="false"
  :background="false"
/>

</div>

---
layout: full
---
<div class="flex flex-col items-center" style="--slidev-code-font-size: 12px; --slidev-code-line-height: 12px">

# Configuration Evolution

````md magic-move {lines: false}
```json
{
  version: "0.0.0",
  general: {
    colors: {
        primary: "#FF0000",
        light: "#00FF00",
        dark: "#0000FF",
    },
    languages: {
        it: true,
        en: false,
    },
    images: {
        logo: "",
    },
    titles: {
        title: "Archivio Digitale",
        subtitle: "Archivio Magazine",
    },
  }
}
```
```json
{
  version: "0.0.1",
  general: {
    colors: {
        primary: "#FF0000",
        light: "#00FF00",
        dark: "#0000FF",
    },
    languages: {
        it: true,
        en: false,
    },
    images: {
        logo: "",
    },
    titles: {
        title: "Archivio Digitale",
        subtitle: "Archivio Magazine",
    },
  },
  homepage: {
        modules: [],
  },
}
```
```json
{
  version: "0.0.3",
  general: {
    colors: {
        primary: "#FF0000",
        light: "#00FF00",
        dark: "#0000FF",
    },
    languages: {
        it: true,
        en: false,
    },
    images: {
        logo: "",
    },
    titles: {
        title: "Archivio Digitale",
        subtitle: "Archivio Magazine",
    },
  },
  homepage: {
        modules: [],
  },
  detail: {
        types: [],
  },
}
```
```json
{
  version: "0.0.4",
  general: {
    colors: {
        primary: "#FF0000",
        light: "#00FF00",
        dark: "#0000FF",
    },
    languages: {
        it: true,
        en: false,
    },
    images: {
        logo: {
            url: "",
            alt: "",
        },
    },
    titles: {
        title: "Archivio Digitale",
        subtitle: "Archivio Magazine",
    },
  },
  homepage: {
        modules: [],
  },
  detail: {
        types: [],
  },
}
```
```json
{
  version: "0.0.5",
  general: {
    ...
    languages: {
        it: true,
        en: false,
    },
    images: {
        logo: {
            url: "",
            alt: "",
        },
    },
    disclaimer: {
        it: {
            title: "",
            text: "",
            button: {
                variant: "primary",
                text: "",
            },
        },
    },
  },
  ...
  detail: {
        header: [],
        images: [],
        info: [],
  },
}
```
```json
{
  version: "0.0.6",
  general: {
    ...
    languages: {
        it: true,
        en: false,
    },
    images: {
        logo: {
            url: "",
            alt: "",
        },
    },
    disclaimer: {
        it: {
            title: "",
            text: "",
            button: {
                variant: "primary",
                text: "",
            },
        },
    },
  },
  ...
  detail: [{
    type: "People",
    fields: {
      header: [],
      info: []
    }
  }],
}
```
```json
{
  version: "0.0.7",
  general: {
    ...
    languages: {
        it: true,
        en: false,
        fr: false,
    },
    images: {
        logo: {
            url: "",
            alt: "",
        },
    },
    disclaimer: {
        it: {
            title: "",
            text: "",
            button: {
                variant: "primary",
                text: "",
            },
        },
    },
  },
  ...
  detail: [{
    type: "People",
    fields: {
      header: [],
      info: []
    }
  }],
}
```
````

</div>
