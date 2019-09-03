### pinpoint
---
https://github.com/naver/pinpoint

```java
// rpc/test/java/com/navercorp/pinpoint/rpc/message/SendPackageTest.java

public class SendPacketTest {
  @Test
  public void testToBuffer() throws Exception {
    byte[] bytes = new byte[10];
    SendPacket packetSend = new SendPacket(bytes);
    
    ChannelBuffer channelBuffer = packetSend.toBuffer();
    
    short packetType = channelBuffer.readShort();
    SendPacket packet = (SendPacket) SendPacket.readBuffer(packetType, channelBuffer);
    Assert.assertArrayEquals(bytes, packet.getPayload());
  }
}
```

```
```

```
```


