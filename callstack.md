[[Stack]]
- Callstack means that JS is a single-thread programming language, so it only does one thing at one time, therefore, it needs a way to keep track of the execution context, and that is the callstack.
```Javascript
  function f1(){
    console.log("This is f1");
    
    f2();
    
    function f2(){
      console.log("This is f2");
      f3();
      function f3(){
        console.log("This is f3");
      }
    }
    console.log("Done with running codes.");
  }
  f1();
```
- [Callstack Tool](http://latentflip.com/loupe/?code=ZnVuY3Rpb24gZjEoKSB7CiAgY29uc29sZS5sb2coJ1RoaXMgaXMgZjEnKQoKICBmMigpCgogIGZ1bmN0aW9uIGYyKCkgewogICAgY29uc29sZS5sb2coJ1RoaXMgaXMgZjInKQoKICAgIGYzKCkKCiAgICBmdW5jdGlvbiBmMygpIHsKICAgICAgY29uc29sZS5sb2coJ1RoaXMgaXMgZjMnKQoKICAgICAgY29uc29sZS5sb2coJ2YzIGRvbmUnKQogICAgfQoKICAgIGNvbnNvbGUubG9nKCdmMiBkb25lJykKICB9CgogIGNvbnNvbGUubG9nKCdmMSBkb25lJykKfQoKZjEoKQ%3D%3D!!!PGJ1dHRvbj5DbGljayBtZSE8L2J1dHRvbj4%3D)