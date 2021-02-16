---
title: Fonctions d’API C qui peuvent être appelées uniquement à partir d’une DLL ou d’une XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api called from dll or xll
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6d2d3c824c482e3726cdaefa869393002a80f44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423117"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a>Fonctions d’API C qui peuvent être appelées uniquement à partir d’une DLL ou d’une XLL

**S’applique à** : Excel 2013 | Office 2013 | Visual Studio 
  
L’API C fournit 15 fonctions de rappel Microsoft Excel qui peuvent uniquement être appelées à l’aide des fonctions **Excel4,** **Excel4v,** **Excel12** ou **Excel12v** (ou par l’une de ces fonctions indirectement à l’aide des fonctions Framework **Excel** ou **Excel12f**). Cela signifie qu’ils ne peuvent être appelés qu’à partir d’une DLL ou d’une XLL.
  
## <a name="in-this-section"></a>Contenu de cette section

[xlAbort](xlabort.md)
  
[xlAsyncReturn](xlasyncreturn.md)
  
[xlCoerce](xlcoerce.md)
  
[xlDefineBinaryName](xldefinebinaryname.md)
  
[xlDisableXLMsgs](xldisablexlmsgs.md)
  
[xlEnableXLMsgs](xlenablexlmsgs.md)
  
[xlEventRegister](xleventregister.md)
  
[xlFree](xlfree.md)
  
[xlGetBinaryName](xlgetbinaryname.md)
  
[xlGetHwnd](xlgethwnd.md)
  
[xlGetInst](xlgetinst.md)
  
[xlGetInstPtr](xlgetinstptr.md)
  
[xlGetName](xlgetname.md)
  
[xlRunningOnCluster](xlrunningoncluster.md)
  
[xlSet](xlset.md)
  
[xlSheetId](xlsheetid.md)
  
[xlSheetNm](xlsheetnm.md)
  
[xlStack](xlstack.md)
  
[xlUDF](xludf.md)
  
## <a name="see-also"></a>Voir aussi



[Fonctions de rappel de l’API C Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)

