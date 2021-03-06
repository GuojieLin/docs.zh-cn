---
title: 如何：启用 TAB 键能够移出 ToolStrip 控件
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], moving between
- TAB key [Windows Forms], enabling
- ToolStrip control [Windows Forms], moving from
ms.assetid: 40f9e88b-09a3-428e-8da8-c00bb65079c6
ms.openlocfilehash: e1d7917d7e12ba286e7ddf4e95a68769852a17f7
ms.sourcegitcommit: 160a88c8087b0e63606e6e35f9bd57fa5f69c168
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/09/2019
ms.locfileid: "57704331"
---
# <a name="how-to-enable-the-tab-key-to-move-out-of-a-toolstrip-control"></a>如何：启用 TAB 键能够移出 ToolStrip 控件
使用以下过程以使用户能够按 TAB 键移动共<xref:System.Windows.Forms.ToolStrip>到下一个控件的 tab 键顺序。  
  
 <xref:System.Windows.Forms.ToolStrip>接受 TAB 键和箭头键选择项中的第一个按<xref:System.Windows.Forms.ToolStrip>。 当用户在第二次按 TAB 键时下, 一个控件，用户会在 tab 键顺序中。  
  
### <a name="to-enable-the-user-to-press-the-tab-key-to-move-out-of-a-toolstrip-to-the-next-control"></a>若要使用户能够按 TAB 键能够移出 ToolStrip 到下一个控件  
  
-   设置<xref:System.Windows.Forms.ToolStrip.TabStop%2A>的属性<xref:System.Windows.Forms.ToolStrip>到`true`。  
  
## <a name="see-also"></a>请参阅
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.TabStop%2A>
- [ToolStrip 控件概述](toolstrip-control-overview-windows-forms.md)
