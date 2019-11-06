# 设置registry

### 1.  临时使用

   ```shell
   npm --registry https://registry.npm.taobao.org install express
   ```

   

### 2. 持久使用

   ```shell
   npm config set registry https://registry.npm.taobao.org
   ```

   - 配置后可通过一下方式来验证是否成功

   - ```shell
     npm config get registry 
     ```

   - ```shell
     npm info express
     ```

### 3. 通过cnpm使用

   ```shell
   npm install -global cnpm --registry=https://registry.npm.taobao.org
   ```

   