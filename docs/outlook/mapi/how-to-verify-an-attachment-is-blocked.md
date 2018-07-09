---
title: Vérifiez la que pièce jointe est bloquée
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 69663470-45f3-86ed-e015-eba32b5a7233
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: a21383e0ea6920075a57d872e82851462bf0e8d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783506"
---
# <a name="verify-an-attachment-is-blocked"></a><span data-ttu-id="64ece-103">Vérifiez la que pièce jointe est bloquée</span><span class="sxs-lookup"><span data-stu-id="64ece-103">Verify an attachment is blocked</span></span>

<span data-ttu-id="64ece-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="64ece-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="64ece-105">En C++, cet exemple de code montre comment utiliser la [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface permettant de savoir si une pièce jointe est bloquée par Microsoft Outlook 2010 ou Microsoft Outlook 2013 pour l’affichage et l’indexation.</span><span class="sxs-lookup"><span data-stu-id="64ece-105">This code sample in C++ shows how to use the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface to find out whether an attachment is blocked by Microsoft Outlook 2010 or Microsoft Outlook 2013 for viewing and indexing.</span></span> 
  
<span data-ttu-id="64ece-106">[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) est dérivé de l’interface [IUnknown](http://msdn.microsoft.com/fr-fr/library/ms680509%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="64ece-106">[IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) is derived from the [IUnknown](http://msdn.microsoft.com/fr-fr/library/ms680509%28VS.85%29.aspx) interface.</span></span> <span data-ttu-id="64ece-107">Vous pouvez obtenir le [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface en appelant [IUnknown::QueryInterface](http://msdn.microsoft.com/fr-fr/library/ms682521%28v=VS.85%29.aspx) sur l’objet de session MAPI, qui demande **IID_IAttachmentSecurity**.</span><span class="sxs-lookup"><span data-stu-id="64ece-107">You can obtain the [IAttachmentSecurity : IUnknown](iattachmentsecurityiunknown.md) interface by calling [IUnknown::QueryInterface](http://msdn.microsoft.com/fr-fr/library/ms682521%28v=VS.85%29.aspx) on the MAPI session object, requesting **IID_IAttachmentSecurity**.</span></span> <span data-ttu-id="64ece-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) renvoie **la valeur true** dans _pfBlocked_ si la pièce jointe est considérée comme non sécurisée par Outlook 2010 ou Outlook 2013 et est bloquée pour l’affichage et l’indexation dans Outlook 2010 ou Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="64ece-108">[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) returns **true** in  _pfBlocked_ if the attachment is considered unsafe by Outlook 2010 or Outlook 2013 and is blocked for viewing and indexing in Outlook 2010 or Outlook 2013.</span></span> 
  
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


