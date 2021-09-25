---
title: Vérification du blocage d’une pièce jointe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: 57c7c3861073910a1f5331c71e9e5ecc1c0c83a0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576197"
---
# <a name="verify-an-attachment-is-blocked"></a>Vérification du blocage d’une pièce jointe

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cet exemple de code en C++ montre comment utiliser l’interface [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) pour savoir si une pièce jointe est bloquée par Microsoft Outlook 2010 ou Microsoft Outlook 2013 pour l’affichage et l’indexation. 
  
[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) est dérivé de [l’interface IUnknown.](https://msdn.microsoft.com/library/ms680509%28VS.85%29.aspx) Vous pouvez obtenir l’interface [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) en appelant [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) sur l’objet de session MAPI, en demandant **IID_IAttachmentSecurity**. [IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) renvoie **true** dans _pfBlocked_ si la pièce jointe est considérée comme non sûre par Outlook 2010 ou Outlook 2013 et est bloquée pour l’affichage et l’indexation dans Outlook 2010 ou Outlook 2013. 
  
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


