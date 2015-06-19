# EventBus / Otto

跨 Activity, View, Thread 等溝通問題。

1. 通常遇到這種問題，一種是建立溝通管道，例如傳遞 callback 的方式。
2. 利用廣播方式，intent broadcast
3. 懶得傳遞 callback 就依靠全域變數註冊 callback.

EventBus 就是走第三種方案。

接著是儲存問題, 可回復性. 如果透過 saveInstanceState 就可以交由系統負責儲存。一種是儲存在 disk 如: sharedPreferences. 再來是 DB 。

# See Also

有 memory leak 的問題:

* [#57 Weak reference to the subscriber](https://github.com/greenrobot/EventBus/issues/57), 解法: [yongjhih/EventBus/commit/3d3c1ca6](https://github.com/yongjhih/EventBus/commit/3d3c1ca6676112bd9dd6bb78245b03b31e5c25fc)