# مفهوم null safety مع Function 

**مفهوم null safety مع Function** 

لو اردنا انشاء Function تستقبل Parameters  ثم بعد استدعائه اردنا اعطاء احد Parameter قيمة null سوف يظهر لنا خطاء لان Parameter هو عباره عن متغير من نوع Non-nullable لا يقبل قيمة null 



    void main() {
    msgPrint("fahad",null);
    }
    
    msgPrint(String name, int age){
      print("my name is : ${name}, amd ,y age is: ${age}");
    }

سوف تظهر لنا رساله 

    The value 'null' can't be assigned to the parameter type 'int' because 'int' is not nullable.
    msgPrint("fahad",null);

تشير ان Argument الذي يشير الى Parameter باسم age لا يقبل قيمة null فيجب جعل المتغير من نوع nullable باضافة علامة. (؟) عند النوع الخاص في Parameter  كما هو في المثال في الاسفل


    void main() {
    msgPrint("fahad",null);
    }
    
    msgPrint(String name, int? age){
      print("my name is : ${name}, amd ,y age is: ${age}");
    }

المخرج 

    my name is : fahad, amd ,y age is: null

الان يمكن اعطاء age قيمة nullبدون حدوث اخطاء وايضا يمكن جعل الاسم عباره عن nullable يقبل قيمة null باضافة علامة علامة. (؟) على name

