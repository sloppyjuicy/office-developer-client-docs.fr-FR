---
title: Vérification du blocage d’une pièce jointe
description: Cet article explique comment vérifier qu’une pièce jointe est bloquée par Microsoft Outlook 2010 ou Microsoft Outlook 2013 pour l’affichage et l’indexation, et fournit une syntaxe.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
ms.openlocfilehash: 4085c1dae8bde8a4f26f04b8a3a8027729633669
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65812382"
---
# <a name="verify-an-attachment-is-blocked"></a>Vérification du blocage d’une pièce jointe

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cet exemple de code en C++ montre comment utiliser l’interface [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) pour déterminer si une pièce jointe est bloquée par Microsoft Outlook 2010 ou Microsoft Outlook 2013 pour l’affichage et l’indexation. 
  
[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) est dérivé de l’interface [IUnknown](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) . Vous pouvez obtenir l’interface [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) en appelant [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) sur l’objet de session MAPI, en demandant **IID_IAttachmentSecurity**. [IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) retourne **true** dans _pfBlocked_ si la pièce jointe est considérée comme non sécurisée par Outlook 2010 ou Outlook 2013 et est bloquée pour l’affichage et l’indexation dans Outlook 2010 ou Outlook 2013. 
  
```cpp
HRESULT IsAttachmentBlocked(LPMAPISESSION lpMAPISession, LPCWSTR pwszFileName, BOOL* pfBlocked) 
{ 
    if (!lpMAPISession || !pwszFileName || !pfBlocked) return MAPI_E_INVALID_PARAMETER; 
 
    HRESULT hRes = S_OK; 
    IAttachmentSecurity* lpAttachSec = NULL; 
    BOOL bBlocked = false; 
 
    hRes = lpMAPISession-&gt;QueryInterface(IID_IAttachmentSecurity,(void**)&amp;lpAttachSec); 
    if (SUCCEEDED(hRes) &amp;&amp; lpAttachSec) 
    { 
        hRes = lpAttachSec-&gt;IsAttachmentBlocked(pwszFileName,&amp;bBlocked); 
    } 
    if (lpAttachSec) lpAttachSec-&gt;Release(); 
 
    *pfBlocked = bBlocked; 
    return hRes; 
}

```


