Парсер JSON файлов, не включающих в себя массивы значений.

Перед сборкой с CMake нужно собрать antlr4-runtime, заменить пути к файлам заголовков и статической библиотеке antlr4-runtime в CMakeLists.txt
После сборки нужно добавить antlr4-runtime.dll в папку bin проекта C# и прописать путь к antlr4-runtime.lib в свойствах проекта StatLibJson
