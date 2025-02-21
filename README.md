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
    samples(`${ds}/mridangam.json`),
  ]);
}
```

## piano

<https://archive.org/details/SalamanderGrandPianoV3>

License: CC-by <http://creativecommons.org/licenses/by/3.0/> Author: Alexander Holm

## VCSL

<https://github.com/sgossner/VCSL>

License: Creative Commons 0

## mrid

Mridingam samples

License: CC-by-sa: <https://creativecommons.org/licenses/by-sa/4.0/> (c) Arthur Carabott 2022, Performer: Harishankar V Menon

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

## going offline

follow these commands to get your machine ready to use dough-samples offline:

```sh
git clone --recurse-submodules https://github.com/felixroos/dough-samples.git
cd dough-samples
# make sure you have node.js (>=v20)
npx serve -p 6543 --cors # serve dough-samples at http://localhost:6543
```

load samples:

```txt
const base = 'http://localhost:6543';
await Promise.all([
  samples(
    base + '/tidal-drum-machines.json',
    base + '/tidal-drum-machines/machines/'
  ),
  samples(base+'/piano.json', base+'/piano/'),
  samples(base+'/Dirt-Samples.json', base+'/Dirt-Samples/'),
  samples(base+'/EmuSP12.json', base+'/tidal-drum-machines/machines/'),
  samples(base+'/vcsl.json', base+'/VCSL/'),
  samples(base+'/mridangam.json', base+'/mrid/'),
]);
```

if you want to add another repo to your offline samples, run:

```sh
git submodule add github:user/repo/main
```

then add this line to your sample setup:

```js
samples(base+'/repo/strudel.json', base+'/repo/')
```
