# TCP�� �̿��� ��Ű���
### ������ �ۼ��� ����
> TCP�� �̿��� ������ ����� �� �� �ܼ��� TCP ��Ŷ���� ĸ��ȭ�ؼ� ����ϴ� ���� �ƴ� ���̷ε带 ������ ��Ŷ�� �ְ� ���� ���� ������ ��Ģ
1. ���� �ʿ��� �� ���� ���� SEQ��ȣ�� ACK��ȣ�� �״�δ�.
2. �޴� �ʿ��� SEQ��ȣ�� ���� ACK��ȣ�� �ȴ�.
3. �޴� �ʿ��� ACK��ȣ�� ���� SEQ��ȣ + �������� ũ��
![Alt text](image-9.png)

# TCP �������̵�
![TCP ���� ���� ��ȭ](image-10.png)
**Listen** : ��Ʈ ��ȣ�� ������� �ִ� ����(��Ʈ ��ȣ ��� ���� ����)\
**Established** : ���� ������ ������ ���� 

���� : LISTENING -> SYN_RECEIVED -> ESTABLISHED

ex)
3 way-handshake �� �� Ŭ���̾�Ʈ�� ��û

Sequence number : 527792041\
Acknowledgment number : 953507065\
966 GET = Ethernet + IPv4 + TCP + Data\
Data = 966 - (14 + 20 + 20) = 912

Ŭ���̾�Ʈ�� ��û���� ������ Ŭ���̾�Ʈ���� �ٽ� ������.

Sequence number : 953507065\
Acknowledgment number : 527792953\
DATA