# rag-agent-gitops
## 一、常见问题汇总
1.网络问题
  因为docker对内地限制我们采用containerd作为容器运行时，但许多国内镜像源仓库里多是docker的镜像，而且为了实现CI/CD，需要持续访问github，故我们选择使用代理。这里我们用的是奈云的订阅链接和FClash，使用奈云是因为它的下载速度很快，而FClash是为了方便修改奈云的配置文件（存在一个比较麻烦的问题，会严重影响后续ArgoCD的同步和容器内部镜像拉取工作），配置如下：
  <img width="1113" height="923" alt="image" src="https://github.com/user-attachments/assets/97d2adf1-f671-454c-a380-8d97cdf41b8a" />
<img width="729" height="810" alt="image" src="https://github.com/user-attachments/assets/c0893a62-bf65-4289-9444-37b7ddfe88c2" />
<img width="712" height="202" alt="image" src="https://github.com/user-attachments/assets/9e128f42-35e9-404f-92aa-983cca7bdbc0" />
<img width="624" height="695" alt="image" src="https://github.com/user-attachments/assets/19743732-bb07-4b70-8b47-19bb5b8bdcb2" />
<img width="711" height="799" alt="image" src="https://github.com/user-attachments/assets/f86dc7a6-c2d2-4cf8-a3da-5b011e6fde78" />
  然后点击编辑，修改奈云的配置文件，如下：
<img width="1073" height="800" alt="image" src="https://github.com/user-attachments/assets/353bf8f9-2658-44bf-beb9-4b34be0f3880" />
<img width="642" height="473" alt="image" src="https://github.com/user-attachments/assets/f3004313-0303-48c0-87c4-4dcbcef4f9f2" />
<img width="915" height="653" alt="image" src="https://github.com/user-attachments/assets/1cfec91d-18fa-4582-8a28-821ee6a5ac7c" />
