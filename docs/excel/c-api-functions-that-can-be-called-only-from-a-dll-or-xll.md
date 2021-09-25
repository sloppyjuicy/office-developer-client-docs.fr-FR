---
title: Fonctions d’API C qui peuvent être appelées uniquement à partir d’une DLL ou d’une XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api called from dll or xll
ms.localizationpriority: medium
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'S’applique à : Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8c53a2f68dab76bc68ea756f25d87e351b8700f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605651"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a>Fonctions d’API C qui peuvent être appelées uniquement à partir d’une DLL ou d’une XLL

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
L’API C fournit 15 fonctions de rappel Microsoft Excel qui peuvent uniquement être appelées à l’aide des fonctions **Excel4,** **Excel4v,** **Excel12** ou **Excel12v** (ou par l’une de ces fonctions indirectement à l’aide des fonctions Framework **Excel** ou **Excel12f).** Cela signifie qu’ils ne peuvent être appelés qu’à partir d’une DLL ou d’une XLL.
  
## <a name="in-this-section"></a>Dans cette section

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

