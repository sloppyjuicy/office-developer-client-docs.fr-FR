---
title: Fonctions de l'API C qui ne peuvent être appelées qu'à partir d'une DLL ou d'une XLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- fonctions [Excel 2007], API c appelée à partir de dll ou XLL
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'S�applique �: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e6d2d3c824c482e3726cdaefa869393002a80f44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301651"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a>Fonctions de l'API C qui ne peuvent être appelées qu'à partir d'une DLL ou d'une XLL

**S’applique à**: Excel 2013 | Office 2013 | Visual Studio 
  
L'API C fournit 15 fonctions de rappel Microsoft Excel qui ne peuvent être appelées qu'à l'aide des fonctions **Excel4**, **Excel4v**, **Excel12**ou **Excel12v** (ou par l'une de ces fonctions indirectement à l'aide des fonctions de l'infrastructure **Excel **ou **Excel12f**). Cela signifie qu'ils peuvent uniquement être appelés à partir d'un fichier DLL ou XLL.
  
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



[Les fonctions de rappel de l'API C Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)

