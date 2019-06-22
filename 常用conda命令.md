# 管理包

- ### 安装包：conda install package_name

  - 同时安装多个包：conda install numpy scipy pandas
  
  - 指定版本号：conda install python=3.6
  
- ### 卸载包：conda remove package_name

- ### 更新包：conda update package_name

  - 更新环境中的所有包：conda update --all
  
- ### 搜索包：conda search search_term(当不知道包的确切名字时使用）

- ### 列出所有安装的包：conda list   
--------
# 管理环境

- ### 创建环境：conda create -n 'env_name' 'list of packages'

  - 例如：conda create -n pytorch python=3.5
  
- ### 进入和离开环境：

  - Linux系统：source activate/deactivate 'env_name'
  
  - Windows系统：activate/deactivate 'env_name'
  
- ### 删除环境：conda env remove -n 'env_name'

- ### 查看环境：conda env list
----------
# 保存和加载环境

共享环境可以让其他人安装你的代码中使用的所有包，并确保这些包版本的正确。

- 首先进入要保存的环境，然后使用conda env export > 'env_name'.yaml 将环境保存为yaml格式；

- 创建环境使用 conda env create -f 'env_name'.yaml 该命令会创建一个新环境，里面具有一样的库。
