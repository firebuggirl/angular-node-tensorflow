# Update Angular 7-21-2020

`ngupdate @angular/cli @angular/core --allow-dirty --force`

`npm audit fix`

`ng serve` or `npm start`

- Error!!

```yaml
node_modules/@types/webgl2/index.d.ts:582:13 - error TS2403: Subsequent variable declarations must have the same type.  Variable 'WebGL2RenderingContext' must be of type '{ new (): WebGL2RenderingContext; prototype: WebGL2RenderingContext; readonly ACTIVE_ATTRIBUTES: number; readonly ACTIVE_TEXTURE: number; readonly ACTIVE_UNIFORMS: number; readonly ALIASED_LINE_WIDTH_RANGE: number; ... 554 more ...; readonly WAIT_FAILED: number; }', but here has type '{ new (): WebGL2RenderingContext; prototype: WebGL2RenderingContext; readonly ACTIVE_ATTRIBUTES: number; readonly ACTIVE_TEXTURE: number; readonly ACTIVE_UNIFORMS: number; readonly ALIASED_LINE_WIDTH_RANGE: number; ... 555 more ...; readonly MAX_CLIENT_WAIT_TIMEOUT_WEBGL: number; }'.

582 declare var WebGL2RenderingContext: {
                ~~~~~~~~~~~~~~~~~~~~~~

  node_modules/typescript/lib/lib.dom.d.ts:16450:13
    16450 declare var WebGL2RenderingContext: {
                      ~~~~~~~~~~~~~~~~~~~~~~
```

## Solution:

- https://dev.to/dkp1903/solving-typescript-tensorflowjs-incompat-issues-4f80


- issue w/ Tensorflow & Typescript:

`npm i --save @types/webgl2`
