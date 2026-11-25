#TeacherSelection 

## Deadlock 四要素

Deadlock 的行程必須同時符合以下四個要素，只要其中一項不成立，就可以避免 deadlock 產生

- 禁止搶占（no preemption）：系統資源不能被強制從Thread退出。
- 持有和等待（hold and wait）：Thread可以在等待時持有系統資源。
- 互斥（mutual exclusion）：資源只能同時分配給一個Thread，無法多個行程共享。
- 循環等待（circular waiting）：Thread互相持有其他Thread所需要的資源，並且等待已被占用的資源。