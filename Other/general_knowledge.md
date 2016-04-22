> ####Program Errors
- trapped errors。导致程序终止执行，如除0，Java中数组越界访问
- untrapped errors。 出错后继续执行，但可能出现任意行为。如C里的缓冲区溢出、Jump到错误地址

> ####Forbidden Behaviours
- 语言设计时，可以定义一组forbidden behaviors. 它必须包括所有untrapped errors, 但可能包含trapped errors.

> ####Well behaved、ill behaved
- well behaved: 如果程序执行不可能出现forbidden behaviors, 则为well behaved。
- ill behaved: 否则为ill behaved...

> ####强、弱类型
- 强类型strongly typed: 如果一种语言的所有程序都是well behaved——即不可能出现forbidden behaviors，则该语言为strongly typed。
- 弱类型weakly typed: 否则为weakly typed。比如C语言的缓冲区溢出，属于trapped errors，即属于forbidden behaviors..故C是弱类型
-前面的人也说了，弱类型语言，类型检查更不严格，如偏向于容忍隐式类型转换。譬如说C语言的int可以变成double。 这样的结果是：容易产生forbidden behaviours，所以是弱类型的

> ####动态、静态类型
- 静态类型 statically: 如果在编译时拒绝ill behaved程序，则是statically typed;
- 动态类型dynamiclly: 如果在运行时拒绝ill behaviors, 则是dynamiclly typed。
