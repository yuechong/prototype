# prototype

if(!object){
    var object = function(prototype){
        function F(){}

        F.prototype = prototype;

        return new F();
    };
}

function inherit(SubClass,SuperClass){

    var prototype = object(SuperClass.prototype);

    prototype.constructor = SubClass;

    SubClass.prototype = prototype;
}
