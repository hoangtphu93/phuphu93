# phuphu93

https://github.com/hoangtphu93
Add the button to every tweet. Put this code to the activate:

const { button } = this.adapter.exports;
this.adapter.attachConfig({
  POST: (ctx: any) =>
    button({
      DEFAULT: {
        img: EXAMPLE_IMG,
        tooltip: 'Parse Tweet',
        exec: () => {
          console.log('parsedCtx:', ctx);
        },
      },
    }),
});
