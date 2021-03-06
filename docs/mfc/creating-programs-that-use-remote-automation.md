---
title: "创建使用远程自动化的程序 |Microsoft 文档"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- C++
helpviewer_keywords:
- Remote Automation, creating programs
ms.assetid: 8eb31320-1037-4029-b1f3-fdc9406dbaf1
caps.latest.revision: 
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 86a9b9f4dccaaa3a97366dffb11955d3b148aff5
ms.sourcegitcommit: fa7a6dccddce3747389c91277a53e296f905305c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/14/2018
---
# <a name="creating-programs-that-use-remote-automation"></a>创建使用远程自动化的程序
任何自动化对象和任何自动化控制器都能使用远程自动化，而无需更改源代码、重新编译或重新链接。 一旦您拥有可本地工作的设置（即在同一计算机上），则只需执行几个步骤即可远程操作它。  
  
#### <a name="to-execute-the-remote-automation-object"></a>执行远程自动化对象  
  
1.  在一台或多台客户端计算机上注册此应用程序。  
  
2.  将客户端访问配置为使用远程服务器。  
  
3.  在一台或多台服务器计算机上安装并注册此应用程序。  
  
4.  将服务器配置为允许远程激活。  
  
5.  在服务器计算机上安装自动化管理器。  
  
6.  在服务器上运行自动化管理器。  
  
7.  在客户端上运行应用程序。  
  
 在客户端计算机上加载并执行服务器应用程序是可以最轻松地完成步骤 1，因为大多数服务器都是自行注册的。 如果你预先本地测试了此设置，则该阶段已完成。 如果服务器应用程序不是自行注册的，您可能需要将其设置为自行注册的。 否则，您将需要提供注册文件，本地用户可运行该文件来执行此步骤。 如果您未执行上述操作，则您或管理员将需要手动编辑注册表（建议不对所有用户执行此过程，而只对大多数高级用户执行此过程）。  
  
 步骤 2 需要使用远程自动化连接 (RAC) 管理器。 运行 RAC 管理器并确保服务器连接选项卡位于顶部。 接下来，为中的服务器对象中找到项**OLE 类**窗格中，然后单击它。 然后转到**网络地址**组合框中，输入将在其上运行远程可执行文件的服务器计算机的名称。 例如，您可以输入\\\MyServer 此处。 然后从提供的列表中选择适当的网络协议。 您可能需要与您的网络管理员联系以确定推荐协议。 在许多情况下，该协议将是 TCP/IP。 最后，您可能需要选择一个身份验证级别。 在大多数情况下，该级别将为“(无)”或“默认”。 现在，右键单击中的服务器**OLE 类**窗格。 这将生成一个快捷菜单，可从该菜单中选择本地或远程操作。 选择远程操作。  
  
 步骤 3 涉及在所选的服务器计算机上正确安装并注册服务器应用程序。 同样，如果应用程序是自行注册的，则执行一次应用程序也将对其进行注册。  
  
 步骤 4 涉及将服务器配置为允许远程操作。 在服务器计算机上运行 RAC 管理器并确保**客户端访问** 选项卡具有焦点。 选择所需的激活模型 (通常**通过密钥允许远程创建**。 如果你选择此选项，你还需要单击**允许远程激活**复选框以设置为 Y 的注册表项的值)。 如果你选择允许远程创建 (ACL) 选项，你还可以选择按下编辑 ACL**编辑 ACL**按钮。  
  
 若要允许远程自动化运行，您需要确保已在服务器计算机上安装并运行自动化管理器。 如果未安装此管理器，请将 AUTMGR32.EXE 复制到 Windows 系统目录。 有关如何执行此操作的信息，请参阅[远程自动化安装](../mfc/remote-automation-installation.md)。 若要启动远程自动化，请运行自动化管理器。 它将显示一个小型状态窗口，其中显示了大量消息。 此窗口在启动后将自行最小化。 如果你想要继续查看状态信息，则可以单击**自动化管理器**任务栏来还原此窗口中的选项卡。  
  
 最后一步是在客户端计算机上执行客户端应用程序。 如果您已按照上述步骤操作，则该应用程序将连接到服务器对象并且就像在本地运行一样准确运行，只不过运行速度慢一点。  
  
 请注意，利用 RAC 管理器，您还可以单击某个单选按钮来在远程自动化和分布式 COM（DCOM，在那些支持 DCOM 的平台上）之间进行切换。 如果您选择 DCOM，则可设置各种其他的配置选项。 有关更多详细信息，请参见 DCOM 文档。  
  
## <a name="see-also"></a>请参阅  
 [远程自动化](../mfc/remote-automation.md)   
 [使用 AUTOCLIK 和 AUTODRIV 运行远程自动化](../mfc/running-remote-automation-using-autoclik-and-autodriv.md)

