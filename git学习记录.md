1、首先ubuntu本地下载git工具->sudo apt-get install git
2、添加信息 git config --global user.name "xxx"
			git config --global user.email "你的邮箱地址"
3、生成密钥：
		ssh-keygen -C 'you email address@gmail.com' -t rsa
		在.ssh文件夹里有公钥和私钥   公钥需要加入到 github 上
4、在github上新建仓库：
	clone到本地 ： git clone  <address>
				git init 
				git add .
				git commit -m "<hello>"
				<git branch <name> 新建一个分支  git chechout <name>在分支上修改  add commit>
				git chechout master 
				git merge <name>  主分支合并分支
				
	本地上传到仓库：
				git init
				git add .
				git commit -m <commit>
				git remote add origin https://git.oschina.net/你的用户名/项目名.git <绑定远端仓库>
				git push -u origin master  ※：此时因为缺少远端仓库的文件 会push失败
				git pull --rebase origin master  <获取文件再执行push>