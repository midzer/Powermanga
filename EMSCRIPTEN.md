# Emscripten

## Build

```
mkdir build
cd build
emcmake cmake ..
emmake make
```

## Link

```
emcc -flto -O3 -fno-rtti -fno-exceptions *.o -o index.html -sUSE_SDL=2 -sUSE_SDL_MIXER=2 -sSDL2_MIXER_FORMATS=ogg -sASYNCIFY -sASYNCIFY_IGNORE_INDIRECT -sASYNCIFY_ONLY=@../../../../funcs.txt -sENVIRONMENT=web --preload-file ../../../../data/@data/ --preload-file ../../../../graphics/@graphics/ --preload-file ../../../../sounds/@sounds/ --preload-file ../../../../texts/@texts/ -sINITIAL_MEMORY=128mb --closure 1 -sEXPORTED_RUNTIME_METHODS=['allocate']
```
