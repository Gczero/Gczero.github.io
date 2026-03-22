SLA:service-level agreement服务可用等级，高可用better

算法：效率（并行），可用性

leslie lamport

执行环境？多机环境，计算单元-》process

沟通！communication abstraction

对于每个计算单元，动作：1.send event。往输出缓存里存放message
2. receive event 往输入缓存拿essage 
3. computation event

i->j:outbufi[j],inbufj[i]

分布式算法的确定性不成立，执行结果不一样，时间顺序，执行速度等影响结果

global configuration，global state

request（交付） indication（确认）（异步过程，同步等待）

事件驱动方式实现分布式算法，只有当请求发生时，才会激活接下来的事件不进行处理（不做无意义事件）

错误：节点机器出现问题->但是尽量说整体提供完整服务。一般错误：crash（在过程中间停止）（计算单元 运行/停下）

link failure：结果丢失，保证通信交互有意义

消息不会无中生有

STUBBORN LINKS

计时器，timeout时对所有消息激活模块，再发一次之前发过的所有消息（通过fair-loss links fll来发）

perfect links：完美可靠的links，发送一定送达，无重复发送，类似tcp

***

多项式时间可解决：P
多项式时间可验证所给的答案正确：NP
P肯定属于NP

NPC（NP-complete）->NP+NP-hard

NP-hard可以不是NP问题，但是是至少比NP问题中最难的问题一样或者更难的问题

若所有NPC问题都找到多项式时间解，则所有NP问题都可解决，即NP=P

判定问题难->对应优化问题难

reduction（归约）转换为另一个形态的问题（A->B已知难推出可能难，证明B也是NP难）
***

mit6.006

