�����Ҫ�����module��������m1��������������ҵ�m1.py���������ڵ�ǰĿ¼���ң�Ȼ�����ڻ�������PYTHONPATH�в��ҡ�Ȼ����python�İ�װ������ص�Ĭ��·����
> PYTHONPATH������Ϊϵͳ��PATH����һ��Ķ��������а������ɸ�Ŀ¼�����PYTHONPATHû���趨�������Ҳ���m1.py����������� ��python�İ�װ������ص�Ĭ��·������Unix�£�ͨ����/usr/local/lib/python��

����Ϊ����������˳�������ǰ·����PYTHONPATH�д������׼moduleͬ����module����Ḳ�Ǳ�׼module��Ҳ����˵�������ǰĿ¼�´���xml.py����ôִ ��import xmlʱ��������ǵ�ǰĿ¼�µ�module��������ϵͳ��׼��xml��

Python�е�package����ܼ򵥣����νṹ���������Ŀ¼�Ĳ�νṹ��ͬ����һ����Java���ƣ�Ψһ��ͬ�ĵط����ڣ�python�е�package�������һ��`__init__.py`���ļ���

���磬���ǿ���������֯һ��package:

```
package1/
    __init__.py
    subPack1/
        __init__.py
        module_11.py
        module_12.py
        module_13.py
    subPack2/
        __init__.py
        module_21.py
        module_22.py
    ����
```
`__init__.py`����Ϊ�գ�ֻҪ�����ڣ��ͱ�����Ŀ¼Ӧ����Ϊһ��package����

�ڶ���Ŀ¼��Ҳ����package1����package1���ڽ������ܹ��������ĵط�������python

```Python
>>>from package1.subPack1.module_11 import funcA
>>>funcA()
```
��ʱ��import����л����ͨ���*������ĳ��module�е�����Ԫ�أ��𰸾���__init__.py�С���subPack1��__init__.py�ļ���д

```Python
__all__ = ['module_13', 'module_12']
```
Ȼ�����python

```Python
>>>from package1.subPack1 import *
>>>module_11.funcA()
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
ImportError: No module named module_11
```
Ҳ����˵����*����ʱ��package�ڵ�module����`__init__.py`���Ƶġ�

����������������package�ڲ�������á����ϣ������ͬһ��package�е�module����ֱ��import���ɡ�Ҳ����˵��`module_12.py`�У�����ֱ��ʹ��`import module_11`

�������ͬһ��package�У���������ϣ����module_21.py�е���module_11.py�е�FuncA����Ӧ��������

```Python
from module_11����.module_11 import funcA
```

�Զ���ģ��������·����������Python��װĿ¼��Lib\site-packages�����*.pth�ļ�����ģ��·����ӵ��ļ��С�