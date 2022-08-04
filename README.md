# UnityRhythmGame2
유니티엔진 리듬게임2

* OST</br>
Smilegate RPG</br>
</br>
* 2.0 변경점</br>
에디터 추가</br>
롱노트 추가</br>

<hr>
* 노트 생성 방식에 대해</br>
</br>
게임</br>
유니티 자체 ObjectPool을 활용하여 노트를 해당 시점에 필요한만큼 생성/해제.</br>
생성은 마디단위로 이루어지고, 해제는 노트가 화면 밖으로 이탈(노트의 y좌표가 0보다 작으면)하면 해제.</br>
노트는 자신의 위치를 실시간으로 보정하기위해 노력(?)함.</br>
</br>
에디터</br>
게임에서 사용하던 ObjectPool 시스템을 그대로 활용하나, 실행 시 노트를 한번에 전부 생성.</br>
노트를 배치하면, ObjectPool이 현재 사용하지 않는 오브젝트를 재활용(ObjectPool.Get())하거나 새로 생성.</br>
노트를 삭제하면, 해당 오브젝트를 바로 회수하지는 않고 비활성화(gameObject.SetActive(false)).</br>
</br>
작성중..
