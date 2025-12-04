# 一切皆对象的设计哲学
  相比与C++而言，Java不存在独立的全局函数，所有程序的入口也必须是类的静态函数。甚至连数据结构也是由类包装，比如数组等。
  但是出于性能考虑，如果我们在处理基本数据类型时，仍然在每次运算时都创建对象，显然是一种浪费。所以Java的八大基本数据类型：
  byte    b = 1;      // 8位
  short   s = 2;      // 16位
  int     i = 3;      // 32位
  long    l = 4L;     // 64位
  float   f = 5.0f;   // 32位
  double  d = 6.0;    // 64位
  char    c = 'A';    // 16位
  boolean flag = true; // 1位（但实际占用空间由JVM决定）并不是对象。
  隔壁python却更加过火，连这些也都成了对象，这也是java的运行速度更快一些的原因（相对python）。
  有趣的是，java还提供了许多集合类：
  ArrayList<String> list = new ArrayList<>();  // 对象
  HashMap<String, Integer> map = new HashMap<>();  // 对象
  LinkedList<Integer> linkedList = new LinkedList<>();  // 对象
  很明显，这些集合类也是数据结构，同样是为了处理基本数据类型，但是他们却只能处理对象，因此就需要将基本的数据类型进行包装（Wrapper），将他们变为类。
  这就是为什么在算法题中，常常时而int，时而Integer，当然，这些包装类也有自己的方法可以使用。

