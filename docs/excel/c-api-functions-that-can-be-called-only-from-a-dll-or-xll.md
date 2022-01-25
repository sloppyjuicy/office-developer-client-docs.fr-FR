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
ms.openlocfilehash: 60c9480c0763bac36f2f4bc8937fd7a3a8b0af8a
ms.sourcegitcommit: 193df57ebf141020852d2ebc8cf0931edb71574a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/25/2022
ms.locfileid: "62199142"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a>Fonctions d’API C qui peuvent être appelées uniquement à partir d’une DLL ou d’une XLL

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
L’API C fournit 15 fonctions de rappel Microsoft Excel qui peuvent uniquement être appelées à l’aide des fonctions **Excel4,** **Excel4v,** **Excel12** ou **Excel12v** (ou par l’une de ces fonctions indirectement à l’aide des fonctions Framework **Excel** ou **Excel12f**). Cela signifie qu’ils ne peuvent être appelés qu’à partir d’une DLL ou d’une XLL.
  
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



[Les fonctions de rappel de l'API C Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)

