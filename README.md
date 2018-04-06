# JS_SingletonClass
Javascript Singleton Class Example

        var Test = (function(){
          var instance = null;

          function Test()
          {
            this.a = 0;
          }
          Test.prototype.constructor = Test;
          Test.prototype = Object.create(Object.prototype);

          return {
            getInstance: function()
            {
              if(instance == null)
                instance = new Test();
              return instance;
            }
          }
        })();
