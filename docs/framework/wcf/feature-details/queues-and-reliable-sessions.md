---
title: 队列和可靠会话
ms.date: 03/30/2017
ms.assetid: 7e794d03-141c-45ed-b6b1-6c0e104c1464
ms.openlocfilehash: 2f79e1eac469dc1d9d775cbca0f06046f10dfb20
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/23/2019
ms.locfileid: "54642904"
---
# <a name="queues-and-reliable-sessions"></a>队列和可靠会话
队列和可靠会话是实现可靠消息传递的 Windows Communication Foundation (WCF) 功能。 在本部分中包含的主题讨论 WCF 可靠消息传递功能。  
  
 可靠消息传递是指可靠消息源（称为“源”）如何将消息可靠地传送到可靠的消息目标（称为“目标”）。  
  
 可靠消息传递具有以下几个关键方面：  
  
-   从源发送到目标的消息的传送保证，而不管消息传送或传输是否失败。  
  
-   源和目标相互分离，这为源和目标提供了独立的故障与恢复，即使源或目标不可用，也可以可靠地传送和传输消息。  
  
 可靠消息传递经常伴随高延迟成本。 “延迟”是指消息从源到达目标所需要的时间。 WCF，因此，提供以下类型的可靠消息传送：  
  
-   [可靠会话](../../../../docs/framework/wcf/feature-details/reliable-sessions.md)，提供没有高延迟成本的可靠传送  
  
-   [WCF 中的队列](../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)，提供可靠传送和源与目标之间的分离。  
  
## <a name="reliable-sessions"></a>可靠会话  
 可靠会话使用 WS-ReliableMessaging 协议提供源和目标之间的端到端可靠消息传送，而不管分隔消息（源和目标）终结点的中介的数量和类型如何。 这包括不使用 SOAP 的任何传输中介（例如 HTTP 代理）或在终结点之间流动所必需的使用 SOAP 的中介（例如基于 SOAP 的路由器或网桥）。 可靠会话使用内存中的传送窗口屏蔽 SOAP 消息级别的失败并在传输失败时重新建立连接。  
  
 可靠会话提供低延迟可靠消息传送。 可靠会话通过任何代理或中介为 SOAP 消息提供的功能相当于 TCP 通过 IP 网桥为数据包提供的功能。 有关可靠会话的详细信息，请参阅[可靠会话](../../../../docs/framework/wcf/feature-details/reliable-sessions.md)。  
  
### <a name="queues"></a>队列  
 WCF 中的队列提供可靠传送消息以及分离的源和目标高延迟成本之间。 WCF 排队通信建立在消息队列 (也称为 MSMQ) 之上。  
  
 MSMQ 作为可选项随 Windows 提供，并作为 NT 服务运行。 它捕获代表源的传输队列中要传输的消息，并将消息传递到目标队列。 目标队列代表目标接受消息，待以后目标请求消息时传递。 MSMQ 队列管理器实现可靠的消息传输协议，以使消息不会在传输过程中丢失。 协议可以是本机的，也可以是基于 SOAP 的协议，例如 Soap 可靠消息传递协议 (SRMP)。  
  
 在队列之间与可靠消息传送相耦合的分离，使松耦合的应用程序能够可靠地通信。 与可靠会话不同，源和目标不必同时运行。 这暗示可以出现此类情况：当源产生消息的速率和目标使用消息的速率不匹配时，队列实际上用作一种负载平衡机制。 有关队列的详细信息，请参阅[WCF 中的队列](../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)。  
  
## <a name="see-also"></a>请参阅
- [WCF 中的队列](../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)
- [在 WCF 中排队](../../../../docs/framework/wcf/feature-details/queuing-in-wcf.md)
- [可靠会话](../../../../docs/framework/wcf/feature-details/reliable-sessions.md)
- [可靠会话概述](../../../../docs/framework/wcf/feature-details/reliable-sessions-overview.md)
