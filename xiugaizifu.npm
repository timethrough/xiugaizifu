def format_credentials(original_str):
    # 使用split方法分割字符串，获取邮箱和密码部分
    parts = original_str.split(':')
    email = parts[2]  # 获取邮箱部分
    password = parts[3]  # 获取密码部分

    # 拼接新格式的字符串
    formatted_str = f"{email}----{password}"
    return formatted_str

# 提示用户输入多行数据，使用EOF（如Unix/Linux下的CTRL+D，Windows下的CTRL+Z后回车）来结束输入
print("请输入多行数据（格式为login:password:邮箱:密码），输入完成后使用EOF结束输入（如Unix/Linux下的CTRL+D，Windows下的CTRL+Z后回车）：")

# 读取多行输入直到EOF
input_lines = []
try:
    while True:
        line = input()
        input_lines.append(line)
except EOFError:
    pass  # 遇到EOF时结束输入

# 指定文件的保存路径，这里需要您根据自己的需求进行修改
# 例如，保存到桌面路径可以是 'C:\\Users\\您的用户名\\Desktop\\processed_credentials.txt'
file_path = 'F:\web3\\processed_credentials.txt'  # 请替换 '您的目标文件夹路径' 为实际路径

# 打开指定路径的文件用于写入
with open(file_path, 'w') as file:
    # 对每一行数据应用格式化逻辑并写入文件
    for line in input_lines:
        formatted_str = format_credentials(line)
        file.write(formatted_str + '\n')  # 写入文件

print(f"处理完成，格式化后的数据已保存到 '{file_path}'。")
