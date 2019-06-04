# RosConnection
Rosjava中DefaultServiceClient 判断 isConnected出现空指针问题修复
改问题会导致service 不能正常调用 还无法 重连
 public boolean isConnected() {
        if (null != this.tcpClient && null != this.tcpClient.getChannel()) {
            return this.tcpClient.getChannel().isConnected();
        } else {
            return false;
        }
    }
