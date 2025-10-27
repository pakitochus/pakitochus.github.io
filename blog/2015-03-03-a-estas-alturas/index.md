---
title: "A estas alturas"
date: "2015-03-03"
categories: 
  - "chusynth"
  - "tecnologia"
tags: 
  - "api-es"
  - "c-es"
  - "ctypes-es"
  - "fluidsynth-es"
  - "pyfluidsynth-es"
  - "python-es"
---

Y cuando ya pensaba que tenía el [fork](https://fjesusmartinez.wordpress.com/2015/02/21/entre-apis-y-ces/ "Entre APIs y Ces…") de pyFluidSynth casi terminado, me doy cuenta de que todavía me falta lo más importante: añadir el driver midi. Sin embargo, conforme uno va implementando cosas se da cuenta de que cada vez es más complicado añadir funcionalidad desde python a una API en C.

En esta ocasión, utilizando las funciones de la API, logro crear un driver MIDI al que conectar luego un teclado. Pero en cuando mando la primera nota, me manda un bonito `SYSSEG: reading NULL VMA` que hará las delicias de todos. ¿Por qué tengo un puntero nulo? Creía que `ctypes` se encargaría de todo.

Este es el código que manejo ahora mismo:

```python
def start_midi(self, mididriver='alsa_seq'): 
  """ Starts the MIDI driver to allow the MIDI keyboard interaction.
   :param mididriver: name of the midi driver, that can be one of these: 'alsa_raw', 'alsa_seq', 'coremidi', 'jack', 'midishare', 'oss', 'winmidi'
    :return:
     """
      if mididriver is not None: 
        assert (mididriver in ['alsa_raw', 'alsa_seq', 'coremidi', 'jack', 'midishare', 'oss', 'winmidi']) 
        fluid_settings_setstr(self.settings, 'midi.driver', mididriver) # Optionally: sets the real time priority to 99. 
        fluid_settings_setnum(self.settings, 'midi.realtimeprio', 99) 
        self.midi_driver = new_fluid_midi_driver(self.settings, fluid_midi_router_handle_midi_event, new_fluid_midi_event) 
        return self.midi_driver
```

No tengo ni idea de como voy a salir del paso, porque en principio parece que la función `fluid_midi_router_handle_midi_event` debería pasar todos los comandos de entrada al sintetizador, pero en lugar de ello, da fallo de segmentación. No sé si es por el `midi.realtimeprio` (que siempre da un warning), o por la función en sí, o por el recientemente añadido `new_fluid_midi_event`, pero la verdad es que estoy bastante estancado. A ver si esta tarde salimos del paso.
