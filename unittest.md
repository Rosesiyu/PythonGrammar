一、一些基本概念：

TestCase（测试用例）: 所有测试用例的基类，它是软件 测试中最基本的组成单元。

                   一个test case就是一个测试用例，是一个完整的测试流程，包括测试前环境的搭建setUp，执行测试代码(run)，以及测试后环境的还原(tearDown)。测试用例是一个完整的测试单元，可以对某一问题进行验证。

TestSuite（测试套件）:多个测试用例test case集合就是TestSuite，TestSuite可以嵌套TestSuite

TestLoader：是用来加载 TestCase到TestSuite中，其中有几个loadTestsFrom_()方法，就是从各个地方寻找TestCase，创建他们的实例，然后add到TestSuite中，再返回一个TestSuite实例

TextTestRunner：是来执行测试用例的，其中的run（test）会执行TestSuite/TestCase中的run(result)方法。

TextTestResult：测试结果会保存到TextTestResult实例中，包括运行了多少用例，成功与失败多少等信息

TestFixture:又叫测试脚手，测试代码的运行环境，指测试准备前和执行后要做的工作，包括setUp和tearDown方法
