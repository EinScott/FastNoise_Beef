# FastNoise Lite for Beef

A port of the [FastNoise Lite](https://github.com/Auburn/FastNoise) noise generation library for the [Beef](https://github.com/beefytech/Beef) programming language.

## Features
- 2D & 3D
- OpenSimplex2 Noise
- OpenSimplex2S Noise
- Cellular (Voronoi) Noise
- Perlin Noise
- Value Noise
- Value Cubic Noise
- OpenSimplex2-based Domain Warp
- Basic Grid Gradient Domain Warp
- Multiple fractal options for all of the above
- Supports floats and/or doubles

## Getting started

Here's an example for creating a 128x128 array of OpenSimplex2 noise

```
// Create and configure FastNoise object
let noise = scope FastNoiseLite();
noise.SetNoiseType(.OpenSimplex2);

// Gather noise data
float[] noiseData = new float[128 * 128];
int index = 0;

for (int y = 0; y < 128; y++)
{
    for (int x = 0; x < 128; x++)
    {
        noiseData[index++] = noise.GetNoise(x, y);
    }
}

// Do something with this data...

delete noiseData;
```

## Documentation
See the original [README](https://github.com/Auburn/FastNoise/blob/master/README.md) and [Wiki](https://github.com/Auburn/FastNoise/wiki) for more info on how to use it (note that the wiki is written for c++).
