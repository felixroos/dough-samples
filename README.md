# dough-samples

default samples for superdough / strudel.

## Usage

To get the default set of strudel samples, use this:

```js
async function loadSamples() {
  const ds = "https://raw.githubusercontent.com/felixroos/dough-samples/main/";
  return Promise.all([
    samples(`${ds}/tidal-drum-machines.json`),
    samples(`${ds}/piano.json`),
    samples(`${ds}/Dirt-Samples.json`),
    samples(`${ds}/EmuSP12.json`),
    samples(`${ds}/vcsl.json`),
  ]);
}
```

## piano

<https://archive.org/details/SalamanderGrandPianoV3>

License: CC-by <http://creativecommons.org/licenses/by/3.0/> Author: Alexander Holm

## VCSL

<https://github.com/sgossner/VCSL>

License: Creative Commons 0

## Dirt-Samples

Note: the Dirt-Samples.json file here only uses a very small subset of the dirt samples

<https://github.com/tidalcycles/Dirt-Samples/>

## tidal-drum-machines

<https://github.com/ritchse/tidal-drum-machines>

## Other Sample Repos

```plaintext
await samples('github:yaxu/clean-breaks/main');
await samples('github:yaxu/spicule/master');
await samples('github:felixroos/estuary-samples/main');
await samples('github:felixroos/samples/main');
await samples('github:emptyflash/samples/main');
await samples('github:Bubobubobubobubo/Dough-Fox/main');
await samples('github:Bubobubobubobubo/Dough-Amen/main');
await samples('github:Bubobubobubobubo/Dough-Amiga/main');
await samples('github:Bubobubobubobubo/Dough-Waveforms/main');
await samples('github:Bubobubobubobubo/Dough-Samples/main');
```
