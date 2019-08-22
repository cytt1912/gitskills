import random
class BaseMessage(object):

    def __init__(self):
        self.payload = {

        }

    # 定义随机生成ordnum函数
    def get_order(self,length = 15):
        char = '0123456789'
        order = ''
        for i in range(length):
            index = random.randint(0,len(char)) - 1
            order += char[index]
        # print(order)
        return order

    # 定义更新payload函数
    def update_payload(self,key,value):
        #payload为字典，更新直接更新字段即可
        self.payload[key] = value
        return self.payload


if __name__ == '__main__':
    payload = {
        "qwe": "wer",
        "charset": "utf-8",
        "ertt": "123"
    }
    b2 = BaseMessage()
    print(payload)
    b2.get_order()
