# ROS 패키지에서 gdb 사용법

gdb는 많이 쓰는 cpp 디버거 중 하나이다.
ros에서 gdb를 사용하는 방법은 아래와 같다.

## 순서
1. Catkin workspace에서 디버그 모드로 빌드한다 </br>
```catkin_make -DCMAKE_BUILD_TYPE=Debug```

2. Launch 파일에서 원하는 노드(디버그 대상 노드)에 launch-prefix="xterm -e gdb --args"를 추가해준다. 아래는 예제이다.
```xml
<launch>
  <node name="some_node" pkg="some_pkg" type="some_node" launch-prefix="xterm -e gdb --args"/>
</launch>
```

3. Launch 파일 실행 후 xterm 창에서 run command로 실행

### 참고
[GDB 커맨드] (https://web.eecs.umich.edu/~sugih/pointers/summary.html) </br>
