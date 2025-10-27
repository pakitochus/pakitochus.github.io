---
title: "Tocando mis primeras notas"
date: "2015-03-04"
categories: 
  - "musica"
  - "tecnologia"
tags: 
  - "fluidsynth-es"
  - "pyfluidsynth-es"
---

Por primera vez, he logrado lanzar `fluidsynth` desde una terminal python, crear su correspondiente driver MIDI y tocar algunas notas con el teclado en directo. A partir de aquí, es todo mejorar.

{{< video https://www.youtube.com/watch?v=2ZC4UAiKpMU >}}

El problema que estaba teniendo era con la función `new_fluid_midi_driver(settings, handler, event_handler_data)`, en el que en la [documentación](http://fluidsynth.sourceforge.net/api/midi_8h.html#ad0971af69fb51398d468b151cba70bee) aparece como que hay que llamarlo (en C) de esta forma:

```C
fluid_settings_t* settings; fluid_midi_driver_t* mdriver; settings = new_fluid_settings(); mdriver = new_fluid_midi_driver(settings, handle_midi_event, NULL);
```

sugiriendo el uso de `fluid_midi_router_handle_midi_event()` como handler callback. Finalmente, la mejor opción para mi fue:

```C
mdriver = new_fluid_midi_driver(settings, fluid_synth_handle_midi_event, synth)
```

O sea, que había que la función `fluid_synth_handle_midi_event` es la pancea y en ningún sitio de la documentación de API te la especifican. Bien por fluidsynth. Y usar el propio objeto sintetizador `synth` como `event_handler_data`.
