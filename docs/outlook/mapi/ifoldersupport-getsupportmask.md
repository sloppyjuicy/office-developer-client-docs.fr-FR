---
title: IFolderSupportGetSupportMask
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IFolderSupport.GetSupportMask
api_type:
- COM
ms.assetid: 8d8aaeb7-57d7-ba4c-95d1-a5368cfc4afe
ms.openlocfilehash: 57933ae3db72ef2f1a57832b704273f06d437218
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373955"
---
# <a name="ifoldersupportgetsupportmask"></a>IFolderSupport::GetSupportMask

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Obtient des informations sur la prise en charge d’un dossier pour le partage.
  
```cpp
HRESULT GetSupportMask( 
    DWORD * pdwSupportMask 
); 
```

## <a name="parameters"></a>Paramètres

 _pdwSupportMask_
  
> [out] Masque de bits indiquant si le dossier prend en charge le partage.
    
 **FS_NONE**
  
> Indique que le dossier ne prend pas en charge le partage.
    
 **FS_SUPPORTS_SHARING**
  
> Indique que le dossier prend en charge le partage.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’appel a réussi.
    

